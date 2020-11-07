---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 0ff95b3e212e61b3d8c9d01b0ad745963d7b24e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709434"
---
# <span data-ttu-id="e5c34-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="e5c34-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="e5c34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5c34-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c34-103">Ta unifiedgroup zwraca listę obsługiwanych marek, modeli i wersji oprogramowania sprzętowego sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="e5c34-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="e5c34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5c34-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5c34-105">DESCRIPTION</span></span>
<span data-ttu-id="e5c34-106">Ta unifiedgroup zwraca listę obsługiwanych marek, modeli i wersji oprogramowania sprzętowego sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="e5c34-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="e5c34-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5c34-107">EXAMPLES</span></span>

### <span data-ttu-id="e5c34-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5c34-108">Example 1</span></span>
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

<span data-ttu-id="e5c34-109">Zwraca listę obsługiwanych marek urządzeń VPN, modeli i wersji oprogramowania układowego:</span><span class="sxs-lookup"><span data-stu-id="e5c34-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="e5c34-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5c34-110">PARAMETERS</span></span>

### <span data-ttu-id="e5c34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c34-111">-DefaultProfile</span></span>
<span data-ttu-id="e5c34-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5c34-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e5c34-113">-Name</span></span>
<span data-ttu-id="e5c34-114">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e5c34-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="e5c34-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c34-115">-ResourceGroupName</span></span>
<span data-ttu-id="e5c34-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e5c34-116">The resource group name.</span></span>

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

### <span data-ttu-id="e5c34-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c34-117">CommonParameters</span></span>
<span data-ttu-id="e5c34-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c34-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c34-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5c34-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c34-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5c34-120">INPUTS</span></span>

### <span data-ttu-id="e5c34-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e5c34-121">System.String</span></span>

## <span data-ttu-id="e5c34-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5c34-122">OUTPUTS</span></span>

### <span data-ttu-id="e5c34-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e5c34-123">System.String</span></span>

## <span data-ttu-id="e5c34-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5c34-124">NOTES</span></span>

## <span data-ttu-id="e5c34-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5c34-125">RELATED LINKS</span></span>