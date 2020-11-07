---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 75725505e7c5239f1b5dc8f05d4cdfe3cf2b4903
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890634"
---
# <span data-ttu-id="3a23c-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="3a23c-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="3a23c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a23c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a23c-103">Pobiera komunikację w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a23c-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="3a23c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a23c-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a23c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a23c-105">DESCRIPTION</span></span>
<span data-ttu-id="3a23c-106">Polecenie cmdlet **Get-AzVirtualNetworkPeering** pobiera komunikację między sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="3a23c-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="3a23c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a23c-107">EXAMPLES</span></span>

### <span data-ttu-id="3a23c-108">Przykład 1: uzyskiwanie komunikacji równorzędnej między dwiema sieciami wirtualnymi</span><span class="sxs-lookup"><span data-stu-id="3a23c-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="3a23c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a23c-109">PARAMETERS</span></span>

### <span data-ttu-id="3a23c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a23c-110">-DefaultProfile</span></span>
<span data-ttu-id="3a23c-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a23c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a23c-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a23c-112">-Name</span></span>
<span data-ttu-id="3a23c-113">Określa nazwę elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a23c-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a23c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a23c-114">-ResourceGroupName</span></span>
<span data-ttu-id="3a23c-115">Określa nazwę grupy zasobów, do której należy element równorzędny sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a23c-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a23c-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3a23c-116">-VirtualNetworkName</span></span>
<span data-ttu-id="3a23c-117">Określa nazwę sieci wirtualnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a23c-117">Specifies the virtual network name that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a23c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a23c-118">CommonParameters</span></span>
<span data-ttu-id="3a23c-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a23c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a23c-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a23c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a23c-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a23c-121">INPUTS</span></span>

## <span data-ttu-id="3a23c-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a23c-122">OUTPUTS</span></span>

### <span data-ttu-id="3a23c-123">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="3a23c-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="3a23c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a23c-124">NOTES</span></span>

## <span data-ttu-id="3a23c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a23c-125">RELATED LINKS</span></span>

[<span data-ttu-id="3a23c-126">Dodaj-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="3a23c-126">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="3a23c-127">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="3a23c-127">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="3a23c-128">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="3a23c-128">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


