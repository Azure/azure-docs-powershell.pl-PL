---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 3be41be3c62b0676ea10e9fe7c9d89927c4de757
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052203"
---
# <span data-ttu-id="9e2bb-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="9e2bb-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="9e2bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2bb-103">Polecenie cmdlet New-AzVirtualHubVnetConnection tworzy zasób HubVirtualNetworkConnection, który jest równorzędny siecią wirtualną do wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="9e2bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e2bb-104">SYNTAX</span></span>

### <span data-ttu-id="9e2bb-105">ByVirtualHubNameByRemoteVirtualNetworkObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9e2bb-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e2bb-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9e2bb-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e2bb-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="9e2bb-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e2bb-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9e2bb-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e2bb-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="9e2bb-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e2bb-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9e2bb-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e2bb-111">Opis</span><span class="sxs-lookup"><span data-stu-id="9e2bb-111">DESCRIPTION</span></span>
<span data-ttu-id="9e2bb-112">Polecenie cmdlet New-AzVirtualHubVnetConnection tworzy zasób HubVirtualNetworkConnection, który jest równorzędny siecią wirtualną do wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="9e2bb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e2bb-113">EXAMPLES</span></span>

### <span data-ttu-id="9e2bb-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e2bb-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
```

<span data-ttu-id="9e2bb-115">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="9e2bb-116">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="9e2bb-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e2bb-117">PARAMETERS</span></span>

### <span data-ttu-id="9e2bb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e2bb-118">-AsJob</span></span>
<span data-ttu-id="9e2bb-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9e2bb-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2bb-120">-DefaultProfile</span></span>
<span data-ttu-id="9e2bb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2bb-122">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="9e2bb-122">-EnableInternetSecurity</span></span>
<span data-ttu-id="9e2bb-123">Włączanie zabezpieczeń internetowych dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="9e2bb-123">Enable internet security for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2bb-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e2bb-124">-Name</span></span>
<span data-ttu-id="9e2bb-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2bb-126">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="9e2bb-126">-ParentObject</span></span>
<span data-ttu-id="9e2bb-127">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2bb-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9e2bb-128">-ParentResourceId</span></span>
<span data-ttu-id="9e2bb-129">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-129">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2bb-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="9e2bb-130">-ParentResourceName</span></span>
<span data-ttu-id="9e2bb-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2bb-132">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e2bb-132">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="9e2bb-133">Zdalna Sieć wirtualna, do której jest podłączone połączenie z siecią wirtualną centrum.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2bb-134">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9e2bb-134">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="9e2bb-135">Zdalna Sieć wirtualna, do której jest podłączone połączenie z siecią wirtualną centrum.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-135">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2bb-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e2bb-136">-ResourceGroupName</span></span>
<span data-ttu-id="9e2bb-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2bb-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e2bb-138">-Confirm</span></span>
<span data-ttu-id="9e2bb-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e2bb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e2bb-140">-WhatIf</span></span>
<span data-ttu-id="9e2bb-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e2bb-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e2bb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2bb-143">CommonParameters</span></span>
<span data-ttu-id="9e2bb-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2bb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2bb-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e2bb-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2bb-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e2bb-146">INPUTS</span></span>

### <span data-ttu-id="9e2bb-147">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9e2bb-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="9e2bb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9e2bb-148">System.String</span></span>

## <span data-ttu-id="9e2bb-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e2bb-149">OUTPUTS</span></span>

### <span data-ttu-id="9e2bb-150">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="9e2bb-150">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="9e2bb-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e2bb-151">NOTES</span></span>

## <span data-ttu-id="9e2bb-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e2bb-152">RELATED LINKS</span></span>

[<span data-ttu-id="9e2bb-153">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="9e2bb-153">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="9e2bb-154">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="9e2bb-154">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
