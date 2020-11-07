---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: f5bf4372c1140402cb56ca875b5532387dd06704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718425"
---
# <span data-ttu-id="6904e-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="6904e-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="6904e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6904e-102">SYNOPSIS</span></span>
<span data-ttu-id="6904e-103">Rozpoczyna operację planowanej pracy awaryjnej odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="6904e-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6904e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6904e-104">SYNTAX</span></span>

### <span data-ttu-id="6904e-105">ByPEObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6904e-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6904e-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="6904e-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6904e-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="6904e-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6904e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6904e-108">DESCRIPTION</span></span>
<span data-ttu-id="6904e-109">Polecenie cmdlet **Start-AzureRmSiteRecoveryPlannedFailoverJob** rozpoczyna planowaną pracę w trybie failover dla jednostki ochrony usługi Azure Site Recovery lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6904e-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="6904e-110">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmSiteRecoveryJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6904e-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="6904e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6904e-111">EXAMPLES</span></span>

## <span data-ttu-id="6904e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6904e-112">PARAMETERS</span></span>

### <span data-ttu-id="6904e-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="6904e-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="6904e-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6904e-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6904e-115">Tak/nie1</span><span class="sxs-lookup"><span data-stu-id="6904e-115">Yes</span></span>
- <span data-ttu-id="6904e-116">Ma</span><span class="sxs-lookup"><span data-stu-id="6904e-116">No</span></span>

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

### <span data-ttu-id="6904e-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6904e-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="6904e-118">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6904e-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="6904e-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6904e-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="6904e-120">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6904e-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="6904e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6904e-121">-DefaultProfile</span></span>
<span data-ttu-id="6904e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6904e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6904e-123">-Direction</span><span class="sxs-lookup"><span data-stu-id="6904e-123">-Direction</span></span>
<span data-ttu-id="6904e-124">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="6904e-124">Specifies the direction of the failover.</span></span>
<span data-ttu-id="6904e-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6904e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6904e-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="6904e-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="6904e-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="6904e-127">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="6904e-128">— Optymalizuj</span><span class="sxs-lookup"><span data-stu-id="6904e-128">-Optimize</span></span>
<span data-ttu-id="6904e-129">Określa, do czego należy zoptymalizować.</span><span class="sxs-lookup"><span data-stu-id="6904e-129">Specifies what to optimize for.</span></span>
<span data-ttu-id="6904e-130">Ten parametr jest stosowany, gdy praca awaryjna została wykonana z witryny platformy Azure do witryny lokalnej, która wymaga znacznej synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="6904e-130">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="6904e-131">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="6904e-131">Valid values are:</span></span>

- <span data-ttu-id="6904e-132">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="6904e-132">ForDowntime</span></span>
- <span data-ttu-id="6904e-133">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="6904e-133">ForSynchronization</span></span>

<span data-ttu-id="6904e-134">Gdy jest określony **ForDowntime** , oznacza to, że dane są synchronizowane przed przejściem w tryb pracy awaryjnej w celu zminimalizowania przestojów.</span><span class="sxs-lookup"><span data-stu-id="6904e-134">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="6904e-135">Synchronizacja jest przeprowadzana bez zamykania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6904e-135">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="6904e-136">Po zakończeniu synchronizacji zadanie zostaje zawieszone.</span><span class="sxs-lookup"><span data-stu-id="6904e-136">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="6904e-137">Wznów zadanie, aby wykonać dodatkową operację synchronizacji, która zamyka maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="6904e-137">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="6904e-138">Gdy jest określony **ForSynchronization** , oznacza to, że dane są synchronizowane podczas pracy awaryjnej tylko wtedy, gdy synchronizacja danych jest zminimalizowana.</span><span class="sxs-lookup"><span data-stu-id="6904e-138">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="6904e-139">Jeśli to ustawienie jest włączone, maszyna wirtualna zostanie natychmiast ZAMKNIĘTA.</span><span class="sxs-lookup"><span data-stu-id="6904e-139">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="6904e-140">Synchronizacja rozpoczyna się po zamknięciu, aby ukończyć operację przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="6904e-140">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="6904e-141">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6904e-141">-ProtectionEntity</span></span>
<span data-ttu-id="6904e-142">Określa obiekt jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="6904e-142">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6904e-143">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6904e-143">-RecoveryPlan</span></span>
<span data-ttu-id="6904e-144">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6904e-144">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="6904e-145">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6904e-145">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="6904e-146">-Server</span><span class="sxs-lookup"><span data-stu-id="6904e-146">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6904e-147">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6904e-147">-ServicesProvider</span></span>
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

### <span data-ttu-id="6904e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6904e-148">CommonParameters</span></span>
<span data-ttu-id="6904e-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6904e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6904e-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6904e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6904e-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6904e-151">INPUTS</span></span>

### <span data-ttu-id="6904e-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6904e-152">ASRProtectionEntity</span></span>
<span data-ttu-id="6904e-153">Parametr "ProtectionEntity" akceptuje wartość typu "ASRProtectionEntity" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6904e-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="6904e-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6904e-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="6904e-155">Parametr "RecoveryPlan" akceptuje wartość typu "ASRRecoveryPlan" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6904e-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="6904e-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6904e-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="6904e-157">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6904e-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="6904e-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6904e-158">OUTPUTS</span></span>

### <span data-ttu-id="6904e-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6904e-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6904e-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6904e-160">NOTES</span></span>

## <span data-ttu-id="6904e-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6904e-161">RELATED LINKS</span></span>

