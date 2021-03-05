---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 5648fe6049a7686d5f3930de6ea780598e2c0b06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970065"
---
# <span data-ttu-id="30c64-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="30c64-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="30c64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30c64-102">SYNOPSIS</span></span>
<span data-ttu-id="30c64-103">Pobiera komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="30c64-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="30c64-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="30c64-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30c64-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="30c64-105">DESCRIPTION</span></span>
<span data-ttu-id="30c64-106">Polecenie **cmdlet Get-AzVirtualNetworkPeering** pobiera połączenie równorzędne z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="30c64-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="30c64-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="30c64-107">EXAMPLES</span></span>

### <span data-ttu-id="30c64-108">Przykład 1. Uzyskiwanie komunikacji równorzędnej między dwiema sieciami wirtualnymi</span><span class="sxs-lookup"><span data-stu-id="30c64-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="30c64-109">Przykład 2. Uzyskiwanie wszystkich komunikacji równorzędnych w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="30c64-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="30c64-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30c64-110">PARAMETERS</span></span>

### <span data-ttu-id="30c64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c64-111">-DefaultProfile</span></span>
<span data-ttu-id="30c64-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="30c64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c64-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="30c64-113">-Name</span></span>
<span data-ttu-id="30c64-114">Określa nazwę komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="30c64-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="30c64-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c64-115">-ResourceGroupName</span></span>
<span data-ttu-id="30c64-116">Określa nazwę grupy zasobów, do której należy komunikacja równorzędna sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="30c64-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="30c64-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="30c64-117">-VirtualNetworkName</span></span>
<span data-ttu-id="30c64-118">Określa nazwę sieci wirtualnej, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30c64-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="30c64-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c64-119">CommonParameters</span></span>
<span data-ttu-id="30c64-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c64-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c64-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30c64-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c64-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30c64-122">INPUTS</span></span>

### <span data-ttu-id="30c64-123">System.String</span><span class="sxs-lookup"><span data-stu-id="30c64-123">System.String</span></span>

## <span data-ttu-id="30c64-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30c64-124">OUTPUTS</span></span>

### <span data-ttu-id="30c64-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="30c64-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="30c64-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="30c64-126">NOTES</span></span>

## <span data-ttu-id="30c64-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30c64-127">RELATED LINKS</span></span>

[<span data-ttu-id="30c64-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="30c64-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="30c64-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="30c64-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="30c64-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="30c64-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
