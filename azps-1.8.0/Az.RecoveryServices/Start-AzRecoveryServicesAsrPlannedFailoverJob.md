---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: ee39fdfcb40c394bfbd7f1d804d8d9785a63f7c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708566"
---
# <span data-ttu-id="5d04b-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="5d04b-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="5d04b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d04b-102">SYNOPSIS</span></span>
<span data-ttu-id="5d04b-103">Rozpoczynanie planowanej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="5d04b-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="5d04b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d04b-104">SYNTAX</span></span>

### <span data-ttu-id="5d04b-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d04b-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d04b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5d04b-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d04b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5d04b-107">DESCRIPTION</span></span>
<span data-ttu-id="5d04b-108">Polecenie cmdlet **Start-AzRecoveryServicesAsrPlannedFailoverJob** rozpoczyna planowaną pracę w trybie failover dla elementu chronionego replikacji odzyskiwania witryny platformy Azure lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5d04b-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="5d04b-109">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d04b-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="5d04b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d04b-110">EXAMPLES</span></span>

### <span data-ttu-id="5d04b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d04b-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="5d04b-112">Rozpoczyna planowaną pracę w trybie failover dla określonego planu odzyskiwania ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="5d04b-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5d04b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d04b-113">PARAMETERS</span></span>

### <span data-ttu-id="5d04b-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="5d04b-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="5d04b-115">Utwórz maszynę wirtualną, jeśli nie można jej odnaleźć podczas awarii do regionu podstawowego (używanej w alternatywnym odzyskiwaniu lokalizacji). Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5d04b-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5d04b-116">Tak/nie1</span><span class="sxs-lookup"><span data-stu-id="5d04b-116">Yes</span></span>
- <span data-ttu-id="5d04b-117">Ma</span><span class="sxs-lookup"><span data-stu-id="5d04b-117">No</span></span>

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

### <span data-ttu-id="5d04b-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="5d04b-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="5d04b-119">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5d04b-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="5d04b-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="5d04b-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="5d04b-121">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5d04b-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="5d04b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d04b-122">-DefaultProfile</span></span>
<span data-ttu-id="5d04b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d04b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5d04b-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="5d04b-124">-Direction</span></span>
<span data-ttu-id="5d04b-125">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="5d04b-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="5d04b-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5d04b-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5d04b-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="5d04b-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="5d04b-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="5d04b-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="5d04b-129">— Optymalizuj</span><span class="sxs-lookup"><span data-stu-id="5d04b-129">-Optimize</span></span>
<span data-ttu-id="5d04b-130">Określa, do czego należy zoptymalizować.</span><span class="sxs-lookup"><span data-stu-id="5d04b-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="5d04b-131">Ten parametr jest stosowany, gdy praca awaryjna została wykonana z witryny platformy Azure do witryny lokalnej, która wymaga znacznej synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="5d04b-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="5d04b-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="5d04b-132">Valid values are:</span></span>

- <span data-ttu-id="5d04b-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="5d04b-133">ForDowntime</span></span>
- <span data-ttu-id="5d04b-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="5d04b-134">ForSynchronization</span></span>

<span data-ttu-id="5d04b-135">Gdy jest określony **ForDowntime** , oznacza to, że dane są synchronizowane przed przejściem w tryb pracy awaryjnej w celu zminimalizowania przestojów.</span><span class="sxs-lookup"><span data-stu-id="5d04b-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="5d04b-136">Synchronizacja jest przeprowadzana bez zamykania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5d04b-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="5d04b-137">Po zakończeniu synchronizacji zadanie zostaje zawieszone.</span><span class="sxs-lookup"><span data-stu-id="5d04b-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="5d04b-138">Wznów zadanie, aby wykonać dodatkową operację synchronizacji, która zamyka maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="5d04b-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="5d04b-139">Gdy jest określony **ForSynchronization** , oznacza to, że dane są synchronizowane podczas pracy awaryjnej tylko wtedy, gdy synchronizacja danych jest zminimalizowana.</span><span class="sxs-lookup"><span data-stu-id="5d04b-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="5d04b-140">Jeśli to ustawienie jest włączone, maszyna wirtualna zostanie natychmiast ZAMKNIĘTA.</span><span class="sxs-lookup"><span data-stu-id="5d04b-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="5d04b-141">Synchronizacja rozpoczyna się po zamknięciu, aby ukończyć operację przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="5d04b-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="5d04b-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5d04b-142">-RecoveryPlan</span></span>
<span data-ttu-id="5d04b-143">Określa, że obiekt planu odzyskiwania ASR odpowiada planowi odzyskiwania, który ma zostać zakończony awaryjnie.</span><span class="sxs-lookup"><span data-stu-id="5d04b-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="5d04b-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5d04b-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5d04b-145">Określa obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionej replikacji w celu jego przemyślnego przekroczenia.</span><span class="sxs-lookup"><span data-stu-id="5d04b-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="5d04b-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5d04b-146">-ServicesProvider</span></span>
<span data-ttu-id="5d04b-147">Umożliwia zidentyfikowanie hosta, na którym ma zostać utworzona maszyna wirtualna, podczas nieprawidłowej lokalizacji do alternatywnej lokalizacji przez określenie obiektu dostawcy usług ASR odpowiadającego dostawcy usług ASR uruchomionemu na hoście.</span><span class="sxs-lookup"><span data-stu-id="5d04b-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="5d04b-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d04b-148">-Confirm</span></span>
<span data-ttu-id="5d04b-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d04b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d04b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d04b-150">-WhatIf</span></span>
<span data-ttu-id="5d04b-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d04b-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d04b-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d04b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d04b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d04b-153">CommonParameters</span></span>
<span data-ttu-id="5d04b-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d04b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d04b-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d04b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d04b-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d04b-156">INPUTS</span></span>

### <span data-ttu-id="5d04b-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5d04b-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="5d04b-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5d04b-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5d04b-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d04b-159">OUTPUTS</span></span>

### <span data-ttu-id="5d04b-160">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5d04b-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5d04b-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d04b-161">NOTES</span></span>

## <span data-ttu-id="5d04b-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d04b-162">RELATED LINKS</span></span>
