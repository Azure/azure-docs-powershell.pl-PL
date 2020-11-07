---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: a05467b19aaf69bccdca64c8e17b894941f3ac6f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708556"
---
# <span data-ttu-id="6a938-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="6a938-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="6a938-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a938-102">SYNOPSIS</span></span>
<span data-ttu-id="6a938-103">Rozpoczyna operację testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="6a938-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="6a938-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a938-104">SYNTAX</span></span>

### <span data-ttu-id="6a938-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6a938-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a938-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="6a938-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a938-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="6a938-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a938-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6a938-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a938-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="6a938-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a938-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6a938-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a938-111">Opis</span><span class="sxs-lookup"><span data-stu-id="6a938-111">DESCRIPTION</span></span>
<span data-ttu-id="6a938-112">Polecenie cmdlet **Start-AzRecoveryServicesAsrTestFailoverJob** rozpoczyna test pracy awaryjnej w trybie failover witryny usługi Azure chronionej przed replikacją lub planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6a938-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="6a938-113">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a938-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="6a938-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a938-114">EXAMPLES</span></span>

### <span data-ttu-id="6a938-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6a938-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="6a938-116">Rozpoczyna operację testowej pracy w trybie failover dla planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="6a938-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6a938-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a938-117">PARAMETERS</span></span>

### <span data-ttu-id="6a938-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6a938-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="6a938-119">{{Fill AzureVMNetworkId Description}}</span><span class="sxs-lookup"><span data-stu-id="6a938-119">{{Fill AzureVMNetworkId Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a938-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="6a938-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="6a938-121">Określa, czy należy utworzyć nową usługę w chmurze, czy należy użyć usługi chmury odzyskiwania skonfigurowanej dla maszyny wirtualnej na potrzeby testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="6a938-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a938-122">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6a938-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="6a938-123">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a938-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="6a938-124">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6a938-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="6a938-125">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6a938-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="6a938-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a938-126">-DefaultProfile</span></span>
<span data-ttu-id="6a938-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a938-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6a938-128">-Direction</span><span class="sxs-lookup"><span data-stu-id="6a938-128">-Direction</span></span>
<span data-ttu-id="6a938-129">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="6a938-129">Specifies the failover direction.</span></span>
<span data-ttu-id="6a938-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a938-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a938-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="6a938-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="6a938-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="6a938-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="6a938-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6a938-133">-RecoveryPlan</span></span>
<span data-ttu-id="6a938-134">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="6a938-134">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a938-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6a938-135">-RecoveryPoint</span></span>
<span data-ttu-id="6a938-136">Umożliwia określenie niestandardowego punktu odzyskiwania w celu przetestowania trybu failover chronionego komputera.</span><span class="sxs-lookup"><span data-stu-id="6a938-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a938-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="6a938-137">-RecoveryTag</span></span>
<span data-ttu-id="6a938-138">Określa znacznik odzyskiwania w celu przetestowania trybu failover na</span><span class="sxs-lookup"><span data-stu-id="6a938-138">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a938-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6a938-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6a938-140">Określa element chroniony replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="6a938-140">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a938-141">-Sieć VMNetwork</span><span class="sxs-lookup"><span data-stu-id="6a938-141">-VMNetwork</span></span>
<span data-ttu-id="6a938-142">Określa sieć maszyny wirtualnej odzyskiwania witryny, do której mają być połączone maszyny wirtualne testowe w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="6a938-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a938-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a938-143">-Confirm</span></span>
<span data-ttu-id="6a938-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a938-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a938-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a938-145">-WhatIf</span></span>
<span data-ttu-id="6a938-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a938-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a938-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a938-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a938-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a938-148">CommonParameters</span></span>
<span data-ttu-id="6a938-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a938-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a938-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a938-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a938-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a938-151">INPUTS</span></span>

### <span data-ttu-id="6a938-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6a938-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="6a938-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6a938-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6a938-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a938-154">OUTPUTS</span></span>

### <span data-ttu-id="6a938-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6a938-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6a938-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a938-156">NOTES</span></span>

## <span data-ttu-id="6a938-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a938-157">RELATED LINKS</span></span>

[<span data-ttu-id="6a938-158">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6a938-158">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)