---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 0c68886906957204ee0885a00bfc07740fb6ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717102"
---
# <span data-ttu-id="a652a-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a652a-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="a652a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a652a-102">SYNOPSIS</span></span>
<span data-ttu-id="a652a-103">Pobiera komunikację w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a652a-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a652a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a652a-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a652a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a652a-105">DESCRIPTION</span></span>
<span data-ttu-id="a652a-106">Polecenie cmdlet **Get-AzureRmVirtualNetworkPeering** pobiera komunikację między sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="a652a-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="a652a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a652a-107">EXAMPLES</span></span>

### <span data-ttu-id="a652a-108">Przykład 1: uzyskiwanie komunikacji równorzędnej między dwiema sieciami wirtualnymi</span><span class="sxs-lookup"><span data-stu-id="a652a-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="a652a-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a652a-109">PARAMETERS</span></span>

### <span data-ttu-id="a652a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a652a-110">-DefaultProfile</span></span>
<span data-ttu-id="a652a-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a652a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a652a-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a652a-112">-Name</span></span>
<span data-ttu-id="a652a-113">Określa nazwę elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a652a-113">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="a652a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a652a-114">-ResourceGroupName</span></span>
<span data-ttu-id="a652a-115">Określa nazwę grupy zasobów, do której należy element równorzędny sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a652a-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="a652a-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a652a-116">-VirtualNetworkName</span></span>
<span data-ttu-id="a652a-117">Określa nazwę sieci wirtualnej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a652a-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a652a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a652a-118">CommonParameters</span></span>
<span data-ttu-id="a652a-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a652a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a652a-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a652a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a652a-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a652a-121">INPUTS</span></span>

### <span data-ttu-id="a652a-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a652a-122">None</span></span>
<span data-ttu-id="a652a-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a652a-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a652a-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a652a-124">OUTPUTS</span></span>

### <span data-ttu-id="a652a-125">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a652a-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="a652a-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a652a-126">NOTES</span></span>

## <span data-ttu-id="a652a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a652a-127">RELATED LINKS</span></span>

[<span data-ttu-id="a652a-128">Dodaj-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a652a-128">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="a652a-129">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a652a-129">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="a652a-130">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a652a-130">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


