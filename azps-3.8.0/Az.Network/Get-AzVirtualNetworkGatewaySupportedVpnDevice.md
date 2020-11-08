---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050631"
---
# <span data-ttu-id="6b16b-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="6b16b-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="6b16b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b16b-102">SYNOPSIS</span></span>
<span data-ttu-id="6b16b-103">Ta unifiedgroup zwraca listę obsługiwanych marek, modeli i wersji oprogramowania sprzętowego sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="6b16b-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="6b16b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b16b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b16b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6b16b-105">DESCRIPTION</span></span>
<span data-ttu-id="6b16b-106">Ta unifiedgroup zwraca listę obsługiwanych marek, modeli i wersji oprogramowania sprzętowego sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="6b16b-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="6b16b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b16b-107">EXAMPLES</span></span>

### <span data-ttu-id="6b16b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6b16b-108">Example 1</span></span>
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

<span data-ttu-id="6b16b-109">Zwraca listę obsługiwanych marek urządzeń VPN, modeli i wersji oprogramowania układowego:</span><span class="sxs-lookup"><span data-stu-id="6b16b-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="6b16b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b16b-110">PARAMETERS</span></span>

### <span data-ttu-id="6b16b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b16b-111">-DefaultProfile</span></span>
<span data-ttu-id="6b16b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b16b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b16b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b16b-113">-Name</span></span>
<span data-ttu-id="6b16b-114">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6b16b-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="6b16b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b16b-115">-ResourceGroupName</span></span>
<span data-ttu-id="6b16b-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b16b-116">The resource group name.</span></span>

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

### <span data-ttu-id="6b16b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b16b-117">CommonParameters</span></span>
<span data-ttu-id="6b16b-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b16b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b16b-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b16b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b16b-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b16b-120">INPUTS</span></span>

### <span data-ttu-id="6b16b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6b16b-121">System.String</span></span>

## <span data-ttu-id="6b16b-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b16b-122">OUTPUTS</span></span>

### <span data-ttu-id="6b16b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6b16b-123">System.String</span></span>

## <span data-ttu-id="6b16b-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b16b-124">NOTES</span></span>

## <span data-ttu-id="6b16b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b16b-125">RELATED LINKS</span></span>
