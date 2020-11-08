---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223229"
---
# <span data-ttu-id="a1127-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="a1127-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="a1127-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1127-102">SYNOPSIS</span></span>
<span data-ttu-id="a1127-103">Tworzy konfigurację karty interfejsu sieciowego ASR zawierającą szczegóły konfiguracji dotyczące pracy awaryjnej i testowej w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="a1127-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="a1127-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1127-104">SYNTAX</span></span>

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

## <span data-ttu-id="a1127-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a1127-105">DESCRIPTION</span></span>
<span data-ttu-id="a1127-106">Polecenie cmdlet **New-AzRecoveryServicesAsrVMNicConfig** umożliwia utworzenie obiektu konfiguracji karty interfejsu sieciowego ASR zawierającego szczegółowe dane związane z pracą awaryjną i testem pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="a1127-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="a1127-107">W przypadku nieprzekazania żadnych informacji odpowiednie wartości są pobierane z chronionego elementu replikacji w celu uniknięcia zmiany wartości null.</span><span class="sxs-lookup"><span data-stu-id="a1127-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="a1127-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1127-108">EXAMPLES</span></span>

### <span data-ttu-id="a1127-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1127-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="a1127-110">Tworzy obiekt ASRVmNicConfig z ustawieniami sieciowymi trybu failover i test faiover skonfigurowanymi dla karty NIC.</span><span class="sxs-lookup"><span data-stu-id="a1127-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="a1127-111">Każda właściwość, która nie została przekazana powyżej, jest pobierana z przekazanego elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="a1127-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="a1127-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a1127-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="a1127-113">Tworzy obiekt ASRVmNicConfig z ustawieniami sieci faiover testowymi skonfigurowanymi dla zmiany nazwy karty sieciowej.</span><span class="sxs-lookup"><span data-stu-id="a1127-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="a1127-114">Każda właściwość, która nie została przekazana powyżej, jest pobierana z przekazanego elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="a1127-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="a1127-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a1127-115">Example 3</span></span>

<span data-ttu-id="a1127-116">Tworzy konfigurację karty interfejsu sieciowego ASR zawierającą szczegóły konfiguracji dotyczące pracy awaryjnej i testowej w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="a1127-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="a1127-117">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="a1127-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="a1127-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1127-118">PARAMETERS</span></span>

### <span data-ttu-id="a1127-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1127-119">-DefaultProfile</span></span>
<span data-ttu-id="a1127-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1127-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1127-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="a1127-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="a1127-122">Określa, czy na karcie odzyskiwania NIC jest włączona przyspieszona sieć.</span><span class="sxs-lookup"><span data-stu-id="a1127-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="a1127-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="a1127-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="a1127-124">Określa, czy funkcja przyspieszania sieci jest włączona na testowej karcie interfejsu sieciowego w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="a1127-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="a1127-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="a1127-125">-NicId</span></span>
<span data-ttu-id="a1127-126">Określ identyfikator GUID karty ASR.</span><span class="sxs-lookup"><span data-stu-id="a1127-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="a1127-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a1127-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="a1127-128">Określa identyfikatory pul adresów zaplecza na karcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1127-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="a1127-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a1127-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="a1127-130">Określa identyfikator NSG skojarzonego z kartą sieciową odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1127-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="a1127-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="a1127-131">-RecoveryNicName</span></span>
<span data-ttu-id="a1127-132">Określa nazwę karty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1127-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="a1127-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1127-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="a1127-134">Określa nazwę grupy zasobów karty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1127-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="a1127-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a1127-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="a1127-136">Określa adres IP karty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1127-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="a1127-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a1127-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="a1127-138">Określa identyfikator publicznego adresu IP skojarzonego z kartą sieciową odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1127-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="a1127-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a1127-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="a1127-140">Określa identyfikator sieci wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1127-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="a1127-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="a1127-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="a1127-142">Określa nazwę podsieci odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1127-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="a1127-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a1127-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a1127-144">Określ element chroniony replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="a1127-144">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="a1127-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="a1127-145">-ReuseExistingNic</span></span>
<span data-ttu-id="a1127-146">Określa, czy można korzystać z istniejącej karty sieciowej podczas pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="a1127-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="a1127-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a1127-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="a1127-148">Określa identyfikatory pul adresów zaplecza na karcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a1127-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="a1127-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a1127-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="a1127-150">Określa identyfikator NSG skojarzonego z testową kartą sieciową w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="a1127-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="a1127-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="a1127-151">-TfoNicName</span></span>
<span data-ttu-id="a1127-152">Określa nazwę testowej karty pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="a1127-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="a1127-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1127-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="a1127-154">Określa nazwę grupy zasobów testowej karty pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="a1127-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="a1127-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a1127-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="a1127-156">Określa adres IP karty interfejsu sieciowego testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="a1127-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="a1127-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a1127-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="a1127-158">Określa identyfikator publicznego adresu IP skojarzonego z testową kartą sieciową w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="a1127-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="a1127-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="a1127-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="a1127-160">Określa, czy podczas testu pracy awaryjnej można korzystać z istniejącej karty interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a1127-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="a1127-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a1127-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="a1127-162">Określa identyfikator sieci wirtualnej testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="a1127-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="a1127-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="a1127-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="a1127-164">Określa nazwę podsieci testowej trybu failover.</span><span class="sxs-lookup"><span data-stu-id="a1127-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="a1127-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1127-165">-Confirm</span></span>
<span data-ttu-id="a1127-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1127-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1127-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1127-167">-WhatIf</span></span>
<span data-ttu-id="a1127-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1127-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1127-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1127-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1127-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1127-170">CommonParameters</span></span>
<span data-ttu-id="a1127-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1127-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1127-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1127-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1127-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1127-173">INPUTS</span></span>

### <span data-ttu-id="a1127-174">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a1127-174">None</span></span>

## <span data-ttu-id="a1127-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1127-175">OUTPUTS</span></span>

### <span data-ttu-id="a1127-176">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="a1127-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="a1127-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1127-177">NOTES</span></span>

## <span data-ttu-id="a1127-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1127-178">RELATED LINKS</span></span>
