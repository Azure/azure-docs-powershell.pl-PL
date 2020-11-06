---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 8aeb992b08e2749168ef3da2db6c264158c6a9ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541704"
---
# <span data-ttu-id="ae346-101">Get-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ae346-101">Get-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="ae346-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae346-102">SYNOPSIS</span></span>
<span data-ttu-id="ae346-103">Pobiera wirtualne połączenie sieciowe w wirtualnym koncentratorze lub zawiera listę wszystkich wirtualnych połączeń sieciowych w koncentratorze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="ae346-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae346-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae346-104">SYNTAX</span></span>

### <span data-ttu-id="ae346-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ae346-105">ByVirtualHubName (Default)</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae346-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ae346-106">ByVirtualHubObject</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae346-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ae346-107">ByVirtualHubResourceId</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae346-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ae346-108">DESCRIPTION</span></span>
<span data-ttu-id="ae346-109">Pobiera wirtualne połączenie sieciowe w wirtualnym koncentratorze lub zawiera listę wszystkich wirtualnych połączeń sieciowych w koncentratorze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="ae346-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="ae346-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae346-110">EXAMPLES</span></span>

### <span data-ttu-id="ae346-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae346-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="ae346-112">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ae346-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="ae346-113">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae346-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="ae346-114">Po utworzeniu połączenia z siecią wirtualną centralą zostanie wykorzystana wirtualna sieć centralnego połączenia z siecią, na której znajduje się nazwa grupy zasobów, nazwa centrum i nazwa połączenia.</span><span class="sxs-lookup"><span data-stu-id="ae346-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="ae346-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ae346-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="ae346-116">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ae346-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="ae346-117">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae346-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="ae346-118">Po utworzeniu połączenia z siecią wirtualną centralą jest wyświetlane wszystkie wirtualne połączenie sieciowe z centrum, w którym jest używana nazwa grupy zasobów i nazwa centrum.</span><span class="sxs-lookup"><span data-stu-id="ae346-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

## <span data-ttu-id="ae346-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae346-119">PARAMETERS</span></span>

### <span data-ttu-id="ae346-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae346-120">-DefaultProfile</span></span>
<span data-ttu-id="ae346-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae346-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae346-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae346-122">-Name</span></span>
<span data-ttu-id="ae346-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ae346-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae346-124">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="ae346-124">-ParentObject</span></span>
<span data-ttu-id="ae346-125">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="ae346-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae346-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ae346-126">-ParentResourceId</span></span>
<span data-ttu-id="ae346-127">Identyfikator zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="ae346-127">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae346-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ae346-128">-ParentResourceName</span></span>
<span data-ttu-id="ae346-129">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="ae346-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae346-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae346-130">-ResourceGroupName</span></span>
<span data-ttu-id="ae346-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae346-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae346-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae346-132">CommonParameters</span></span>
<span data-ttu-id="ae346-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae346-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae346-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae346-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae346-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae346-135">INPUTS</span></span>

### <span data-ttu-id="ae346-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ae346-136">None</span></span>

## <span data-ttu-id="ae346-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae346-137">OUTPUTS</span></span>

### <span data-ttu-id="ae346-138">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="ae346-138">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="ae346-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae346-139">NOTES</span></span>

## <span data-ttu-id="ae346-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae346-140">RELATED LINKS</span></span>
