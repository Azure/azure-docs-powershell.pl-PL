---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 80fbb17d31c37dafd4ba16b059c1dda5a987bea4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872591"
---
# <span data-ttu-id="89c64-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="89c64-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="89c64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89c64-102">SYNOPSIS</span></span>
<span data-ttu-id="89c64-103">Anuluje uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="89c64-103">Cancels a running job.</span></span>

## <span data-ttu-id="89c64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89c64-104">SYNTAX</span></span>

### <span data-ttu-id="89c64-105">JobFilterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="89c64-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c64-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="89c64-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89c64-107">Opis</span><span class="sxs-lookup"><span data-stu-id="89c64-107">DESCRIPTION</span></span>
<span data-ttu-id="89c64-108">Polecenie cmdlet **stop-AzRecoveryServicesBackupJob** anuluje istniejące zadanie kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="89c64-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="89c64-109">Za pomocą tego polecenia cmdlet można zatrzymać zadanie, które trwa zbyt długo i blokuje inne działania.</span><span class="sxs-lookup"><span data-stu-id="89c64-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="89c64-110">Możesz anulować tylko typy zadań tworzenie kopii zapasowej i przywracanie.</span><span class="sxs-lookup"><span data-stu-id="89c64-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="89c64-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="89c64-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="89c64-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89c64-112">EXAMPLES</span></span>

### <span data-ttu-id="89c64-113">Przykład 1: zatrzymanie zadania kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="89c64-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="89c64-114">Pierwsze polecenie pobiera zadanie kopii zapasowej, a następnie zapisuje zadanie w zmiennej $Job.</span><span class="sxs-lookup"><span data-stu-id="89c64-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="89c64-115">Ostatnie polecenie zatrzymuje zadanie, określając identyfikator wystąpienia zadania kopii zapasowej w $Job.</span><span class="sxs-lookup"><span data-stu-id="89c64-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="89c64-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89c64-116">PARAMETERS</span></span>

### <span data-ttu-id="89c64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c64-117">-DefaultProfile</span></span>
<span data-ttu-id="89c64-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89c64-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89c64-119">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="89c64-119">-Job</span></span>
<span data-ttu-id="89c64-120">Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89c64-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="89c64-121">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="89c64-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="89c64-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="89c64-122">-JobId</span></span>
<span data-ttu-id="89c64-123">Określa identyfikator zadania, które ma zostać anulowane.</span><span class="sxs-lookup"><span data-stu-id="89c64-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="89c64-124">Identyfikator jest właściwością InstanceId obiektu **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="89c64-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="89c64-125">Aby uzyskać obiekt **BackupJob** , użyj polecenie Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="89c64-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="89c64-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="89c64-126">-VaultId</span></span>
<span data-ttu-id="89c64-127">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="89c64-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="89c64-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89c64-128">-Confirm</span></span>
<span data-ttu-id="89c64-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89c64-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89c64-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89c64-130">-WhatIf</span></span>
<span data-ttu-id="89c64-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89c64-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89c64-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89c64-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89c64-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c64-133">CommonParameters</span></span>
<span data-ttu-id="89c64-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89c64-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c64-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89c64-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c64-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89c64-136">INPUTS</span></span>

### <span data-ttu-id="89c64-137">System. String</span><span class="sxs-lookup"><span data-stu-id="89c64-137">System.String</span></span>

## <span data-ttu-id="89c64-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89c64-138">OUTPUTS</span></span>

### <span data-ttu-id="89c64-139">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="89c64-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="89c64-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89c64-140">NOTES</span></span>

## <span data-ttu-id="89c64-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89c64-141">RELATED LINKS</span></span>

[<span data-ttu-id="89c64-142">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="89c64-142">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="89c64-143">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="89c64-143">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


