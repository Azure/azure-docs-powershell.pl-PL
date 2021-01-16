---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490973"
---
# <span data-ttu-id="22e2c-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="22e2c-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="22e2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="22e2c-103">Tworzenie zewnętrznej konfiguracji serwera usługi RADIUS</span><span class="sxs-lookup"><span data-stu-id="22e2c-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="22e2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22e2c-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22e2c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22e2c-105">DESCRIPTION</span></span>
<span data-ttu-id="22e2c-106">Polecenie cmdlet New-AzRadiusServer powoduje utworzenie zewnętrznej konfiguracji serwera RADIUS, która będzie używana w konfiguracji bramy sieci wirtualnej i serwera sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="22e2c-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="22e2c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22e2c-107">EXAMPLES</span></span>

### <span data-ttu-id="22e2c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22e2c-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="22e2c-109">Tworzenie wielu zewnętrznych konfiguracji serwera RADIUS, które będą używane do konfigurowania P2S w nowej bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22e2c-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="22e2c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22e2c-110">PARAMETERS</span></span>

### <span data-ttu-id="22e2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e2c-111">-DefaultProfile</span></span>
<span data-ttu-id="22e2c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22e2c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22e2c-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="22e2c-113">-RadiusServerAddress</span></span>
<span data-ttu-id="22e2c-114">Adres zewnętrznego serwera RADIUS</span><span class="sxs-lookup"><span data-stu-id="22e2c-114">External radius server address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e2c-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="22e2c-115">-RadiusServerScore</span></span>
<span data-ttu-id="22e2c-116">Wynik zewnętrznego serwera RADIUS</span><span class="sxs-lookup"><span data-stu-id="22e2c-116">External radius server score</span></span>

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

### <span data-ttu-id="22e2c-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="22e2c-117">-RadiusServerSecret</span></span>
<span data-ttu-id="22e2c-118">Klucz tajny zewnętrznego serwera RADIUS</span><span class="sxs-lookup"><span data-stu-id="22e2c-118">External radius server secret</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e2c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e2c-119">CommonParameters</span></span>
<span data-ttu-id="22e2c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e2c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e2c-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22e2c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e2c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22e2c-122">INPUTS</span></span>

### <span data-ttu-id="22e2c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="22e2c-123">System.String</span></span>

### <span data-ttu-id="22e2c-124">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="22e2c-124">System.Security.SecureString</span></span>

### <span data-ttu-id="22e2c-125">System. Int32</span><span class="sxs-lookup"><span data-stu-id="22e2c-125">System.Int32</span></span>

## <span data-ttu-id="22e2c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22e2c-126">OUTPUTS</span></span>

### <span data-ttu-id="22e2c-127">Microsoft. Azure. Commands. Network. models. PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="22e2c-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="22e2c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22e2c-128">NOTES</span></span>

## <span data-ttu-id="22e2c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22e2c-129">RELATED LINKS</span></span>
