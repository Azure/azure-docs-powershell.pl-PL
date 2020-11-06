---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e96a57a00d6314015d1d13f4f540d3f763c96c23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543059"
---
# <span data-ttu-id="64c91-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="64c91-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="64c91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64c91-102">SYNOPSIS</span></span>
<span data-ttu-id="64c91-103">Rozpoczynanie planowanej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="64c91-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64c91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64c91-104">SYNTAX</span></span>

### <span data-ttu-id="64c91-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="64c91-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64c91-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="64c91-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64c91-107">Opis</span><span class="sxs-lookup"><span data-stu-id="64c91-107">DESCRIPTION</span></span>
<span data-ttu-id="64c91-108">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** rozpoczyna planowaną pracę w trybie failover dla elementu chronionego replikacji odzyskiwania witryny platformy Azure lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="64c91-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="64c91-109">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64c91-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="64c91-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64c91-110">EXAMPLES</span></span>

### <span data-ttu-id="64c91-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64c91-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="64c91-112">Rozpoczyna planowaną pracę w trybie failover dla określonego planu odzyskiwania ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="64c91-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="64c91-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64c91-113">PARAMETERS</span></span>

### <span data-ttu-id="64c91-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="64c91-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="64c91-115">Utwórz maszynę wirtualną, jeśli nie można jej odnaleźć podczas awarii do regionu podstawowego (używanej w alternatywnym odzyskiwaniu lokalizacji). Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="64c91-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64c91-116">Tak/nie1</span><span class="sxs-lookup"><span data-stu-id="64c91-116">Yes</span></span>
- <span data-ttu-id="64c91-117">Ma</span><span class="sxs-lookup"><span data-stu-id="64c91-117">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c91-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="64c91-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="64c91-119">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="64c91-119">Specifies the primary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c91-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="64c91-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="64c91-121">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="64c91-121">Specifies the secondary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c91-122">-Direction</span><span class="sxs-lookup"><span data-stu-id="64c91-122">-Direction</span></span>
<span data-ttu-id="64c91-123">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="64c91-123">Specifies the direction of the failover.</span></span>
<span data-ttu-id="64c91-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="64c91-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64c91-125">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="64c91-125">PrimaryToRecovery</span></span>
- <span data-ttu-id="64c91-126">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="64c91-126">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c91-127">— Optymalizuj</span><span class="sxs-lookup"><span data-stu-id="64c91-127">-Optimize</span></span>
<span data-ttu-id="64c91-128">Określa, do czego należy zoptymalizować.</span><span class="sxs-lookup"><span data-stu-id="64c91-128">Specifies what to optimize for.</span></span>
<span data-ttu-id="64c91-129">Ten parametr jest stosowany, gdy praca awaryjna została wykonana z witryny platformy Azure do witryny lokalnej, która wymaga znacznej synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="64c91-129">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="64c91-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="64c91-130">Valid values are:</span></span>

- <span data-ttu-id="64c91-131">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="64c91-131">ForDowntime</span></span>
- <span data-ttu-id="64c91-132">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="64c91-132">ForSynchronization</span></span>

<span data-ttu-id="64c91-133">Gdy jest określony **ForDowntime** , oznacza to, że dane są synchronizowane przed przejściem w tryb pracy awaryjnej w celu zminimalizowania przestojów.</span><span class="sxs-lookup"><span data-stu-id="64c91-133">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="64c91-134">Synchronizacja jest przeprowadzana bez zamykania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64c91-134">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="64c91-135">Po zakończeniu synchronizacji zadanie zostaje zawieszone.</span><span class="sxs-lookup"><span data-stu-id="64c91-135">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="64c91-136">Wznów zadanie, aby wykonać dodatkową operację synchronizacji, która zamyka maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="64c91-136">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="64c91-137">Gdy jest określony **ForSynchronization** , oznacza to, że dane są synchronizowane podczas pracy awaryjnej tylko wtedy, gdy synchronizacja danych jest zminimalizowana.</span><span class="sxs-lookup"><span data-stu-id="64c91-137">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="64c91-138">Jeśli to ustawienie jest włączone, maszyna wirtualna zostanie natychmiast ZAMKNIĘTA.</span><span class="sxs-lookup"><span data-stu-id="64c91-138">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="64c91-139">Synchronizacja rozpoczyna się po zamknięciu, aby ukończyć operację przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="64c91-139">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c91-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64c91-140">-RecoveryPlan</span></span>
<span data-ttu-id="64c91-141">Określa, że obiekt planu odzyskiwania ASR odpowiada planowi odzyskiwania, który ma zostać zakończony awaryjnie.</span><span class="sxs-lookup"><span data-stu-id="64c91-141">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c91-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64c91-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="64c91-143">Określa obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionej replikacji w celu jego przemyślnego przekroczenia.</span><span class="sxs-lookup"><span data-stu-id="64c91-143">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c91-144">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="64c91-144">-ServicesProvider</span></span>
<span data-ttu-id="64c91-145">Umożliwia zidentyfikowanie hosta, na którym ma zostać utworzona maszyna wirtualna, podczas nieprawidłowej lokalizacji do alternatywnej lokalizacji przez określenie obiektu dostawcy usług ASR odpowiadającego dostawcy usług ASR uruchomionemu na hoście.</span><span class="sxs-lookup"><span data-stu-id="64c91-145">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span> 

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c91-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64c91-146">-Confirm</span></span>
<span data-ttu-id="64c91-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64c91-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c91-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64c91-148">-WhatIf</span></span>
<span data-ttu-id="64c91-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64c91-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64c91-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64c91-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c91-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c91-151">CommonParameters</span></span>
<span data-ttu-id="64c91-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c91-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c91-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c91-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c91-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64c91-154">INPUTS</span></span>

### <span data-ttu-id="64c91-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="64c91-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="64c91-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64c91-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="64c91-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64c91-157">OUTPUTS</span></span>

### <span data-ttu-id="64c91-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="64c91-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="64c91-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64c91-159">NOTES</span></span>

## <span data-ttu-id="64c91-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64c91-160">RELATED LINKS</span></span>

