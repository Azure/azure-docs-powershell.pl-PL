---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: f9f0808db919ad5d1d38b29daa720fb9b8a5baee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528298"
---
# <span data-ttu-id="1264a-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="1264a-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="1264a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1264a-102">SYNOPSIS</span></span>
<span data-ttu-id="1264a-103">Pobiera szczegóły zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="1264a-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1264a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1264a-104">SYNTAX</span></span>

### <span data-ttu-id="1264a-105">JobsFiltersSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1264a-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1264a-106">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="1264a-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1264a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1264a-107">DESCRIPTION</span></span>
<span data-ttu-id="1264a-108">Polecenie cmdlet **Get-AzureRmBackupJobDetails** pobiera szczegółowe informacje o zadaniu kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="1264a-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="1264a-109">Za pomocą tego polecenia cmdlet można zbierać informacje o zadaniu, które nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="1264a-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="1264a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1264a-110">EXAMPLES</span></span>

### <span data-ttu-id="1264a-111">Przykład 1. Wyświetlanie szczegółów zadania zakończonego niepowodzeniem</span><span class="sxs-lookup"><span data-stu-id="1264a-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="1264a-112">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="1264a-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="1264a-113">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="1264a-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="1264a-114">Drugie polecenie pobiera zadania zakończone niepowodzeniem z magazynu w $Vault, a następnie zapisuje je w zmiennej tablicowej $Jobs.</span><span class="sxs-lookup"><span data-stu-id="1264a-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>

<span data-ttu-id="1264a-115">Trzecie zadanie otrzymuje szczegóły dla pierwszego zadania w zmiennej $Jobs, a następnie zapisuje te dane w zmiennej $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="1264a-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>

<span data-ttu-id="1264a-116">Polecenie ostatnie wyświetla Właściwość **ErrorDetails** $JobDetails przy użyciu standardowej składni z kropką.</span><span class="sxs-lookup"><span data-stu-id="1264a-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="1264a-117">Przykład 2: wyświetlanie zalecanej akcji dla zadania zakończonego niepowodzeniem</span><span class="sxs-lookup"><span data-stu-id="1264a-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="1264a-118">To polecenie wyświetla zalecaną akcję ze zmiennej $JobDetails utworzonej w pierwszym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="1264a-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="1264a-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1264a-119">PARAMETERS</span></span>

### <span data-ttu-id="1264a-120">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="1264a-120">-Job</span></span>
<span data-ttu-id="1264a-121">Określa zadanie, dla którego to polecenie cmdlet pobiera szczegóły.</span><span class="sxs-lookup"><span data-stu-id="1264a-121">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="1264a-122">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="1264a-122">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="1264a-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="1264a-123">-JobId</span></span>
<span data-ttu-id="1264a-124">Określa identyfikator zadania, dla którego to polecenie cmdlet pobiera szczegóły.</span><span class="sxs-lookup"><span data-stu-id="1264a-124">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="1264a-125">Identyfikator jest właściwością **InstanceId** obiektu **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="1264a-125">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="1264a-126">Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenie Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="1264a-126">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

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

### <span data-ttu-id="1264a-127">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="1264a-127">-Vault</span></span>
<span data-ttu-id="1264a-128">Określa magazyn kopii zapasowych, dla którego to polecenie cmdlet pobiera szczegóły zadania.</span><span class="sxs-lookup"><span data-stu-id="1264a-128">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="1264a-129">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="1264a-129">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="1264a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1264a-130">-DefaultProfile</span></span>
<span data-ttu-id="1264a-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1264a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1264a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1264a-132">CommonParameters</span></span>
<span data-ttu-id="1264a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1264a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1264a-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1264a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1264a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1264a-135">INPUTS</span></span>

### <span data-ttu-id="1264a-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1264a-136">None</span></span>

## <span data-ttu-id="1264a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1264a-137">OUTPUTS</span></span>

### <span data-ttu-id="1264a-138">AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="1264a-138">AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="1264a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1264a-139">NOTES</span></span>
* <span data-ttu-id="1264a-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1264a-140">None</span></span>

## <span data-ttu-id="1264a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1264a-141">RELATED LINKS</span></span>

[<span data-ttu-id="1264a-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="1264a-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="1264a-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="1264a-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


