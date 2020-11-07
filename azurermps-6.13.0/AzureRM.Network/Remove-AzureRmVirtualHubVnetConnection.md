---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 3a7c48803f18bf73f75e721296757e37ff89d44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716577"
---
# <span data-ttu-id="f4d4d-101">Remove-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f4d4d-101">Remove-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="f4d4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d4d-103">Polecenie cmdlet Remove-AzureRmVirtualHubVnetConnection usuwa połączenie wirtualnej sieci Azure, które są równorzędne ze zdalną siecią wirtualną do sieci wirtualnej centrali.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-103">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4d4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4d4d-104">SYNTAX</span></span>

### <span data-ttu-id="f4d4d-105">ByHubVirtualNetworkConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4d4d-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4d4d-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f4d4d-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzureRmVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4d4d-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="f4d4d-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4d4d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f4d4d-108">DESCRIPTION</span></span>
<span data-ttu-id="f4d4d-109">Polecenie cmdlet Remove-AzureRmVirtualHubVnetConnection usuwa połączenie wirtualnej sieci Azure, które są równorzędne ze zdalną siecią wirtualną do sieci wirtualnej centrali.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-109">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="f4d4d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4d4d-110">EXAMPLES</span></span>

### <span data-ttu-id="f4d4d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f4d4d-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="f4d4d-112">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f4d4d-113">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="f4d4d-114">Po utworzeniu połączenia z siecią wirtualną centrum usuwa wirtualne połączenie sieciowe z centrum przy użyciu nazwy grupy zasobów, nazwy centrum i nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="f4d4d-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f4d4d-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzureRmHubVnetConnection
```

<span data-ttu-id="f4d4d-116">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f4d4d-117">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="f4d4d-118">Po utworzeniu połączenia z siecią wirtualną centrum usuwa wirtualne połączenie sieciowe z centrum przy użyciu połączeń rurowych programu PowerShell w danych wyjściowych polecenia Get-AzureRmHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzureRmHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="f4d4d-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4d4d-119">PARAMETERS</span></span>

### <span data-ttu-id="f4d4d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4d4d-120">-AsJob</span></span>
<span data-ttu-id="f4d4d-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f4d4d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4d4d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d4d-122">-DefaultProfile</span></span>
<span data-ttu-id="f4d4d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d4d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f4d4d-124">-Force</span></span>
<span data-ttu-id="f4d4d-125">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="f4d4d-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f4d4d-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4d4d-126">-InputObject</span></span>
<span data-ttu-id="f4d4d-127">Zasób hubvirtualnetworkconnection do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d4d-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4d4d-128">-Name</span></span>
<span data-ttu-id="f4d4d-129">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-129">The resource name.</span></span>

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

### <span data-ttu-id="f4d4d-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f4d4d-130">-ParentResourceName</span></span>
<span data-ttu-id="f4d4d-131">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-131">The parent resource name.</span></span>

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

### <span data-ttu-id="f4d4d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4d4d-132">-PassThru</span></span>
<span data-ttu-id="f4d4d-133">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f4d4d-134">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4d4d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d4d-135">-ResourceGroupName</span></span>
<span data-ttu-id="f4d4d-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-136">The resource group name.</span></span>

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

### <span data-ttu-id="f4d4d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4d4d-137">-ResourceId</span></span>
<span data-ttu-id="f4d4d-138">Identyfikator zasobu zasobu hubvirtualnetworkconnection do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="f4d4d-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4d4d-139">-Confirm</span></span>
<span data-ttu-id="f4d4d-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d4d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d4d-141">-WhatIf</span></span>
<span data-ttu-id="f4d4d-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d4d-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d4d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d4d-144">CommonParameters</span></span>
<span data-ttu-id="f4d4d-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d4d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d4d-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d4d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d4d-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4d4d-147">INPUTS</span></span>

### <span data-ttu-id="f4d4d-148">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="f4d4d-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="f4d4d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f4d4d-149">System.String</span></span>

## <span data-ttu-id="f4d4d-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4d4d-150">OUTPUTS</span></span>

### <span data-ttu-id="f4d4d-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4d4d-151">System.Boolean</span></span>

## <span data-ttu-id="f4d4d-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4d4d-152">NOTES</span></span>

## <span data-ttu-id="f4d4d-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4d4d-153">RELATED LINKS</span></span>
