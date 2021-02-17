---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184642"
---
# <span data-ttu-id="b6eb4-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="b6eb4-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="b6eb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="b6eb4-103">To polecenie commandlet zwraca listę obsługiwanych marek urządzeń VPN, modeli i wersji oprogramowania układowego.</span><span class="sxs-lookup"><span data-stu-id="b6eb4-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="b6eb4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6eb4-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6eb4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="b6eb4-106">To polecenie commandlet zwraca listę obsługiwanych marek urządzeń VPN, modeli i wersji oprogramowania układowego.</span><span class="sxs-lookup"><span data-stu-id="b6eb4-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="b6eb4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6eb4-107">EXAMPLES</span></span>

### <span data-ttu-id="b6eb4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b6eb4-108">Example 1</span></span>
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

<span data-ttu-id="b6eb4-109">Zwraca listę obsługiwanych marek urządzeń SIECI VPN, modeli i wersji oprogramowania układowego:</span><span class="sxs-lookup"><span data-stu-id="b6eb4-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="b6eb4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6eb4-110">PARAMETERS</span></span>

### <span data-ttu-id="b6eb4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6eb4-111">-DefaultProfile</span></span>
<span data-ttu-id="b6eb4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6eb4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6eb4-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b6eb4-113">-Name</span></span>
<span data-ttu-id="b6eb4-114">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6eb4-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="b6eb4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6eb4-115">-ResourceGroupName</span></span>
<span data-ttu-id="b6eb4-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6eb4-116">The resource group name.</span></span>

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

### <span data-ttu-id="b6eb4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6eb4-117">CommonParameters</span></span>
<span data-ttu-id="b6eb4-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6eb4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6eb4-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6eb4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6eb4-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6eb4-120">INPUTS</span></span>

### <span data-ttu-id="b6eb4-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b6eb4-121">System.String</span></span>

## <span data-ttu-id="b6eb4-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6eb4-122">OUTPUTS</span></span>

### <span data-ttu-id="b6eb4-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b6eb4-123">System.String</span></span>

## <span data-ttu-id="b6eb4-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6eb4-124">NOTES</span></span>

## <span data-ttu-id="b6eb4-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6eb4-125">RELATED LINKS</span></span>
