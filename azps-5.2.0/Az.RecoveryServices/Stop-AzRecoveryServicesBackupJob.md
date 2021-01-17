---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 41234c91d5c833f15a4914d2af2de93c9c5bf288
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331717"
---
# <span data-ttu-id="76677-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="76677-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="76677-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76677-102">SYNOPSIS</span></span>
<span data-ttu-id="76677-103">Anuluje uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="76677-103">Cancels a running job.</span></span>

## <span data-ttu-id="76677-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76677-104">SYNTAX</span></span>

### <span data-ttu-id="76677-105">JobFilterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="76677-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76677-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="76677-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76677-107">Opis</span><span class="sxs-lookup"><span data-stu-id="76677-107">DESCRIPTION</span></span>
<span data-ttu-id="76677-108">Polecenie cmdlet **stop-AzRecoveryServicesBackupJob** anuluje istniejące zadanie kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="76677-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="76677-109">Za pomocą tego polecenia cmdlet można zatrzymać zadanie, które trwa zbyt długo i blokuje inne działania.</span><span class="sxs-lookup"><span data-stu-id="76677-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="76677-110">Możesz anulować tylko typy zadań tworzenie kopii zapasowej i przywracanie.</span><span class="sxs-lookup"><span data-stu-id="76677-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="76677-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="76677-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="76677-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76677-112">EXAMPLES</span></span>

### <span data-ttu-id="76677-113">Przykład 1: zatrzymanie zadania kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="76677-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="76677-114">Pierwsze polecenie pobiera zadanie kopii zapasowej, a następnie zapisuje zadanie w zmiennej $Job.</span><span class="sxs-lookup"><span data-stu-id="76677-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="76677-115">Ostatnie polecenie zatrzymuje zadanie, określając identyfikator wystąpienia zadania kopii zapasowej w $Job.</span><span class="sxs-lookup"><span data-stu-id="76677-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="76677-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76677-116">PARAMETERS</span></span>

### <span data-ttu-id="76677-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76677-117">-DefaultProfile</span></span>
<span data-ttu-id="76677-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76677-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76677-119">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="76677-119">-Job</span></span>
<span data-ttu-id="76677-120">Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76677-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="76677-121">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="76677-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="76677-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="76677-122">-JobId</span></span>
<span data-ttu-id="76677-123">Określa identyfikator zadania, które ma zostać anulowane.</span><span class="sxs-lookup"><span data-stu-id="76677-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="76677-124">Identyfikator jest właściwością InstanceId obiektu **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="76677-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="76677-125">Aby uzyskać obiekt **BackupJob** , użyj polecenie Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="76677-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="76677-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="76677-126">-VaultId</span></span>
<span data-ttu-id="76677-127">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="76677-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="76677-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76677-128">-Confirm</span></span>
<span data-ttu-id="76677-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76677-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76677-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76677-130">-WhatIf</span></span>
<span data-ttu-id="76677-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76677-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="76677-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76677-132">CommonParameters</span></span>
<span data-ttu-id="76677-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76677-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76677-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76677-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76677-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76677-135">INPUTS</span></span>

### <span data-ttu-id="76677-136">System. String</span><span class="sxs-lookup"><span data-stu-id="76677-136">System.String</span></span>

## <span data-ttu-id="76677-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76677-137">OUTPUTS</span></span>

### <span data-ttu-id="76677-138">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="76677-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="76677-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76677-139">NOTES</span></span>

## <span data-ttu-id="76677-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76677-140">RELATED LINKS</span></span>

[<span data-ttu-id="76677-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="76677-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="76677-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="76677-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


