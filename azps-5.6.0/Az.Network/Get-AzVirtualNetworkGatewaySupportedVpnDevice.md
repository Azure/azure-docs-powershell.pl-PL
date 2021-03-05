---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 45cb703d6fdc87238f4d1ed35ada90aadeed501b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987806"
---
# <span data-ttu-id="f1cc7-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="f1cc7-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="f1cc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cc7-103">To polecenie commandlet zwraca listę obsługiwanych marek urządzeń VPN, modeli i wersji oprogramowania układowego.</span><span class="sxs-lookup"><span data-stu-id="f1cc7-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="f1cc7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1cc7-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1cc7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1cc7-105">DESCRIPTION</span></span>
<span data-ttu-id="f1cc7-106">To polecenie commandlet zwraca listę obsługiwanych marek urządzeń VPN, modeli i wersji oprogramowania układowego.</span><span class="sxs-lookup"><span data-stu-id="f1cc7-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="f1cc7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1cc7-107">EXAMPLES</span></span>

### <span data-ttu-id="f1cc7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f1cc7-108">Example 1</span></span>
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

<span data-ttu-id="f1cc7-109">Zwraca listę obsługiwanych marek urządzeń SIECI VPN, modeli i wersji oprogramowania układowego:</span><span class="sxs-lookup"><span data-stu-id="f1cc7-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="f1cc7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1cc7-110">PARAMETERS</span></span>

### <span data-ttu-id="f1cc7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cc7-111">-DefaultProfile</span></span>
<span data-ttu-id="f1cc7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1cc7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1cc7-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f1cc7-113">-Name</span></span>
<span data-ttu-id="f1cc7-114">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f1cc7-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="f1cc7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1cc7-115">-ResourceGroupName</span></span>
<span data-ttu-id="f1cc7-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f1cc7-116">The resource group name.</span></span>

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

### <span data-ttu-id="f1cc7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cc7-117">CommonParameters</span></span>
<span data-ttu-id="f1cc7-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1cc7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cc7-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1cc7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cc7-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1cc7-120">INPUTS</span></span>

### <span data-ttu-id="f1cc7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f1cc7-121">System.String</span></span>

## <span data-ttu-id="f1cc7-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1cc7-122">OUTPUTS</span></span>

### <span data-ttu-id="f1cc7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f1cc7-123">System.String</span></span>

## <span data-ttu-id="f1cc7-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1cc7-124">NOTES</span></span>

## <span data-ttu-id="f1cc7-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1cc7-125">RELATED LINKS</span></span>
