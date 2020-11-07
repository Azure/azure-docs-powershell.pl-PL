---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: cf15d39a8c1ec320b45e488ccaac7903c82e30f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897966"
---
# <span data-ttu-id="6a62b-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a62b-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="6a62b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a62b-102">SYNOPSIS</span></span>
<span data-ttu-id="6a62b-103">Pobiera obwód ExpressRoute platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6a62b-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a62b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a62b-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a62b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a62b-105">DESCRIPTION</span></span>
<span data-ttu-id="6a62b-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuit** służy do pobierania obiektu obwodu ExpressRoute z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6a62b-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="6a62b-107">Zwracany obiekt obwodu może być wykorzystywany jako wejście dla innych poleceń cmdlet, które działają na obwodach ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a62b-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="6a62b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a62b-108">EXAMPLES</span></span>

### <span data-ttu-id="6a62b-109">Przykład 1: pobieranie obwodu ExpressRoute do usunięcia</span><span class="sxs-lookup"><span data-stu-id="6a62b-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="6a62b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a62b-110">PARAMETERS</span></span>

### <span data-ttu-id="6a62b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a62b-111">-DefaultProfile</span></span>
<span data-ttu-id="6a62b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a62b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a62b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a62b-113">-Name</span></span>
<span data-ttu-id="6a62b-114">Nazwa obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a62b-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a62b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a62b-115">-ResourceGroupName</span></span>
<span data-ttu-id="6a62b-116">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a62b-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="6a62b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a62b-117">CommonParameters</span></span>
<span data-ttu-id="6a62b-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a62b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a62b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a62b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a62b-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a62b-120">INPUTS</span></span>

## <span data-ttu-id="6a62b-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a62b-121">OUTPUTS</span></span>

### <span data-ttu-id="6a62b-122">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a62b-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="6a62b-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a62b-123">NOTES</span></span>

## <span data-ttu-id="6a62b-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a62b-124">RELATED LINKS</span></span>

[<span data-ttu-id="6a62b-125">Przenieś — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a62b-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6a62b-126">Nowe — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a62b-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6a62b-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a62b-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6a62b-128">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a62b-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
