---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189314"
---
# <span data-ttu-id="c6768-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="c6768-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="c6768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6768-102">SYNOPSIS</span></span>
<span data-ttu-id="c6768-103">Tworzy konfigurację ASR NIC zawierającą szczegóły konfiguracji związanej z trybu failover i testowanie jej.</span><span class="sxs-lookup"><span data-stu-id="c6768-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="c6768-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6768-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryNicName <String>] [-RecoveryNicResourceGroupName <String>]
 [-ReuseExistingNic] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoNicName <String>] [-TfoNicResourceGroupName <String>] [-TfoReuseExistingNic] [-TfoVMSubnetName <String>]
 [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo] [-TfoNicStaticIPAddress <String>]
 [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6768-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6768-105">DESCRIPTION</span></span>
<span data-ttu-id="c6768-106">Polecenie **cmdlet New-AzRecoveryServicesAsrVMNicConfig** tworzy obiekt konfiguracji ASR NIC zawierający szczegóły związane z trybu failover i testowanie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="c6768-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="c6768-107">W przypadku, gdy żadne informacje nie zostaną przekazane, odpowiednie wartości są wybierane z elementu chronionego replikacją, aby uniknąć aktualizowania tych wartości do wartości null.</span><span class="sxs-lookup"><span data-stu-id="c6768-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="c6768-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6768-108">EXAMPLES</span></span>

### <span data-ttu-id="c6768-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c6768-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="c6768-110">Tworzy obiekt ASRVmNicConfig z trybu failover i przetestuj faiover sieciowe ustawienia skonfigurowane dla nic.</span><span class="sxs-lookup"><span data-stu-id="c6768-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="c6768-111">Każda właściwość, która nie jest przekazywana powyżej, jest pobierana z przekazywanego elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="c6768-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="c6768-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c6768-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="c6768-113">Tworzy obiekt ASRVmNicConfig z testowymi ustawieniami sieci faiover skonfigurowanymi dla zmiany nazwy przez nic.</span><span class="sxs-lookup"><span data-stu-id="c6768-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="c6768-114">Każda właściwość, która nie jest przekazywana powyżej, jest pobierana z przekazywanego elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="c6768-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="c6768-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c6768-115">Example 3</span></span>

<span data-ttu-id="c6768-116">Tworzy konfigurację ASR NIC zawierającą szczegóły konfiguracji związanej z trybu failover i testowanie jej.</span><span class="sxs-lookup"><span data-stu-id="c6768-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="c6768-117">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="c6768-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="c6768-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6768-118">PARAMETERS</span></span>

### <span data-ttu-id="c6768-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6768-119">-DefaultProfile</span></span>
<span data-ttu-id="c6768-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6768-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6768-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="c6768-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="c6768-122">Określa, czy tryb sieci przyspieszonej jest włączony w przypadku karty NIC odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c6768-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6768-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="c6768-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="c6768-124">Określa, czy tryb sieci przyspieszonej jest włączony w testowej chmurze trybu failover.</span><span class="sxs-lookup"><span data-stu-id="c6768-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6768-125">- NicId</span><span class="sxs-lookup"><span data-stu-id="c6768-125">-NicId</span></span>
<span data-ttu-id="c6768-126">Określ identyfikator GUID NIC ASR.</span><span class="sxs-lookup"><span data-stu-id="c6768-126">Specify the ASR NIC GUID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6768-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c6768-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="c6768-128">Określa identyfikatory pul adresów zaplecza dla karty NIC odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c6768-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6768-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c6768-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="c6768-130">Określa identyfikator NSG skojarzonego z skojarzoną z siecią NIC odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c6768-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="c6768-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="c6768-131">-RecoveryNicName</span></span>
<span data-ttu-id="c6768-132">Określa nazwę nic odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c6768-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="c6768-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6768-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="c6768-134">Określa nazwę grupy zasobów NIC odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c6768-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="c6768-135">-RecoveryNicDressIPAddress</span><span class="sxs-lookup"><span data-stu-id="c6768-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="c6768-136">Określa adres IP sieci NIC odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c6768-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="c6768-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="c6768-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="c6768-138">Określa identyfikator publicznego adresu IP skojarzonego z siecią NIC odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c6768-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="c6768-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="c6768-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="c6768-140">Określa identyfikator sieci wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c6768-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="c6768-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="c6768-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="c6768-142">Określa nazwę podsieci odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c6768-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="c6768-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c6768-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c6768-144">Określanie elementu chronionego replikacją asr.</span><span class="sxs-lookup"><span data-stu-id="c6768-144">Specify the ASR Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6768-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="c6768-145">-ReuseExistingNic</span></span>
<span data-ttu-id="c6768-146">Określa, czy podczas trybu failover można używać istniejącej karty nic.</span><span class="sxs-lookup"><span data-stu-id="c6768-146">Specifies whether an existing NIC can be used during failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6768-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c6768-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="c6768-148">Określa identyfikatory pul adresów zaplecza dla karty NIC odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c6768-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6768-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c6768-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="c6768-150">Określa identyfikator NSG skojarzony z testową skojarzoną z skojarzoną z testową skojarzoną z siecią NIC trybu failover.</span><span class="sxs-lookup"><span data-stu-id="c6768-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="c6768-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="c6768-151">-TfoNicName</span></span>
<span data-ttu-id="c6768-152">Określa nazwę testu trybu failover NIC.</span><span class="sxs-lookup"><span data-stu-id="c6768-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="c6768-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6768-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="c6768-154">Określa nazwę testowej grupy zasobów NIC trybu failover.</span><span class="sxs-lookup"><span data-stu-id="c6768-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="c6768-155">-TfoNicDressIPAddress</span><span class="sxs-lookup"><span data-stu-id="c6768-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="c6768-156">Określa adres IP testowej nic trybu failover.</span><span class="sxs-lookup"><span data-stu-id="c6768-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="c6768-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="c6768-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="c6768-158">Określa identyfikator publicznego adresu IP skojarzonego z testową skojarzoną z siecią NIC trybu failover.</span><span class="sxs-lookup"><span data-stu-id="c6768-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="c6768-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="c6768-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="c6768-160">Określa, czy podczas testowania trybu failover może być używana istniejąca karta NIC.</span><span class="sxs-lookup"><span data-stu-id="c6768-160">Specifies whether an existing NIC can be used during test failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6768-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="c6768-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="c6768-162">Określa identyfikator testowej sieci wirtualnej trybu failover.</span><span class="sxs-lookup"><span data-stu-id="c6768-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="c6768-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="c6768-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="c6768-164">Określa nazwę testowej podsieci trybu failover.</span><span class="sxs-lookup"><span data-stu-id="c6768-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="c6768-165">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6768-165">-Confirm</span></span>
<span data-ttu-id="c6768-166">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c6768-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6768-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6768-167">-WhatIf</span></span>
<span data-ttu-id="c6768-168">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6768-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6768-169">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c6768-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6768-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6768-170">CommonParameters</span></span>
<span data-ttu-id="c6768-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6768-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6768-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6768-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6768-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6768-173">INPUTS</span></span>

### <span data-ttu-id="c6768-174">Brak</span><span class="sxs-lookup"><span data-stu-id="c6768-174">None</span></span>

## <span data-ttu-id="c6768-175">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6768-175">OUTPUTS</span></span>

### <span data-ttu-id="c6768-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="c6768-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="c6768-177">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6768-177">NOTES</span></span>

## <span data-ttu-id="c6768-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6768-178">RELATED LINKS</span></span>
