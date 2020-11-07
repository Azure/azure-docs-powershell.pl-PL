---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: c8cf8074d6b077ed67f46f747c80439b41f9abca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872692"
---
# <span data-ttu-id="5413d-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="5413d-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="5413d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5413d-102">SYNOPSIS</span></span>

<span data-ttu-id="5413d-103">Pobiera szczegóły zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="5413d-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="5413d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5413d-104">SYNTAX</span></span>

### <span data-ttu-id="5413d-105">JobFilterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5413d-105">JobFilterSet (Default)</span></span>

```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5413d-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="5413d-106">IdFilterSet</span></span>

```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5413d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5413d-107">DESCRIPTION</span></span>

<span data-ttu-id="5413d-108">Polecenie cmdlet **Get-AzRecoveryServicesBackupJobDetail** pobiera dane zadania kopii zapasowej Azure dotyczące określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="5413d-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="5413d-109">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="5413d-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="5413d-110">Ostrzeżenie: alias **Get-AzRecoveryServicesBackupJobDetails** zostanie usunięty w przyszłym wydaniu w ramach zmiany podziału.</span><span class="sxs-lookup"><span data-stu-id="5413d-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="5413d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5413d-111">EXAMPLES</span></span>

### <span data-ttu-id="5413d-112">Przykład 1: pobieranie szczegółów zadania tworzenia kopii zapasowej dla nieudanych zadań</span><span class="sxs-lookup"><span data-stu-id="5413d-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="5413d-113">Pierwsze polecenie pobiera tablicę nieudanych zadań w magazynie, a następnie zapisuje je w tablicy $Jobs.</span><span class="sxs-lookup"><span data-stu-id="5413d-113">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="5413d-114">Drugie polecenie pobiera szczegóły zadania z nieudanymi zadaniami w $Jobs, a następnie zapisuje je w zmiennej $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="5413d-114">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="5413d-115">W ostatnim poleceniu są wyświetlane szczegóły błędu dotyczące zadań zakończonych niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="5413d-115">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="5413d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5413d-116">PARAMETERS</span></span>

### <span data-ttu-id="5413d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5413d-117">-DefaultProfile</span></span>

<span data-ttu-id="5413d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5413d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5413d-119">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="5413d-119">-Job</span></span>

<span data-ttu-id="5413d-120">Określa zadanie do pobrania.</span><span class="sxs-lookup"><span data-stu-id="5413d-120">Specifies the job to get.</span></span>
<span data-ttu-id="5413d-121">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="5413d-121">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="5413d-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="5413d-122">-JobId</span></span>

<span data-ttu-id="5413d-123">Określa identyfikator zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="5413d-123">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="5413d-124">Identyfikator jest właściwością JobId obiektu **Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="5413d-124">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="5413d-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5413d-125">-VaultId</span></span>

<span data-ttu-id="5413d-126">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="5413d-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5413d-127">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5413d-127">-CommonParameters</span></span>

<span data-ttu-id="5413d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5413d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5413d-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5413d-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5413d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5413d-130">INPUTS</span></span>

### <span data-ttu-id="5413d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5413d-131">System.String</span></span>

## <span data-ttu-id="5413d-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5413d-132">OUTPUTS</span></span>

### <span data-ttu-id="5413d-133">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="5413d-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5413d-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5413d-134">NOTES</span></span>

## <span data-ttu-id="5413d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5413d-135">RELATED LINKS</span></span>

[<span data-ttu-id="5413d-136">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5413d-136">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
