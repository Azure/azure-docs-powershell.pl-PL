---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c7f7f8603c03300f4f1df1d47a62ed35ca3b93d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331762"
---
# <span data-ttu-id="2fa1b-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2fa1b-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2fa1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fa1b-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa1b-103">Konfiguruje połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="2fa1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fa1b-104">SYNTAX</span></span>

### <span data-ttu-id="2fa1b-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2fa1b-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa1b-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="2fa1b-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa1b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2fa1b-107">DESCRIPTION</span></span>
<span data-ttu-id="2fa1b-108">Polecenie cmdlet **Set-AzVirtualNetworkGatewayConnection** konfiguruje połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="2fa1b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fa1b-109">EXAMPLES</span></span>

### <span data-ttu-id="2fa1b-110">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="2fa1b-110">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

### <span data-ttu-id="2fa1b-111">Przykład 2: Dodawanie/aktualizowanie znaczników do istniejącego VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2fa1b-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
                          Name          Value
                          ============  ============
                          testtagValue  SomeKeyValue
                          testtagKey    SomeTagKey
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="2fa1b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fa1b-112">PARAMETERS</span></span>

### <span data-ttu-id="2fa1b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fa1b-113">-AsJob</span></span>
<span data-ttu-id="2fa1b-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2fa1b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fa1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa1b-115">-DefaultProfile</span></span>
<span data-ttu-id="2fa1b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fa1b-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="2fa1b-117">-EnableBgp</span></span>
<span data-ttu-id="2fa1b-118">Czy sesja BGP ma być używana w tunelu VPN S2S</span><span class="sxs-lookup"><span data-stu-id="2fa1b-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fa1b-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="2fa1b-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="2fa1b-120">Limit czasu wykrywania nieaktywnych połączeń równorzędnych połączenia w sekundach</span><span class="sxs-lookup"><span data-stu-id="2fa1b-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fa1b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2fa1b-121">-Force</span></span>
<span data-ttu-id="2fa1b-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fa1b-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="2fa1b-123">-IpsecPolicies</span></span>
<span data-ttu-id="2fa1b-124">Lista zasad IPSec.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fa1b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2fa1b-125">-Tag</span></span>
<span data-ttu-id="2fa1b-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa1b-127">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="2fa1b-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="2fa1b-128">Lista zasad wyboru ruchu.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-128">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fa1b-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="2fa1b-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="2fa1b-130">Czy używać PrivateIP dla połączeń S2S</span><span class="sxs-lookup"><span data-stu-id="2fa1b-130">Whether to use PrivateIP for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa1b-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="2fa1b-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="2fa1b-132">Czy używać selektorów ruchu opartego na zasadach dla połączenia S2S</span><span class="sxs-lookup"><span data-stu-id="2fa1b-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa1b-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2fa1b-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="2fa1b-134">Określa obiekt PSVirtualNetworkGatewayConnection, którego używa polecenie cmdlet do modyfikowania połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fa1b-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2fa1b-135">-Confirm</span></span>
<span data-ttu-id="2fa1b-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa1b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa1b-137">-WhatIf</span></span>
<span data-ttu-id="2fa1b-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa1b-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa1b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa1b-140">CommonParameters</span></span>
<span data-ttu-id="2fa1b-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fa1b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa1b-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa1b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa1b-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fa1b-143">INPUTS</span></span>

### <span data-ttu-id="2fa1b-144">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2fa1b-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="2fa1b-145">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2fa1b-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2fa1b-146">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="2fa1b-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="2fa1b-147">Microsoft. Azure. Commands. Network. models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="2fa1b-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="2fa1b-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fa1b-148">OUTPUTS</span></span>

### <span data-ttu-id="2fa1b-149">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2fa1b-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2fa1b-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fa1b-150">NOTES</span></span>

## <span data-ttu-id="2fa1b-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fa1b-151">RELATED LINKS</span></span>

[<span data-ttu-id="2fa1b-152">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2fa1b-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2fa1b-153">Nowe — AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2fa1b-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2fa1b-154">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2fa1b-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


