---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380989"
---
# <span data-ttu-id="2a259-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="2a259-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="2a259-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a259-102">SYNOPSIS</span></span>
<span data-ttu-id="2a259-103">Ta unifiedgroup zwraca listę obsługiwanych marek, modeli i wersji oprogramowania sprzętowego sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="2a259-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="2a259-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a259-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a259-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a259-105">DESCRIPTION</span></span>
<span data-ttu-id="2a259-106">Ta unifiedgroup zwraca listę obsługiwanych marek, modeli i wersji oprogramowania sprzętowego sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="2a259-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="2a259-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a259-107">EXAMPLES</span></span>

### <span data-ttu-id="2a259-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a259-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="2a259-109">Zwraca listę obsługiwanych marek urządzeń VPN, modeli i wersji oprogramowania układowego:</span><span class="sxs-lookup"><span data-stu-id="2a259-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="2a259-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a259-110">PARAMETERS</span></span>

### <span data-ttu-id="2a259-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a259-111">-DefaultProfile</span></span>
<span data-ttu-id="2a259-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a259-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a259-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a259-113">-Name</span></span>
<span data-ttu-id="2a259-114">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2a259-114">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a259-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a259-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a259-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a259-116">The resource group name.</span></span>

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

### <span data-ttu-id="2a259-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a259-117">CommonParameters</span></span>
<span data-ttu-id="2a259-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a259-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a259-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a259-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a259-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a259-120">INPUTS</span></span>

### <span data-ttu-id="2a259-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2a259-121">System.String</span></span>

## <span data-ttu-id="2a259-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a259-122">OUTPUTS</span></span>

### <span data-ttu-id="2a259-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2a259-123">System.String</span></span>

## <span data-ttu-id="2a259-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a259-124">NOTES</span></span>

## <span data-ttu-id="2a259-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a259-125">RELATED LINKS</span></span>
