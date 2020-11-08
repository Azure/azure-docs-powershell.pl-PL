---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220564"
---
# <span data-ttu-id="2eed9-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2eed9-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="2eed9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2eed9-102">SYNOPSIS</span></span>
<span data-ttu-id="2eed9-103">Pobiera komunikację w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2eed9-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="2eed9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2eed9-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eed9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2eed9-105">DESCRIPTION</span></span>
<span data-ttu-id="2eed9-106">Polecenie cmdlet **Get-AzVirtualNetworkPeering** pobiera komunikację między sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="2eed9-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="2eed9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2eed9-107">EXAMPLES</span></span>

### <span data-ttu-id="2eed9-108">Przykład 1: uzyskiwanie komunikacji równorzędnej między dwiema sieciami wirtualnymi</span><span class="sxs-lookup"><span data-stu-id="2eed9-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="2eed9-109">Przykład 2: pobieranie wszystkich elementów równorzędnych w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2eed9-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="2eed9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2eed9-110">PARAMETERS</span></span>

### <span data-ttu-id="2eed9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eed9-111">-DefaultProfile</span></span>
<span data-ttu-id="2eed9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2eed9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eed9-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2eed9-113">-Name</span></span>
<span data-ttu-id="2eed9-114">Określa nazwę elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2eed9-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="2eed9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eed9-115">-ResourceGroupName</span></span>
<span data-ttu-id="2eed9-116">Określa nazwę grupy zasobów, do której należy element równorzędny sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2eed9-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="2eed9-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2eed9-117">-VirtualNetworkName</span></span>
<span data-ttu-id="2eed9-118">Określa nazwę sieci wirtualnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eed9-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2eed9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eed9-119">CommonParameters</span></span>
<span data-ttu-id="2eed9-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eed9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eed9-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eed9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eed9-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2eed9-122">INPUTS</span></span>

### <span data-ttu-id="2eed9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2eed9-123">System.String</span></span>

## <span data-ttu-id="2eed9-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2eed9-124">OUTPUTS</span></span>

### <span data-ttu-id="2eed9-125">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2eed9-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="2eed9-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2eed9-126">NOTES</span></span>

## <span data-ttu-id="2eed9-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2eed9-127">RELATED LINKS</span></span>

[<span data-ttu-id="2eed9-128">Dodaj-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2eed9-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="2eed9-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2eed9-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="2eed9-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2eed9-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
