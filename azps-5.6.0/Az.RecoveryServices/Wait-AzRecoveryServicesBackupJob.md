---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: e0b3dc87ffdfc86f39f201b6384f38ce8ca1c70a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960145"
---
# <span data-ttu-id="157d4-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="157d4-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="157d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="157d4-102">SYNOPSIS</span></span>

<span data-ttu-id="157d4-103">Czeka na zakończenie zadania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="157d4-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="157d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="157d4-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="157d4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="157d4-105">DESCRIPTION</span></span>

<span data-ttu-id="157d4-106">Polecenie cmdlet **Wait-AzRecoveryServicesBackupJob** czeka na ukończenie zadania kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="157d4-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="157d4-107">Tworzenie zadań kopii zapasowej może zająć dużo czasu.</span><span class="sxs-lookup"><span data-stu-id="157d4-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="157d4-108">Jeśli zadanie kopii zapasowej zostanie uruchomione w ramach skryptu, może być konieczne wymusienie na skryptie czekania na ukończenie zadania przed kontynuowaniem wykonywania innych zadań.</span><span class="sxs-lookup"><span data-stu-id="157d4-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="157d4-109">Skrypt, który zawiera to polecenie cmdlet, może być prostszy niż skrypt, który ankietuje usługę kopii zapasowej na temat stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="157d4-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="157d4-110">Ustaw kontekst magazynu przy użyciu parametru -VaultId.</span><span class="sxs-lookup"><span data-stu-id="157d4-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="157d4-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="157d4-111">EXAMPLES</span></span>

### <span data-ttu-id="157d4-112">Przykład 1. Oczekiwanie na zakończenie zadania</span><span class="sxs-lookup"><span data-stu-id="157d4-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="157d4-113">Ten skrypt ankietuje pierwsze zadanie, które obecnie trwa do czasu jego ukończenia lub wygaśnięcia limitu czasu 1 godziny.</span><span class="sxs-lookup"><span data-stu-id="157d4-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="157d4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="157d4-114">PARAMETERS</span></span>

### <span data-ttu-id="157d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157d4-115">-DefaultProfile</span></span>

<span data-ttu-id="157d4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="157d4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="157d4-117">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="157d4-117">-Job</span></span>

<span data-ttu-id="157d4-118">Określa zadanie, na które należy poczekać.</span><span class="sxs-lookup"><span data-stu-id="157d4-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="157d4-119">Aby uzyskać obiekt **BackupJob,** użyj polecenia cmdlet **Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="157d4-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="157d4-120">— Limit czasu</span><span class="sxs-lookup"><span data-stu-id="157d4-120">-Timeout</span></span>

<span data-ttu-id="157d4-121">Określa maksymalny czas (w sekundach), przez który to polecenie cmdlet oczekuje na ukończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="157d4-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="157d4-122">Zalecane jest określenie wartości przec.</span><span class="sxs-lookup"><span data-stu-id="157d4-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157d4-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="157d4-123">-VaultId</span></span>

<span data-ttu-id="157d4-124">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="157d4-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="157d4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157d4-125">CommonParameters</span></span>
<span data-ttu-id="157d4-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="157d4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157d4-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="157d4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157d4-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="157d4-128">INPUTS</span></span>

### <span data-ttu-id="157d4-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="157d4-129">System.Object</span></span>

### <span data-ttu-id="157d4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="157d4-130">System.String</span></span>

## <span data-ttu-id="157d4-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="157d4-131">OUTPUTS</span></span>

### <span data-ttu-id="157d4-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="157d4-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="157d4-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="157d4-133">NOTES</span></span>

## <span data-ttu-id="157d4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="157d4-134">RELATED LINKS</span></span>

[<span data-ttu-id="157d4-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="157d4-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
