---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526714"
---
# <span data-ttu-id="16609-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="16609-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="16609-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16609-102">SYNOPSIS</span></span>
<span data-ttu-id="16609-103">Pobiera szczegóły zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="16609-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16609-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16609-104">SYNTAX</span></span>

### <span data-ttu-id="16609-105">JobFilterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="16609-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16609-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="16609-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16609-107">Opis</span><span class="sxs-lookup"><span data-stu-id="16609-107">DESCRIPTION</span></span>
<span data-ttu-id="16609-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupJobDetails** pobiera dane zadania kopii zapasowej Azure dotyczące określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="16609-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="16609-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="16609-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="16609-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16609-110">EXAMPLES</span></span>

### <span data-ttu-id="16609-111">Przykład 1: pobieranie szczegółów zadania tworzenia kopii zapasowej dla nieudanych zadań</span><span class="sxs-lookup"><span data-stu-id="16609-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="16609-112">Pierwsze polecenie pobiera tablicę nieudanych zadań w magazynie, a następnie zapisuje je w tablicy $Jobs.</span><span class="sxs-lookup"><span data-stu-id="16609-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="16609-113">Drugie polecenie pobiera szczegóły zadania z nieudanymi zadaniami w $Jobs, a następnie zapisuje je w zmiennej $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="16609-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="16609-114">W ostatnim poleceniu są wyświetlane szczegóły błędu dotyczące zadań zakończonych niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="16609-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="16609-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16609-115">PARAMETERS</span></span>

### <span data-ttu-id="16609-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16609-116">-DefaultProfile</span></span>
<span data-ttu-id="16609-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16609-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16609-118">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="16609-118">-Job</span></span>
<span data-ttu-id="16609-119">Określa zadanie do pobrania.</span><span class="sxs-lookup"><span data-stu-id="16609-119">Specifies the job to get.</span></span>
<span data-ttu-id="16609-120">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="16609-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16609-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="16609-121">-JobId</span></span>
<span data-ttu-id="16609-122">Określa identyfikator zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="16609-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="16609-123">Identyfikator jest właściwością InstanceId obiektu **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="16609-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16609-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16609-124">CommonParameters</span></span>
<span data-ttu-id="16609-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16609-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16609-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16609-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16609-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16609-127">INPUTS</span></span>

### <span data-ttu-id="16609-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="16609-128">None</span></span>
<span data-ttu-id="16609-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="16609-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16609-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16609-130">OUTPUTS</span></span>

### <span data-ttu-id="16609-131">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="16609-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="16609-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16609-132">NOTES</span></span>

## <span data-ttu-id="16609-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16609-133">RELATED LINKS</span></span>

[<span data-ttu-id="16609-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="16609-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


