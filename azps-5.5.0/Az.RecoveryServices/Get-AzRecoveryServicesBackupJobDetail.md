---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 6c12cccff6305c96bf2df037e32b8af35170454a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192986"
---
# <span data-ttu-id="3ca1c-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="3ca1c-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="3ca1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ca1c-102">SYNOPSIS</span></span>

<span data-ttu-id="3ca1c-103">Pobiera szczegółowe informacje dotyczące zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="3ca1c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3ca1c-104">SYNTAX</span></span>

### <span data-ttu-id="3ca1c-105">JobFilterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ca1c-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="3ca1c-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ca1c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3ca1c-107">DESCRIPTION</span></span>

<span data-ttu-id="3ca1c-108">Polecenie **cmdlet Get-AzRecoveryServicesBackupJobDetail** pobiera szczegóły zadania kopii zapasowej platformy Azure dla określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="3ca1c-109">Ustaw kontekst magazynu przy użyciu parametru -VaultId.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="3ca1c-110">Ostrzeżenie: **Alias Get-AzRecoveryServicesBackupJobDetails** zostanie usunięty w przyszłej wersji z podziałem na zmiany.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="3ca1c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3ca1c-111">EXAMPLES</span></span>

### <span data-ttu-id="3ca1c-112">Przykład 1. Uzyskiwanie szczegółów zadania kopii zapasowej dla zadań, których wykonywanie zakończyło się niepowodzeniem</span><span class="sxs-lookup"><span data-stu-id="3ca1c-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="3ca1c-113">Pierwsze polecenie pobiera odpowiedni magazyn.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="3ca1c-114">Drugie polecenie pobiera tablicę zadań, których niepowodzenie nie powiodło się w magazynie, a następnie przechowuje je w $Jobs tablicy.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="3ca1c-115">Trzecie polecenie pobiera szczegółowe informacje o zadaniu pierwszego zadania, które nie powiodło się w programie $Jobs, a następnie przechowuje je w $JobDetails danych.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="3ca1c-116">Końcowe polecenie wyświetla szczegóły błędu dla zadań, których nie udało się znaleźć.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="3ca1c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ca1c-117">PARAMETERS</span></span>

### <span data-ttu-id="3ca1c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca1c-118">-DefaultProfile</span></span>

<span data-ttu-id="3ca1c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca1c-120">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="3ca1c-120">-Job</span></span>

<span data-ttu-id="3ca1c-121">Określa zadanie do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-121">Specifies the job to get.</span></span>
<span data-ttu-id="3ca1c-122">Aby uzyskać obiekt **BackupJob,** użyj polecenia cmdlet **Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="3ca1c-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="3ca1c-123">- JobId</span><span class="sxs-lookup"><span data-stu-id="3ca1c-123">-JobId</span></span>

<span data-ttu-id="3ca1c-124">Określa identyfikator zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="3ca1c-125">Identyfikator jest właściwością JobId obiektu **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase.**</span><span class="sxs-lookup"><span data-stu-id="3ca1c-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="3ca1c-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3ca1c-126">-VaultId</span></span>

<span data-ttu-id="3ca1c-127">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3ca1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca1c-128">CommonParameters</span></span>
<span data-ttu-id="3ca1c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca1c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca1c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ca1c-131">INPUTS</span></span>

### <span data-ttu-id="3ca1c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3ca1c-132">System.String</span></span>

## <span data-ttu-id="3ca1c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ca1c-133">OUTPUTS</span></span>

### <span data-ttu-id="3ca1c-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="3ca1c-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3ca1c-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3ca1c-135">NOTES</span></span>

## <span data-ttu-id="3ca1c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ca1c-136">RELATED LINKS</span></span>

[<span data-ttu-id="3ca1c-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3ca1c-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
