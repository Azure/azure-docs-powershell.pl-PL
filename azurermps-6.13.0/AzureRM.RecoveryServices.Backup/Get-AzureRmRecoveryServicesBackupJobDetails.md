---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 7d39ce49a76d8519f2eacf0649c52051290274f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526161"
---
# <span data-ttu-id="368b6-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="368b6-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="368b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="368b6-102">SYNOPSIS</span></span>
<span data-ttu-id="368b6-103">Pobiera szczegóły zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="368b6-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="368b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="368b6-104">SYNTAX</span></span>

### <span data-ttu-id="368b6-105">JobFilterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="368b6-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="368b6-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="368b6-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="368b6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="368b6-107">DESCRIPTION</span></span>
<span data-ttu-id="368b6-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupJobDetails** pobiera dane zadania kopii zapasowej Azure dotyczące określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="368b6-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="368b6-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="368b6-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="368b6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="368b6-110">EXAMPLES</span></span>

### <span data-ttu-id="368b6-111">Przykład 1: pobieranie szczegółów zadania tworzenia kopii zapasowej dla nieudanych zadań</span><span class="sxs-lookup"><span data-stu-id="368b6-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="368b6-112">Pierwsze polecenie pobiera tablicę nieudanych zadań w magazynie, a następnie zapisuje je w tablicy $Jobs.</span><span class="sxs-lookup"><span data-stu-id="368b6-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="368b6-113">Drugie polecenie pobiera szczegóły zadania z nieudanymi zadaniami w $Jobs, a następnie zapisuje je w zmiennej $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="368b6-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="368b6-114">W ostatnim poleceniu są wyświetlane szczegóły błędu dotyczące zadań zakończonych niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="368b6-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="368b6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="368b6-115">PARAMETERS</span></span>

### <span data-ttu-id="368b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="368b6-116">-DefaultProfile</span></span>
<span data-ttu-id="368b6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="368b6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="368b6-118">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="368b6-118">-Job</span></span>
<span data-ttu-id="368b6-119">Określa zadanie do pobrania.</span><span class="sxs-lookup"><span data-stu-id="368b6-119">Specifies the job to get.</span></span>
<span data-ttu-id="368b6-120">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="368b6-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="368b6-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="368b6-121">-JobId</span></span>
<span data-ttu-id="368b6-122">Określa identyfikator zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="368b6-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="368b6-123">Identyfikator jest właściwością InstanceId obiektu **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="368b6-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="368b6-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="368b6-124">-VaultId</span></span>
<span data-ttu-id="368b6-125">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="368b6-125">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="368b6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="368b6-126">CommonParameters</span></span>
<span data-ttu-id="368b6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="368b6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="368b6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="368b6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="368b6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="368b6-129">INPUTS</span></span>

### <span data-ttu-id="368b6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="368b6-130">System.String</span></span>
<span data-ttu-id="368b6-131">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="368b6-131">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="368b6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="368b6-132">OUTPUTS</span></span>

### <span data-ttu-id="368b6-133">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="368b6-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="368b6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="368b6-134">NOTES</span></span>

## <span data-ttu-id="368b6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="368b6-135">RELATED LINKS</span></span>

[<span data-ttu-id="368b6-136">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="368b6-136">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


