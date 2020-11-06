---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/stop-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 8368e875a8657da1d8934980832ac950b6424cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541571"
---
# <span data-ttu-id="558b5-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="558b5-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="558b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="558b5-102">SYNOPSIS</span></span>
<span data-ttu-id="558b5-103">Anuluje uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="558b5-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="558b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="558b5-104">SYNTAX</span></span>

### <span data-ttu-id="558b5-105">JobFilterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="558b5-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="558b5-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="558b5-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="558b5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="558b5-107">DESCRIPTION</span></span>
<span data-ttu-id="558b5-108">Polecenie cmdlet **stop-AzureRmRecoveryServicesBackupJob** anuluje istniejące zadanie kopii zapasowej Azure.</span><span class="sxs-lookup"><span data-stu-id="558b5-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="558b5-109">Za pomocą tego polecenia cmdlet można zatrzymać zadanie, które trwa zbyt długo i blokuje inne działania.</span><span class="sxs-lookup"><span data-stu-id="558b5-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="558b5-110">Możesz anulować tylko typy zadań tworzenie kopii zapasowej i przywracanie.</span><span class="sxs-lookup"><span data-stu-id="558b5-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="558b5-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="558b5-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="558b5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="558b5-112">EXAMPLES</span></span>

### <span data-ttu-id="558b5-113">Przykład 1: zatrzymanie zadania kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="558b5-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="558b5-114">Pierwsze polecenie pobiera zadanie kopii zapasowej, a następnie zapisuje zadanie w zmiennej $Job.</span><span class="sxs-lookup"><span data-stu-id="558b5-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="558b5-115">Ostatnie polecenie zatrzymuje zadanie, określając identyfikator wystąpienia zadania kopii zapasowej w $Job.</span><span class="sxs-lookup"><span data-stu-id="558b5-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="558b5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="558b5-116">PARAMETERS</span></span>

### <span data-ttu-id="558b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="558b5-117">-DefaultProfile</span></span>
<span data-ttu-id="558b5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="558b5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="558b5-119">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="558b5-119">-Job</span></span>
<span data-ttu-id="558b5-120">Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="558b5-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="558b5-121">Aby uzyskać obiekt **BackupJob** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="558b5-121">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="558b5-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="558b5-122">-JobId</span></span>
<span data-ttu-id="558b5-123">Określa identyfikator zadania, które ma zostać anulowane.</span><span class="sxs-lookup"><span data-stu-id="558b5-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="558b5-124">Identyfikator jest właściwością InstanceId obiektu **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="558b5-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="558b5-125">Aby uzyskać obiekt **BackupJob** , użyj polecenie Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="558b5-125">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="558b5-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="558b5-126">-VaultId</span></span>
<span data-ttu-id="558b5-127">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="558b5-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="558b5-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="558b5-128">-Confirm</span></span>
<span data-ttu-id="558b5-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="558b5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="558b5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="558b5-130">-WhatIf</span></span>
<span data-ttu-id="558b5-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="558b5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="558b5-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="558b5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="558b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="558b5-133">CommonParameters</span></span>
<span data-ttu-id="558b5-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="558b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="558b5-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="558b5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="558b5-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="558b5-136">INPUTS</span></span>

### <span data-ttu-id="558b5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="558b5-137">System.String</span></span>
<span data-ttu-id="558b5-138">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="558b5-138">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="558b5-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="558b5-139">OUTPUTS</span></span>

### <span data-ttu-id="558b5-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="558b5-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="558b5-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="558b5-141">NOTES</span></span>

## <span data-ttu-id="558b5-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="558b5-142">RELATED LINKS</span></span>

[<span data-ttu-id="558b5-143">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="558b5-143">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="558b5-144">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="558b5-144">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


