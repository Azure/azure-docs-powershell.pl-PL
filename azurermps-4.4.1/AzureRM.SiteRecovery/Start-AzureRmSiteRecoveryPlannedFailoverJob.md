---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: e723aacbfbd1b782a91fdc6aa589bfe15df42cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545984"
---
# <span data-ttu-id="fe940-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="fe940-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="fe940-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe940-102">SYNOPSIS</span></span>
<span data-ttu-id="fe940-103">Rozpoczyna operację planowanej pracy awaryjnej odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="fe940-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe940-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe940-104">SYNTAX</span></span>

### <span data-ttu-id="fe940-105">ByPEObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe940-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe940-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="fe940-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe940-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="fe940-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe940-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fe940-108">DESCRIPTION</span></span>
<span data-ttu-id="fe940-109">Polecenie cmdlet **Start-AzureRmSiteRecoveryPlannedFailoverJob** rozpoczyna planowaną pracę w trybie failover dla jednostki ochrony usługi Azure Site Recovery lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="fe940-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="fe940-110">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmSiteRecoveryJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe940-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="fe940-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe940-111">EXAMPLES</span></span>

## <span data-ttu-id="fe940-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe940-112">PARAMETERS</span></span>

### <span data-ttu-id="fe940-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="fe940-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="fe940-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fe940-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe940-115">Tak/nie1</span><span class="sxs-lookup"><span data-stu-id="fe940-115">Yes</span></span>
- <span data-ttu-id="fe940-116">Ma</span><span class="sxs-lookup"><span data-stu-id="fe940-116">No</span></span>

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

### <span data-ttu-id="fe940-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="fe940-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="fe940-118">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="fe940-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="fe940-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="fe940-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="fe940-120">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="fe940-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="fe940-121">-Direction</span><span class="sxs-lookup"><span data-stu-id="fe940-121">-Direction</span></span>
<span data-ttu-id="fe940-122">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="fe940-122">Specifies the direction of the failover.</span></span>
<span data-ttu-id="fe940-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fe940-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe940-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="fe940-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="fe940-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="fe940-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="fe940-126">— Optymalizuj</span><span class="sxs-lookup"><span data-stu-id="fe940-126">-Optimize</span></span>
<span data-ttu-id="fe940-127">Określa, do czego należy zoptymalizować.</span><span class="sxs-lookup"><span data-stu-id="fe940-127">Specifies what to optimize for.</span></span>
<span data-ttu-id="fe940-128">Ten parametr jest stosowany, gdy praca awaryjna została wykonana z witryny platformy Azure do witryny lokalnej, która wymaga znacznej synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="fe940-128">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="fe940-129">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="fe940-129">Valid values are:</span></span>

- <span data-ttu-id="fe940-130">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="fe940-130">ForDowntime</span></span>
- <span data-ttu-id="fe940-131">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="fe940-131">ForSynchronization</span></span>

<span data-ttu-id="fe940-132">Gdy jest określony **ForDowntime** , oznacza to, że dane są synchronizowane przed przejściem w tryb pracy awaryjnej w celu zminimalizowania przestojów.</span><span class="sxs-lookup"><span data-stu-id="fe940-132">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="fe940-133">Synchronizacja jest przeprowadzana bez zamykania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fe940-133">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="fe940-134">Po zakończeniu synchronizacji zadanie zostaje zawieszone.</span><span class="sxs-lookup"><span data-stu-id="fe940-134">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="fe940-135">Wznów zadanie, aby wykonać dodatkową operację synchronizacji, która zamyka maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="fe940-135">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="fe940-136">Gdy jest określony **ForSynchronization** , oznacza to, że dane są synchronizowane podczas pracy awaryjnej tylko wtedy, gdy synchronizacja danych jest zminimalizowana.</span><span class="sxs-lookup"><span data-stu-id="fe940-136">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="fe940-137">Jeśli to ustawienie jest włączone, maszyna wirtualna zostanie natychmiast ZAMKNIĘTA.</span><span class="sxs-lookup"><span data-stu-id="fe940-137">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="fe940-138">Synchronizacja rozpoczyna się po zamknięciu, aby ukończyć operację przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="fe940-138">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="fe940-139">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="fe940-139">-ProtectionEntity</span></span>
<span data-ttu-id="fe940-140">Określa obiekt jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="fe940-140">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe940-141">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fe940-141">-RecoveryPlan</span></span>
<span data-ttu-id="fe940-142">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="fe940-142">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe940-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fe940-143">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe940-144">-Server</span><span class="sxs-lookup"><span data-stu-id="fe940-144">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe940-145">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fe940-145">-ServicesProvider</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe940-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe940-146">-DefaultProfile</span></span>
<span data-ttu-id="fe940-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe940-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe940-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe940-148">CommonParameters</span></span>
<span data-ttu-id="fe940-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe940-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe940-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe940-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe940-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe940-151">INPUTS</span></span>

### <span data-ttu-id="fe940-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="fe940-152">ASRProtectionEntity</span></span>
<span data-ttu-id="fe940-153">Parametr "ProtectionEntity" akceptuje wartość typu "ASRProtectionEntity" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="fe940-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="fe940-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fe940-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="fe940-155">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="fe940-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="fe940-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fe940-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="fe940-157">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="fe940-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="fe940-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe940-158">OUTPUTS</span></span>

### <span data-ttu-id="fe940-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fe940-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fe940-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe940-160">NOTES</span></span>

## <span data-ttu-id="fe940-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe940-161">RELATED LINKS</span></span>

