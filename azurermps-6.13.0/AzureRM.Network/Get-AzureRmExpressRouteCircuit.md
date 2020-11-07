---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 969d7c5f55d210cdff74066d08af50bbcc47181e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717397"
---
# <span data-ttu-id="2b4cd-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b4cd-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="2b4cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4cd-103">Pobiera obwód ExpressRoute platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2b4cd-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b4cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b4cd-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b4cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b4cd-105">DESCRIPTION</span></span>
<span data-ttu-id="2b4cd-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuit** służy do pobierania obiektu obwodu ExpressRoute z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2b4cd-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="2b4cd-107">Zwracany obiekt obwodu może być wykorzystywany jako wejście dla innych poleceń cmdlet, które działają na obwodach ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2b4cd-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="2b4cd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b4cd-108">EXAMPLES</span></span>

### <span data-ttu-id="2b4cd-109">Przykład 1: pobieranie obwodu ExpressRoute do usunięcia</span><span class="sxs-lookup"><span data-stu-id="2b4cd-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="2b4cd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b4cd-110">PARAMETERS</span></span>

### <span data-ttu-id="2b4cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b4cd-111">-DefaultProfile</span></span>
<span data-ttu-id="2b4cd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b4cd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b4cd-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b4cd-113">-Name</span></span>
<span data-ttu-id="2b4cd-114">Nazwa obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2b4cd-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4cd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b4cd-115">-ResourceGroupName</span></span>
<span data-ttu-id="2b4cd-116">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2b4cd-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4cd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4cd-117">CommonParameters</span></span>
<span data-ttu-id="2b4cd-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b4cd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4cd-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b4cd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4cd-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b4cd-120">INPUTS</span></span>

### <span data-ttu-id="2b4cd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2b4cd-121">System.String</span></span>

## <span data-ttu-id="2b4cd-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b4cd-122">OUTPUTS</span></span>

### <span data-ttu-id="2b4cd-123">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b4cd-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2b4cd-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b4cd-124">NOTES</span></span>

## <span data-ttu-id="2b4cd-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b4cd-125">RELATED LINKS</span></span>

[<span data-ttu-id="2b4cd-126">Przenieś — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b4cd-126">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2b4cd-127">Nowe — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b4cd-127">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2b4cd-128">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b4cd-128">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2b4cd-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2b4cd-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)