---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050345"
---
# <span data-ttu-id="0058f-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0058f-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="0058f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0058f-102">SYNOPSIS</span></span>
<span data-ttu-id="0058f-103">Pobiera komunikację w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0058f-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="0058f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0058f-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0058f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0058f-105">DESCRIPTION</span></span>
<span data-ttu-id="0058f-106">Polecenie cmdlet **Get-AzVirtualNetworkPeering** pobiera komunikację między sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="0058f-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="0058f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0058f-107">EXAMPLES</span></span>

### <span data-ttu-id="0058f-108">Przykład 1: uzyskiwanie komunikacji równorzędnej między dwiema sieciami wirtualnymi</span><span class="sxs-lookup"><span data-stu-id="0058f-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="0058f-109">Przykład 2: pobieranie wszystkich elementów równorzędnych w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0058f-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="0058f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0058f-110">PARAMETERS</span></span>

### <span data-ttu-id="0058f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0058f-111">-DefaultProfile</span></span>
<span data-ttu-id="0058f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0058f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0058f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0058f-113">-Name</span></span>
<span data-ttu-id="0058f-114">Określa nazwę elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0058f-114">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0058f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0058f-115">-ResourceGroupName</span></span>
<span data-ttu-id="0058f-116">Określa nazwę grupy zasobów, do której należy element równorzędny sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0058f-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="0058f-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0058f-117">-VirtualNetworkName</span></span>
<span data-ttu-id="0058f-118">Określa nazwę sieci wirtualnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0058f-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0058f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0058f-119">CommonParameters</span></span>
<span data-ttu-id="0058f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0058f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0058f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0058f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0058f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0058f-122">INPUTS</span></span>

### <span data-ttu-id="0058f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0058f-123">System.String</span></span>

## <span data-ttu-id="0058f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0058f-124">OUTPUTS</span></span>

### <span data-ttu-id="0058f-125">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0058f-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="0058f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0058f-126">NOTES</span></span>

## <span data-ttu-id="0058f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0058f-127">RELATED LINKS</span></span>

[<span data-ttu-id="0058f-128">Dodaj-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0058f-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="0058f-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0058f-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="0058f-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0058f-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
