---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192826"
---
# <span data-ttu-id="42ef4-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="42ef4-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="42ef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="42ef4-103">Rozpoczyna testowanie operacji trybu failover.</span><span class="sxs-lookup"><span data-stu-id="42ef4-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="42ef4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="42ef4-104">SYNTAX</span></span>

### <span data-ttu-id="42ef4-105">ByRPIObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="42ef4-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ef4-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="42ef4-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ef4-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="42ef4-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ef4-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="42ef4-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ef4-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="42ef4-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ef4-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="42ef4-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42ef4-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="42ef4-111">DESCRIPTION</span></span>
<span data-ttu-id="42ef4-112">Polecenie cmdlet **Start-AzRecoveryServicesAsrTestFailoverJob** uruchamia test trybu failover elementu chronionego replikacją usługi Azure Site Recovery lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="42ef4-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="42ef4-113">Możesz sprawdzić, czy zadanie zakończyło się pomyślnie za pomocą Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42ef4-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="42ef4-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="42ef4-114">EXAMPLES</span></span>

### <span data-ttu-id="42ef4-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42ef4-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="42ef4-116">Rozpoczyna testowanie operacji trybu failover dla planu odzyskiwania z określonymi parametrami i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="42ef4-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="42ef4-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="42ef4-117">Example 2</span></span>

<span data-ttu-id="42ef4-118">Rozpoczyna testowanie operacji trybu failover.</span><span class="sxs-lookup"><span data-stu-id="42ef4-118">Starts a test failover operation.</span></span> <span data-ttu-id="42ef4-119">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="42ef4-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="42ef4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42ef4-120">PARAMETERS</span></span>

### <span data-ttu-id="42ef4-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="42ef4-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="42ef4-122">Określa identyfikator sieci maszyny wirtualnej platformy Azure dla odzyskiwania maszyny wirtualnej po trybie failover.</span><span class="sxs-lookup"><span data-stu-id="42ef4-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="42ef4-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="42ef4-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="42ef4-124">Określa, czy należy utworzyć nową usługę w chmurze, czy też do testowania trybu failover powinna zostać użyta usługa odzyskiwania w chmurze skonfigurowana dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="42ef4-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="42ef4-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="42ef4-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="42ef4-126">Określa plik certyfikatu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="42ef4-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="42ef4-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="42ef4-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="42ef4-128">Określa plik certyfikatu pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="42ef4-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="42ef4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ef4-129">-DefaultProfile</span></span>
<span data-ttu-id="42ef4-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="42ef4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="42ef4-131">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="42ef4-131">-Direction</span></span>
<span data-ttu-id="42ef4-132">Określa kierunek trybu failover.</span><span class="sxs-lookup"><span data-stu-id="42ef4-132">Specifies the failover direction.</span></span>
<span data-ttu-id="42ef4-133">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="42ef4-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="42ef4-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="42ef4-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="42ef4-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="42ef4-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="42ef4-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42ef4-136">-RecoveryPlan</span></span>
<span data-ttu-id="42ef4-137">Określa obiekt planu odzyskiwania po stronie asr.</span><span class="sxs-lookup"><span data-stu-id="42ef4-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="42ef4-138">- RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="42ef4-138">-RecoveryPoint</span></span>
<span data-ttu-id="42ef4-139">Określa niestandardowy punkt odzyskiwania do przetestowania trybu failover chronionego komputera.</span><span class="sxs-lookup"><span data-stu-id="42ef4-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="42ef4-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="42ef4-140">-RecoveryTag</span></span>
<span data-ttu-id="42ef4-141">Określa tag odzyskiwania do przetestowania trybu failover</span><span class="sxs-lookup"><span data-stu-id="42ef4-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="42ef4-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="42ef4-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="42ef4-143">Określa element chroniony replikacją asr.</span><span class="sxs-lookup"><span data-stu-id="42ef4-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="42ef4-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="42ef4-144">-VMNetwork</span></span>
<span data-ttu-id="42ef4-145">Określa sieć maszyn wirtualnych odzyskiwania witryny w celu połączenia testowych maszyn wirtualnych trybu failover.</span><span class="sxs-lookup"><span data-stu-id="42ef4-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="42ef4-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42ef4-146">-Confirm</span></span>
<span data-ttu-id="42ef4-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="42ef4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42ef4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ef4-148">-WhatIf</span></span>
<span data-ttu-id="42ef4-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42ef4-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42ef4-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="42ef4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42ef4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ef4-151">CommonParameters</span></span>
<span data-ttu-id="42ef4-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ef4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ef4-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42ef4-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ef4-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42ef4-154">INPUTS</span></span>

### <span data-ttu-id="42ef4-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42ef4-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="42ef4-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="42ef4-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="42ef4-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42ef4-157">OUTPUTS</span></span>

### <span data-ttu-id="42ef4-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="42ef4-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="42ef4-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="42ef4-159">NOTES</span></span>

## <span data-ttu-id="42ef4-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42ef4-160">RELATED LINKS</span></span>

[<span data-ttu-id="42ef4-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="42ef4-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
