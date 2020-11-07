---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: bf4ba77a7162faaf593e11b68a82fe5a6e55df1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716960"
---
# <span data-ttu-id="ea36c-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="ea36c-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="ea36c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea36c-102">SYNOPSIS</span></span>
<span data-ttu-id="ea36c-103">Pobiera szczegóły zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="ea36c-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea36c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea36c-104">SYNTAX</span></span>

### <span data-ttu-id="ea36c-105">JobsFiltersSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea36c-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea36c-106">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="ea36c-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea36c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ea36c-107">DESCRIPTION</span></span>
<span data-ttu-id="ea36c-108">Polecenie cmdlet **Get-AzureRmBackupJobDetails** pobiera szczegółowe informacje o zadaniu kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="ea36c-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="ea36c-109">Za pomocą tego polecenia cmdlet można zbierać informacje o zadaniu, które nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="ea36c-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="ea36c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea36c-110">EXAMPLES</span></span>

### <span data-ttu-id="ea36c-111">Przykład 1. Wyświetlanie szczegółów zadania zakończonego niepowodzeniem</span><span class="sxs-lookup"><span data-stu-id="ea36c-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="ea36c-112">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="ea36c-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ea36c-113">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="ea36c-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="ea36c-114">Drugie polecenie pobiera zadania zakończone niepowodzeniem z magazynu w $Vault, a następnie zapisuje je w zmiennej tablicowej $Jobs.</span><span class="sxs-lookup"><span data-stu-id="ea36c-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>
<span data-ttu-id="ea36c-115">Trzecie zadanie otrzymuje szczegóły dla pierwszego zadania w zmiennej $Jobs, a następnie zapisuje te dane w zmiennej $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="ea36c-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>
<span data-ttu-id="ea36c-116">Polecenie ostatnie wyświetla Właściwość **ErrorDetails** $JobDetails przy użyciu standardowej składni z kropką.</span><span class="sxs-lookup"><span data-stu-id="ea36c-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="ea36c-117">Przykład 2: wyświetlanie zalecanej akcji dla zadania zakończonego niepowodzeniem</span><span class="sxs-lookup"><span data-stu-id="ea36c-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="ea36c-118">To polecenie wyświetla zalecaną akcję ze zmiennej $JobDetails utworzonej w pierwszym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="ea36c-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="ea36c-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea36c-119">PARAMETERS</span></span>

### <span data-ttu-id="ea36c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea36c-120">-DefaultProfile</span></span>
<span data-ttu-id="ea36c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ea36c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea36c-122">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="ea36c-122">-Job</span></span>
<span data-ttu-id="ea36c-123">Określa zadanie, dla którego to polecenie cmdlet pobiera szczegóły.</span><span class="sxs-lookup"><span data-stu-id="ea36c-123">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="ea36c-124">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="ea36c-124">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea36c-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="ea36c-125">-JobId</span></span>
<span data-ttu-id="ea36c-126">Określa identyfikator zadania, dla którego to polecenie cmdlet pobiera szczegóły.</span><span class="sxs-lookup"><span data-stu-id="ea36c-126">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="ea36c-127">Identyfikator jest właściwością **InstanceId** obiektu **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="ea36c-127">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="ea36c-128">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenie Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="ea36c-128">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea36c-129">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="ea36c-129">-Vault</span></span>
<span data-ttu-id="ea36c-130">Określa magazyn kopii zapasowych, dla którego to polecenie cmdlet pobiera szczegóły zadania.</span><span class="sxs-lookup"><span data-stu-id="ea36c-130">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="ea36c-131">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="ea36c-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea36c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea36c-132">CommonParameters</span></span>
<span data-ttu-id="ea36c-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea36c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea36c-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea36c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea36c-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea36c-135">INPUTS</span></span>

### <span data-ttu-id="ea36c-136">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="ea36c-136">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>
<span data-ttu-id="ea36c-137">Parametry: zadanie (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ea36c-137">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="ea36c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea36c-138">OUTPUTS</span></span>

### <span data-ttu-id="ea36c-139">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="ea36c-139">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJobDetails</span></span>

## <span data-ttu-id="ea36c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea36c-140">NOTES</span></span>

## <span data-ttu-id="ea36c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea36c-141">RELATED LINKS</span></span>

[<span data-ttu-id="ea36c-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ea36c-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="ea36c-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ea36c-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


