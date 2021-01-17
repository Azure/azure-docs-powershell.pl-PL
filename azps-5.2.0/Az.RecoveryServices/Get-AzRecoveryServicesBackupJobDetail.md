---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343093"
---
# <span data-ttu-id="2ea55-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="2ea55-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="2ea55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ea55-102">SYNOPSIS</span></span>

<span data-ttu-id="2ea55-103">Pobiera szczegóły zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2ea55-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="2ea55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ea55-104">SYNTAX</span></span>

### <span data-ttu-id="2ea55-105">JobFilterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2ea55-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ea55-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="2ea55-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ea55-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2ea55-107">DESCRIPTION</span></span>

<span data-ttu-id="2ea55-108">Polecenie cmdlet **Get-AzRecoveryServicesBackupJobDetail** pobiera dane zadania kopii zapasowej Azure dotyczące określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="2ea55-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="2ea55-109">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="2ea55-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="2ea55-110">Ostrzeżenie: alias **Get-AzRecoveryServicesBackupJobDetails** zostanie usunięty w przyszłym wydaniu w ramach zmiany podziału.</span><span class="sxs-lookup"><span data-stu-id="2ea55-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="2ea55-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ea55-111">EXAMPLES</span></span>

### <span data-ttu-id="2ea55-112">Przykład 1: pobieranie szczegółów zadania tworzenia kopii zapasowej dla nieudanych zadań</span><span class="sxs-lookup"><span data-stu-id="2ea55-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="2ea55-113">Pierwsze polecenie pobiera odpowiedni magazyn.</span><span class="sxs-lookup"><span data-stu-id="2ea55-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="2ea55-114">Drugie polecenie pobiera tablicę nieudanych zadań w magazynie, a następnie zapisuje je w tablicy $Jobs.</span><span class="sxs-lookup"><span data-stu-id="2ea55-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="2ea55-115">W trzecim poleceniu są dostępne szczegóły zadania dla pierwszego zadania zakończonego niepowodzeniem w $Jobs, a następnie są one przechowywane w zmiennej $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="2ea55-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="2ea55-116">W ostatnim poleceniu są wyświetlane szczegóły błędu dotyczące zadań zakończonych niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="2ea55-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="2ea55-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ea55-117">PARAMETERS</span></span>

### <span data-ttu-id="2ea55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea55-118">-DefaultProfile</span></span>

<span data-ttu-id="2ea55-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea55-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ea55-120">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="2ea55-120">-Job</span></span>

<span data-ttu-id="2ea55-121">Określa zadanie do pobrania.</span><span class="sxs-lookup"><span data-stu-id="2ea55-121">Specifies the job to get.</span></span>
<span data-ttu-id="2ea55-122">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="2ea55-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="2ea55-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="2ea55-123">-JobId</span></span>

<span data-ttu-id="2ea55-124">Określa identyfikator zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2ea55-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="2ea55-125">Identyfikator jest właściwością JobId obiektu **Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="2ea55-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="2ea55-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2ea55-126">-VaultId</span></span>

<span data-ttu-id="2ea55-127">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2ea55-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2ea55-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea55-128">CommonParameters</span></span>
<span data-ttu-id="2ea55-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea55-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea55-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ea55-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea55-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ea55-131">INPUTS</span></span>

### <span data-ttu-id="2ea55-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ea55-132">System.String</span></span>

## <span data-ttu-id="2ea55-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ea55-133">OUTPUTS</span></span>

### <span data-ttu-id="2ea55-134">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="2ea55-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2ea55-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ea55-135">NOTES</span></span>

## <span data-ttu-id="2ea55-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ea55-136">RELATED LINKS</span></span>

[<span data-ttu-id="2ea55-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="2ea55-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
