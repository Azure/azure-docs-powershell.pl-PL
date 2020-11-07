---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e3ba40bf4527571ed6b3396a9208a9a0931a7be7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896610"
---
# <span data-ttu-id="74abb-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="74abb-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="74abb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74abb-102">SYNOPSIS</span></span>
<span data-ttu-id="74abb-103">Aktualizuje istniejące HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="74abb-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="74abb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74abb-104">SYNTAX</span></span>

### <span data-ttu-id="74abb-105">ByHubVirtualNetworkConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="74abb-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74abb-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="74abb-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74abb-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="74abb-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> -EnableInternetSecurity <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74abb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="74abb-108">DESCRIPTION</span></span>
<span data-ttu-id="74abb-109">Aktualizuje istniejące HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="74abb-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="74abb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74abb-110">EXAMPLES</span></span>

### <span data-ttu-id="74abb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74abb-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
```

<span data-ttu-id="74abb-112">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="74abb-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="74abb-113">Zostanie również utworzone wirtualne połączenie sieciowe, które jest równorzędne siecią wirtualną koncentratora wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="74abb-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="74abb-114">To połączenie sieci wirtualnej zostanie następnie zaktualizowane w celu włączenia zabezpieczeń internetowych.</span><span class="sxs-lookup"><span data-stu-id="74abb-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="74abb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74abb-115">PARAMETERS</span></span>

### <span data-ttu-id="74abb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74abb-116">-AsJob</span></span>
<span data-ttu-id="74abb-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="74abb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74abb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74abb-118">-DefaultProfile</span></span>
<span data-ttu-id="74abb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74abb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74abb-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="74abb-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="74abb-121">Włącz zabezpieczenia internetowe dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="74abb-121">Enable internet security for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74abb-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74abb-122">-InputObject</span></span>
<span data-ttu-id="74abb-123">Zasób hubvirtualnetworkconnection do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="74abb-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74abb-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74abb-124">-Name</span></span>
<span data-ttu-id="74abb-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="74abb-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74abb-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="74abb-126">-ParentResourceName</span></span>
<span data-ttu-id="74abb-127">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="74abb-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74abb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74abb-128">-ResourceGroupName</span></span>
<span data-ttu-id="74abb-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74abb-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74abb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74abb-130">-ResourceId</span></span>
<span data-ttu-id="74abb-131">Identyfikator zasobu zasobu hubvirtualnetworkconnection do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="74abb-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74abb-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74abb-132">-Confirm</span></span>
<span data-ttu-id="74abb-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74abb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74abb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74abb-134">-WhatIf</span></span>
<span data-ttu-id="74abb-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74abb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74abb-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74abb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74abb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74abb-137">CommonParameters</span></span>
<span data-ttu-id="74abb-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74abb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74abb-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74abb-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74abb-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74abb-140">INPUTS</span></span>

### <span data-ttu-id="74abb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="74abb-141">System.String</span></span>

### <span data-ttu-id="74abb-142">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="74abb-142">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="74abb-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74abb-143">OUTPUTS</span></span>

### <span data-ttu-id="74abb-144">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="74abb-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="74abb-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74abb-145">NOTES</span></span>

## <span data-ttu-id="74abb-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74abb-146">RELATED LINKS</span></span>