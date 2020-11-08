---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f7b6cd7171b6f50ed0f239e733ca98f0ecd5c05a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051652"
---
# <span data-ttu-id="953b8-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="953b8-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="953b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="953b8-102">SYNOPSIS</span></span>
<span data-ttu-id="953b8-103">Tworzy konfigurację karty interfejsu sieciowego ASR zawierającą szczegóły konfiguracji dotyczące pracy awaryjnej i testowej w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="953b8-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="953b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="953b8-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoVMSubnetName <String>] [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo]
 [-TfoNicStaticIPAddress <String>] [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="953b8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="953b8-105">DESCRIPTION</span></span>
<span data-ttu-id="953b8-106">Polecenie cmdlet **New-AzRecoveryServicesAsrVMNicConfig** umożliwia utworzenie obiektu konfiguracji karty interfejsu sieciowego ASR zawierającego szczegółowe dane związane z pracą awaryjną i testem pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="953b8-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="953b8-107">W przypadku nieprzekazania żadnych informacji odpowiednie wartości są pobierane z chronionego elementu replikacji w celu uniknięcia zmiany wartości null.</span><span class="sxs-lookup"><span data-stu-id="953b8-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="953b8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="953b8-108">EXAMPLES</span></span>

### <span data-ttu-id="953b8-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="953b8-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="953b8-110">Tworzy obiekt ASRVmNicConfig z ustawieniami sieciowymi trybu failover i test faiover skonfigurowanymi dla karty NIC.</span><span class="sxs-lookup"><span data-stu-id="953b8-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="953b8-111">Każda właściwość, która nie została przekazana powyżej, jest pobierana z przekazanego elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="953b8-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

## <span data-ttu-id="953b8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="953b8-112">PARAMETERS</span></span>

### <span data-ttu-id="953b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953b8-113">-DefaultProfile</span></span>
<span data-ttu-id="953b8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="953b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="953b8-115">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="953b8-115">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="953b8-116">Określa, czy na karcie odzyskiwania NIC jest włączona przyspieszona sieć.</span><span class="sxs-lookup"><span data-stu-id="953b8-116">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="953b8-117">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="953b8-117">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="953b8-118">Określa, czy funkcja przyspieszania sieci jest włączona na testowej karcie interfejsu sieciowego w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="953b8-118">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="953b8-119">-NicId</span><span class="sxs-lookup"><span data-stu-id="953b8-119">-NicId</span></span>
<span data-ttu-id="953b8-120">Określ identyfikator GUID karty ASR.</span><span class="sxs-lookup"><span data-stu-id="953b8-120">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="953b8-121">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="953b8-121">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="953b8-122">Określa identyfikatory pul adresów zaplecza na karcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="953b8-122">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="953b8-123">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="953b8-123">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="953b8-124">Określa identyfikator NSG skojarzonego z kartą sieciową odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="953b8-124">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="953b8-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="953b8-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="953b8-126">Określa adres IP karty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="953b8-126">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="953b8-127">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="953b8-127">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="953b8-128">Określa identyfikator publicznego adresu IP skojarzonego z kartą sieciową odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="953b8-128">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="953b8-129">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="953b8-129">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="953b8-130">Określa identyfikator sieci wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="953b8-130">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="953b8-131">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="953b8-131">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="953b8-132">Określa nazwę podsieci odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="953b8-132">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="953b8-133">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="953b8-133">-ReplicationProtectedItem</span></span>
<span data-ttu-id="953b8-134">Określ element chroniony replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="953b8-134">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="953b8-135">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="953b8-135">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="953b8-136">Określa identyfikatory pul adresów zaplecza na karcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="953b8-136">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="953b8-137">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="953b8-137">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="953b8-138">Określa identyfikator NSG skojarzonego z testową kartą sieciową w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="953b8-138">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="953b8-139">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="953b8-139">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="953b8-140">Określa adres IP karty interfejsu sieciowego testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="953b8-140">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="953b8-141">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="953b8-141">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="953b8-142">Określa identyfikator publicznego adresu IP skojarzonego z testową kartą sieciową w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="953b8-142">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="953b8-143">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="953b8-143">-TfoVMNetworkId</span></span>
<span data-ttu-id="953b8-144">Określa identyfikator sieci wirtualnej testowej pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="953b8-144">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="953b8-145">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="953b8-145">-TfoVMSubnetName</span></span>
<span data-ttu-id="953b8-146">Określa nazwę podsieci testowej trybu failover.</span><span class="sxs-lookup"><span data-stu-id="953b8-146">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="953b8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953b8-147">CommonParameters</span></span>
<span data-ttu-id="953b8-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="953b8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953b8-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="953b8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953b8-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="953b8-150">INPUTS</span></span>

### <span data-ttu-id="953b8-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="953b8-151">None</span></span>

## <span data-ttu-id="953b8-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="953b8-152">OUTPUTS</span></span>

### <span data-ttu-id="953b8-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="953b8-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="953b8-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="953b8-154">NOTES</span></span>

## <span data-ttu-id="953b8-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="953b8-155">RELATED LINKS</span></span>
