---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 6805d6671d0335599dc95f206ddb8482867734fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717618"
---
# <span data-ttu-id="5ff7b-101">New-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5ff7b-101">New-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="5ff7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ff7b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff7b-103">Polecenie cmdlet New-AzureRmVirtualHubVnetConnection tworzy zasób HubVirtualNetworkConnection, który jest równorzędny siecią wirtualną do wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-103">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ff7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ff7b-104">SYNTAX</span></span>

### <span data-ttu-id="5ff7b-105">ByVirtualHubNameByRemoteVirtualNetworkObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ff7b-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ff7b-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5ff7b-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff7b-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="5ff7b-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ff7b-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5ff7b-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff7b-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="5ff7b-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ff7b-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5ff7b-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff7b-111">Opis</span><span class="sxs-lookup"><span data-stu-id="5ff7b-111">DESCRIPTION</span></span>
<span data-ttu-id="5ff7b-112">Polecenie cmdlet New-AzureRmVirtualHubVnetConnection tworzy zasób HubVirtualNetworkConnection, który jest równorzędny siecią wirtualną do wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-112">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="5ff7b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ff7b-113">EXAMPLES</span></span>

### <span data-ttu-id="5ff7b-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ff7b-114">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="5ff7b-115">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="5ff7b-116">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="5ff7b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ff7b-117">PARAMETERS</span></span>

### <span data-ttu-id="5ff7b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ff7b-118">-AsJob</span></span>
<span data-ttu-id="5ff7b-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5ff7b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ff7b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff7b-120">-DefaultProfile</span></span>
<span data-ttu-id="5ff7b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ff7b-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ff7b-122">-Name</span></span>
<span data-ttu-id="5ff7b-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff7b-124">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="5ff7b-124">-ParentObject</span></span>
<span data-ttu-id="5ff7b-125">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff7b-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ff7b-126">-ParentResourceId</span></span>
<span data-ttu-id="5ff7b-127">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-127">The parent resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff7b-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5ff7b-128">-ParentResourceName</span></span>
<span data-ttu-id="5ff7b-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff7b-130">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5ff7b-130">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="5ff7b-131">Zdalna Sieć wirtualna, do której jest podłączone połączenie z siecią wirtualną centrum.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-131">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff7b-132">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5ff7b-132">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="5ff7b-133">Zdalna Sieć wirtualna, do której jest podłączone połączenie z siecią wirtualną centrum.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff7b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff7b-134">-ResourceGroupName</span></span>
<span data-ttu-id="5ff7b-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff7b-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ff7b-136">-Confirm</span></span>
<span data-ttu-id="5ff7b-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff7b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff7b-138">-WhatIf</span></span>
<span data-ttu-id="5ff7b-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff7b-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff7b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff7b-141">CommonParameters</span></span>
<span data-ttu-id="5ff7b-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff7b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff7b-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff7b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff7b-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ff7b-144">INPUTS</span></span>

### <span data-ttu-id="5ff7b-145">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5ff7b-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="5ff7b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5ff7b-146">System.String</span></span>

## <span data-ttu-id="5ff7b-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ff7b-147">OUTPUTS</span></span>

### <span data-ttu-id="5ff7b-148">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="5ff7b-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="5ff7b-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ff7b-149">NOTES</span></span>

## <span data-ttu-id="5ff7b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ff7b-150">RELATED LINKS</span></span>
