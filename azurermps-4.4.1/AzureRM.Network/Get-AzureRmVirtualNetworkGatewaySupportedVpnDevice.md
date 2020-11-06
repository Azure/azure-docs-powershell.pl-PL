---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f66765d69cb6d9d626322446223aa5f94ff94eac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527437"
---
# <span data-ttu-id="eb92d-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="eb92d-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="eb92d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb92d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb92d-103">Ta unifiedgroup zwraca listę obsługiwanych marek, modeli i wersji oprogramowania sprzętowego sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="eb92d-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb92d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb92d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb92d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb92d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb92d-106">Ta unifiedgroup zwraca listę obsługiwanych marek, modeli i wersji oprogramowania sprzętowego sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="eb92d-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="eb92d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb92d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb92d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eb92d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="eb92d-109">Zwraca listę obsługiwanych marek urządzeń VPN, modeli i wersji oprogramowania układowego:</span><span class="sxs-lookup"><span data-stu-id="eb92d-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="eb92d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb92d-110">PARAMETERS</span></span>

### <span data-ttu-id="eb92d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb92d-111">-DefaultProfile</span></span>
<span data-ttu-id="eb92d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb92d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb92d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eb92d-113">-Name</span></span>
<span data-ttu-id="eb92d-114">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eb92d-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="eb92d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb92d-115">-ResourceGroupName</span></span>
<span data-ttu-id="eb92d-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eb92d-116">The resource group name.</span></span>

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

### <span data-ttu-id="eb92d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb92d-117">CommonParameters</span></span>
<span data-ttu-id="eb92d-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb92d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb92d-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb92d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb92d-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb92d-120">INPUTS</span></span>

### <span data-ttu-id="eb92d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="eb92d-121">System.String</span></span>

## <span data-ttu-id="eb92d-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb92d-122">OUTPUTS</span></span>

### <span data-ttu-id="eb92d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="eb92d-123">System.String</span></span>

## <span data-ttu-id="eb92d-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb92d-124">NOTES</span></span>

## <span data-ttu-id="eb92d-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb92d-125">RELATED LINKS</span></span>

