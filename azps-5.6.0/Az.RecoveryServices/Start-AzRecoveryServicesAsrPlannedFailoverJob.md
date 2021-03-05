---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: 78aa310d6fd3cdb7a27de066e234744b3e450520
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000961"
---
# <span data-ttu-id="e3538-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e3538-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="e3538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3538-102">SYNOPSIS</span></span>
<span data-ttu-id="e3538-103">Rozpoczyna planowaną operację trybu failover.</span><span class="sxs-lookup"><span data-stu-id="e3538-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="e3538-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e3538-104">SYNTAX</span></span>

### <span data-ttu-id="e3538-105">ByRPIObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e3538-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3538-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e3538-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3538-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e3538-107">DESCRIPTION</span></span>
<span data-ttu-id="e3538-108">Polecenie cmdlet **Start-AzRecoveryServicesAsrPlannedFailoverJob** uruchamia planowane trybu failover dla elementu chronionego replikacją usługi Azure Site Recovery lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e3538-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="e3538-109">Możesz sprawdzić, czy zadanie zakończy się powodzeniem, używając Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3538-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="e3538-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e3538-110">EXAMPLES</span></span>

### <span data-ttu-id="e3538-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3538-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="e3538-112">Rozpoczyna planowane trybu failover dla określonego planu odzyskiwania asr i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="e3538-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e3538-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3538-113">PARAMETERS</span></span>

### <span data-ttu-id="e3538-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="e3538-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="e3538-115">Utwórz maszynę wirtualną, jeśli nie zostanie znaleziona w przypadku powrotu do regionu podstawowego (używanego w alternatywnym odzyskiwaniu lokalizacji). Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e3538-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3538-116">Tak</span><span class="sxs-lookup"><span data-stu-id="e3538-116">Yes</span></span>
- <span data-ttu-id="e3538-117">Nie</span><span class="sxs-lookup"><span data-stu-id="e3538-117">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e3538-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="e3538-119">Określa plik certyfikatu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="e3538-119">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e3538-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="e3538-121">Określa plik certyfikatu pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="e3538-121">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3538-122">-DefaultProfile</span></span>
<span data-ttu-id="e3538-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3538-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e3538-124">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="e3538-124">-Direction</span></span>
<span data-ttu-id="e3538-125">Określa kierunek trybu failover.</span><span class="sxs-lookup"><span data-stu-id="e3538-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="e3538-126">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e3538-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3538-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e3538-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="e3538-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e3538-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-129">— Optymalizowanie</span><span class="sxs-lookup"><span data-stu-id="e3538-129">-Optimize</span></span>
<span data-ttu-id="e3538-130">Określa, pod kątem czego ma być optymalizowana.</span><span class="sxs-lookup"><span data-stu-id="e3538-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="e3538-131">Ten parametr ma zastosowanie, gdy trybu failover jest wykonywane z witryny platformy Azure do witryny lokalnej, co wymaga istotnej synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="e3538-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="e3538-132">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="e3538-132">Valid values are:</span></span>

- <span data-ttu-id="e3538-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="e3538-133">ForDowntime</span></span>
- <span data-ttu-id="e3538-134">Synchronizacja</span><span class="sxs-lookup"><span data-stu-id="e3538-134">ForSynchronization</span></span>

<span data-ttu-id="e3538-135">Jeśli **określono forDowntime,** oznacza to, że dane są synchronizowane przed trybu failover w celu zminimalizowania przestojów.</span><span class="sxs-lookup"><span data-stu-id="e3538-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="e3538-136">Synchronizacja jest wykonywana bez zamykania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e3538-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="e3538-137">Po zakończeniu synchronizacji zadanie zostaje zawieszone.</span><span class="sxs-lookup"><span data-stu-id="e3538-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="e3538-138">Wznów zadanie, aby wykonać dodatkową operację synchronizacji, która zamyka maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="e3538-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="e3538-139">Jeśli **jest określona synchronizacja,** oznacza to, że dane są synchronizowane tylko w trybie failover, więc synchronizacja danych jest zminimalizowana.</span><span class="sxs-lookup"><span data-stu-id="e3538-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="e3538-140">Gdy to ustawienie jest włączone, maszynę wirtualną należy natychmiast zamknąć.</span><span class="sxs-lookup"><span data-stu-id="e3538-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="e3538-141">Synchronizacja rozpoczyna się po zamknięciu systemu w celu ukończenia operacji trybu failover.</span><span class="sxs-lookup"><span data-stu-id="e3538-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e3538-142">-RecoveryPlan</span></span>
<span data-ttu-id="e3538-143">Określa obiekt planu odzyskiwania po stronie asr, który odpowiada planowi odzyskiwania, który ma zostać aawarii.</span><span class="sxs-lookup"><span data-stu-id="e3538-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e3538-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e3538-145">Określa obiekt elementu chronionego przez asr replikacji odpowiadający elementowi chronionego replikacją, który ma zostać aawarii.</span><span class="sxs-lookup"><span data-stu-id="e3538-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e3538-146">-ServicesProvider</span></span>
<span data-ttu-id="e3538-147">Identyfikuje hosta, na którym ma być tworzyć maszyny wirtualne podczas pracy w awarii do lokalizacji alternatywnej, określając obiekt dostawcy usług ASR odpowiadający dostawcy usług ASR uruchomionego na hoście.</span><span class="sxs-lookup"><span data-stu-id="e3538-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3538-148">-Confirm</span></span>
<span data-ttu-id="e3538-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e3538-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3538-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3538-150">-WhatIf</span></span>
<span data-ttu-id="e3538-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3538-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3538-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e3538-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3538-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3538-153">CommonParameters</span></span>
<span data-ttu-id="e3538-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3538-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3538-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3538-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3538-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3538-156">INPUTS</span></span>

### <span data-ttu-id="e3538-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e3538-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="e3538-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e3538-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e3538-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3538-159">OUTPUTS</span></span>

### <span data-ttu-id="e3538-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="e3538-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e3538-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e3538-161">NOTES</span></span>

## <span data-ttu-id="e3538-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3538-162">RELATED LINKS</span></span>
