---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358150"
---
# <span data-ttu-id="0ae57-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0ae57-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="0ae57-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ae57-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae57-103">Rozpoczyna operację testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="0ae57-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="0ae57-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ae57-104">SYNTAX</span></span>

### <span data-ttu-id="0ae57-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0ae57-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ae57-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0ae57-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ae57-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0ae57-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ae57-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0ae57-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ae57-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0ae57-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ae57-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0ae57-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ae57-111">Opis</span><span class="sxs-lookup"><span data-stu-id="0ae57-111">DESCRIPTION</span></span>
<span data-ttu-id="0ae57-112">Polecenie cmdlet **Start-AzRecoveryServicesAsrTestFailoverJob** rozpoczyna test pracy awaryjnej w trybie failover witryny usługi Azure chronionej przed replikacją lub planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0ae57-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="0ae57-113">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ae57-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="0ae57-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ae57-114">EXAMPLES</span></span>

### <span data-ttu-id="0ae57-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ae57-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="0ae57-116">Rozpoczyna operację testowej pracy w trybie failover dla planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="0ae57-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="0ae57-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0ae57-117">Example 2</span></span>

<span data-ttu-id="0ae57-118">Rozpoczyna operację testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="0ae57-118">Starts a test failover operation.</span></span> <span data-ttu-id="0ae57-119">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="0ae57-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="0ae57-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ae57-120">PARAMETERS</span></span>

### <span data-ttu-id="0ae57-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0ae57-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="0ae57-122">Określa identyfikator sieci maszyny wirtualnej Azure dla maszyny wirtualnej odzyskiwania po przełączeniu do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="0ae57-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="0ae57-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="0ae57-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="0ae57-124">Określa, czy należy utworzyć nową usługę w chmurze, czy należy użyć usługi chmury odzyskiwania skonfigurowanej dla maszyny wirtualnej na potrzeby testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="0ae57-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="0ae57-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0ae57-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="0ae57-126">Określa podstawowy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0ae57-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="0ae57-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0ae57-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="0ae57-128">Określa pomocniczy plik certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="0ae57-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="0ae57-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae57-129">-DefaultProfile</span></span>
<span data-ttu-id="0ae57-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ae57-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0ae57-131">-Direction</span><span class="sxs-lookup"><span data-stu-id="0ae57-131">-Direction</span></span>
<span data-ttu-id="0ae57-132">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="0ae57-132">Specifies the failover direction.</span></span>
<span data-ttu-id="0ae57-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0ae57-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ae57-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0ae57-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="0ae57-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0ae57-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="0ae57-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0ae57-136">-RecoveryPlan</span></span>
<span data-ttu-id="0ae57-137">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="0ae57-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="0ae57-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0ae57-138">-RecoveryPoint</span></span>
<span data-ttu-id="0ae57-139">Umożliwia określenie niestandardowego punktu odzyskiwania w celu przetestowania trybu failover chronionego komputera.</span><span class="sxs-lookup"><span data-stu-id="0ae57-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="0ae57-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="0ae57-140">-RecoveryTag</span></span>
<span data-ttu-id="0ae57-141">Określa znacznik odzyskiwania w celu przetestowania trybu failover na</span><span class="sxs-lookup"><span data-stu-id="0ae57-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="0ae57-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0ae57-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0ae57-143">Określa element chroniony replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="0ae57-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="0ae57-144">-Sieć VMNetwork</span><span class="sxs-lookup"><span data-stu-id="0ae57-144">-VMNetwork</span></span>
<span data-ttu-id="0ae57-145">Określa sieć maszyny wirtualnej odzyskiwania witryny, do której mają być połączone maszyny wirtualne testowe w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="0ae57-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="0ae57-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ae57-146">-Confirm</span></span>
<span data-ttu-id="0ae57-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ae57-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ae57-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ae57-148">-WhatIf</span></span>
<span data-ttu-id="0ae57-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ae57-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ae57-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ae57-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ae57-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae57-151">CommonParameters</span></span>
<span data-ttu-id="0ae57-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ae57-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae57-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ae57-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae57-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ae57-154">INPUTS</span></span>

### <span data-ttu-id="0ae57-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0ae57-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="0ae57-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0ae57-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0ae57-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ae57-157">OUTPUTS</span></span>

### <span data-ttu-id="0ae57-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0ae57-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0ae57-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ae57-159">NOTES</span></span>

## <span data-ttu-id="0ae57-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ae57-160">RELATED LINKS</span></span>

[<span data-ttu-id="0ae57-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0ae57-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
