---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: f72d398eaea1d127ba600130fae3bbc690052332
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890830"
---
# <span data-ttu-id="bc5cd-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc5cd-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="bc5cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc5cd-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5cd-103">Pobiera obwód ExpressRoute platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bc5cd-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="bc5cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc5cd-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc5cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc5cd-105">DESCRIPTION</span></span>
<span data-ttu-id="bc5cd-106">Polecenie cmdlet **Get-AzExpressRouteCircuit** służy do pobierania obiektu obwodu ExpressRoute z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bc5cd-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="bc5cd-107">Zwracany obiekt obwodu może być wykorzystywany jako wejście dla innych poleceń cmdlet, które działają na obwodach ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bc5cd-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="bc5cd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc5cd-108">EXAMPLES</span></span>

### <span data-ttu-id="bc5cd-109">Przykład 1: pobieranie obwodu ExpressRoute do usunięcia</span><span class="sxs-lookup"><span data-stu-id="bc5cd-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="bc5cd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc5cd-110">PARAMETERS</span></span>

### <span data-ttu-id="bc5cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5cd-111">-DefaultProfile</span></span>
<span data-ttu-id="bc5cd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc5cd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc5cd-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc5cd-113">-Name</span></span>
<span data-ttu-id="bc5cd-114">Nazwa obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bc5cd-114">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="bc5cd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc5cd-115">-ResourceGroupName</span></span>
<span data-ttu-id="bc5cd-116">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bc5cd-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="bc5cd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5cd-117">CommonParameters</span></span>
<span data-ttu-id="bc5cd-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc5cd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5cd-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc5cd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5cd-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc5cd-120">INPUTS</span></span>

## <span data-ttu-id="bc5cd-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc5cd-121">OUTPUTS</span></span>

### <span data-ttu-id="bc5cd-122">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc5cd-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bc5cd-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc5cd-123">NOTES</span></span>

## <span data-ttu-id="bc5cd-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc5cd-124">RELATED LINKS</span></span>

[<span data-ttu-id="bc5cd-125">Przenieś — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc5cd-125">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="bc5cd-126">Nowe — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc5cd-126">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="bc5cd-127">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc5cd-127">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="bc5cd-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bc5cd-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
