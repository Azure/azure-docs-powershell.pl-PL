---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: df52a9b690060903affa666d66bfbd2a3afb7aea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526641"
---
# <span data-ttu-id="13702-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="13702-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="13702-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13702-102">SYNOPSIS</span></span>
<span data-ttu-id="13702-103">Rozpoczynanie planowanej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="13702-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13702-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13702-104">SYNTAX</span></span>

### <span data-ttu-id="13702-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13702-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13702-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="13702-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13702-107">Opis</span><span class="sxs-lookup"><span data-stu-id="13702-107">DESCRIPTION</span></span>
<span data-ttu-id="13702-108">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** rozpoczyna planowaną pracę w trybie failover dla elementu chronionego replikacji odzyskiwania witryny platformy Azure lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="13702-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="13702-109">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13702-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="13702-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13702-110">EXAMPLES</span></span>

### <span data-ttu-id="13702-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13702-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="13702-112">Rozpoczyna planowaną pracę w trybie failover dla określonego planu odzyskiwania ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="13702-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="13702-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13702-113">PARAMETERS</span></span>

### <span data-ttu-id="13702-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13702-114">-Confirm</span></span>
<span data-ttu-id="13702-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13702-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13702-116">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="13702-116">-CreateVmIfNotFound</span></span>
<span data-ttu-id="13702-117">Utwórz maszynę wirtualną, jeśli nie można jej odnaleźć podczas awarii do regionu podstawowego (używanej w alternatywnym odzyskiwaniu lokalizacji). Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="13702-117">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13702-118">Tak/nie1</span><span class="sxs-lookup"><span data-stu-id="13702-118">Yes</span></span>
- <span data-ttu-id="13702-119">Ma</span><span class="sxs-lookup"><span data-stu-id="13702-119">No</span></span>

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

### <span data-ttu-id="13702-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="13702-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="13702-121">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="13702-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="13702-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="13702-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="13702-123">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="13702-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="13702-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13702-124">-DefaultProfile</span></span>
<span data-ttu-id="13702-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13702-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13702-126">-Direction</span><span class="sxs-lookup"><span data-stu-id="13702-126">-Direction</span></span>
<span data-ttu-id="13702-127">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="13702-127">Specifies the direction of the failover.</span></span>
<span data-ttu-id="13702-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="13702-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13702-129">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="13702-129">PrimaryToRecovery</span></span>
- <span data-ttu-id="13702-130">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="13702-130">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="13702-131">— Optymalizuj</span><span class="sxs-lookup"><span data-stu-id="13702-131">-Optimize</span></span>
<span data-ttu-id="13702-132">Określa, do czego należy zoptymalizować.</span><span class="sxs-lookup"><span data-stu-id="13702-132">Specifies what to optimize for.</span></span>
<span data-ttu-id="13702-133">Ten parametr jest stosowany, gdy praca awaryjna została wykonana z witryny platformy Azure do witryny lokalnej, która wymaga znacznej synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="13702-133">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="13702-134">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="13702-134">Valid values are:</span></span>

- <span data-ttu-id="13702-135">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="13702-135">ForDowntime</span></span>
- <span data-ttu-id="13702-136">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="13702-136">ForSynchronization</span></span>

<span data-ttu-id="13702-137">Gdy jest określony **ForDowntime** , oznacza to, że dane są synchronizowane przed przejściem w tryb pracy awaryjnej w celu zminimalizowania przestojów.</span><span class="sxs-lookup"><span data-stu-id="13702-137">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="13702-138">Synchronizacja jest przeprowadzana bez zamykania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="13702-138">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="13702-139">Po zakończeniu synchronizacji zadanie zostaje zawieszone.</span><span class="sxs-lookup"><span data-stu-id="13702-139">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="13702-140">Wznów zadanie, aby wykonać dodatkową operację synchronizacji, która zamyka maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="13702-140">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="13702-141">Gdy jest określony **ForSynchronization** , oznacza to, że dane są synchronizowane podczas pracy awaryjnej tylko wtedy, gdy synchronizacja danych jest zminimalizowana.</span><span class="sxs-lookup"><span data-stu-id="13702-141">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="13702-142">Jeśli to ustawienie jest włączone, maszyna wirtualna zostanie natychmiast ZAMKNIĘTA.</span><span class="sxs-lookup"><span data-stu-id="13702-142">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="13702-143">Synchronizacja rozpoczyna się po zamknięciu, aby ukończyć operację przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="13702-143">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="13702-144">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="13702-144">-RecoveryPlan</span></span>
<span data-ttu-id="13702-145">Określa, że obiekt planu odzyskiwania ASR odpowiada planowi odzyskiwania, który ma zostać zakończony awaryjnie.</span><span class="sxs-lookup"><span data-stu-id="13702-145">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="13702-146">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="13702-146">-ReplicationProtectedItem</span></span>
<span data-ttu-id="13702-147">Określa obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionej replikacji w celu jego przemyślnego przekroczenia.</span><span class="sxs-lookup"><span data-stu-id="13702-147">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="13702-148">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="13702-148">-ServicesProvider</span></span>
<span data-ttu-id="13702-149">Umożliwia zidentyfikowanie hosta, na którym ma zostać utworzona maszyna wirtualna, podczas nieprawidłowej lokalizacji do alternatywnej lokalizacji przez określenie obiektu dostawcy usług ASR odpowiadającego dostawcy usług ASR uruchomionemu na hoście.</span><span class="sxs-lookup"><span data-stu-id="13702-149">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="13702-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13702-150">-WhatIf</span></span>
<span data-ttu-id="13702-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13702-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13702-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13702-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13702-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13702-153">CommonParameters</span></span>
<span data-ttu-id="13702-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13702-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13702-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13702-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13702-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13702-156">INPUTS</span></span>

### <span data-ttu-id="13702-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="13702-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="13702-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="13702-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="13702-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13702-159">OUTPUTS</span></span>

### <span data-ttu-id="13702-160">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="13702-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="13702-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13702-161">NOTES</span></span>

## <span data-ttu-id="13702-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13702-162">RELATED LINKS</span></span>
