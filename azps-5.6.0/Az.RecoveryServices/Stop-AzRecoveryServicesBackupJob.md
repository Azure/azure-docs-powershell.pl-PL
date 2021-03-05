---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 0eaabc025a9252cdd48500f294fab699e7ebea1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000954"
---
# <span data-ttu-id="a60a6-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a60a6-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="a60a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a60a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a60a6-103">Anulowanie zadania uruchomionego.</span><span class="sxs-lookup"><span data-stu-id="a60a6-103">Cancels a running job.</span></span>

## <span data-ttu-id="a60a6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a60a6-104">SYNTAX</span></span>

### <span data-ttu-id="a60a6-105">JobFilterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a60a6-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a60a6-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="a60a6-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a60a6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a60a6-107">DESCRIPTION</span></span>
<span data-ttu-id="a60a6-108">Polecenie **cmdlet Stop-AzRecoveryServicesBackupJob** anuluje istniejące zadanie kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a60a6-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="a60a6-109">To polecenie cmdlet pozwala zatrzymać zadanie, które trwa zbyt długo, i blokuje inne działania.</span><span class="sxs-lookup"><span data-stu-id="a60a6-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="a60a6-110">Można anulować tylko zadania typu Kopia zapasowa i Przywracanie.</span><span class="sxs-lookup"><span data-stu-id="a60a6-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="a60a6-111">Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60a6-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a60a6-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a60a6-112">EXAMPLES</span></span>

### <span data-ttu-id="a60a6-113">Przykład 1. Zatrzymywanie zadania kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="a60a6-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="a60a6-114">Pierwsze polecenie pobiera zadanie kopii zapasowej, a następnie przechowuje je w $Job danych.</span><span class="sxs-lookup"><span data-stu-id="a60a6-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="a60a6-115">Ostatnie polecenie zatrzymuje zadanie, określając identyfikator wystąpienia zadania kopii zapasowej w $Job.</span><span class="sxs-lookup"><span data-stu-id="a60a6-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="a60a6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a60a6-116">PARAMETERS</span></span>

### <span data-ttu-id="a60a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60a6-117">-DefaultProfile</span></span>
<span data-ttu-id="a60a6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a60a6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a60a6-119">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="a60a6-119">-Job</span></span>
<span data-ttu-id="a60a6-120">Określa zadanie, które to polecenie cmdlet anuluje.</span><span class="sxs-lookup"><span data-stu-id="a60a6-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="a60a6-121">Aby uzyskać obiekt **BackupJob,** użyj Get-AzRecoveryServicesBackupJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60a6-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="a60a6-122">- JobId</span><span class="sxs-lookup"><span data-stu-id="a60a6-122">-JobId</span></span>
<span data-ttu-id="a60a6-123">Określa identyfikator zadania do anulowania.</span><span class="sxs-lookup"><span data-stu-id="a60a6-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="a60a6-124">Identyfikator jest właściwością InstanceId obiektu **BackupJob.**</span><span class="sxs-lookup"><span data-stu-id="a60a6-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="a60a6-125">Aby uzyskać obiekt **BackupJob,** użyj funkcji Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="a60a6-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="a60a6-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a60a6-126">-VaultId</span></span>
<span data-ttu-id="a60a6-127">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a60a6-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a60a6-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a60a6-128">-Confirm</span></span>
<span data-ttu-id="a60a6-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a60a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a60a6-130">-WhatIf</span></span>
<span data-ttu-id="a60a6-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60a6-131">Shows what would happen if the cmdlet runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60a6-132">CommonParameters</span></span>
<span data-ttu-id="a60a6-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60a6-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a60a6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60a6-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a60a6-135">INPUTS</span></span>

### <span data-ttu-id="a60a6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a60a6-136">System.String</span></span>

## <span data-ttu-id="a60a6-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a60a6-137">OUTPUTS</span></span>

### <span data-ttu-id="a60a6-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="a60a6-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a60a6-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a60a6-139">NOTES</span></span>

## <span data-ttu-id="a60a6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a60a6-140">RELATED LINKS</span></span>

[<span data-ttu-id="a60a6-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a60a6-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="a60a6-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a60a6-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


