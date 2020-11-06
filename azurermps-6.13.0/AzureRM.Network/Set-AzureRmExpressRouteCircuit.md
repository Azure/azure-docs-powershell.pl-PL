---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 8ef7121e057759a6fbdb341d9d6bc137692a36cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554039"
---
# <span data-ttu-id="c3641-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3641-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="c3641-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3641-102">SYNOPSIS</span></span>
<span data-ttu-id="c3641-103">Modyfikuje obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c3641-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3641-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3641-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3641-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3641-105">DESCRIPTION</span></span>
<span data-ttu-id="c3641-106">Polecenie cmdlet **Set-AzureRmExpressRouteCircuit** zapisuje zmodyfikowany obwód ExpressRoute na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c3641-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="c3641-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3641-107">EXAMPLES</span></span>

### <span data-ttu-id="c3641-108">Przykład 1: Zmienianie ServiceKeyu obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c3641-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="c3641-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3641-109">PARAMETERS</span></span>

### <span data-ttu-id="c3641-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3641-110">-AsJob</span></span>
<span data-ttu-id="c3641-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c3641-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3641-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3641-112">-DefaultProfile</span></span>
<span data-ttu-id="c3641-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3641-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3641-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3641-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c3641-115">Określa obiekt **ExpressRouteCircuit** , który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3641-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3641-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3641-116">CommonParameters</span></span>
<span data-ttu-id="c3641-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3641-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3641-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3641-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3641-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3641-119">INPUTS</span></span>

### <span data-ttu-id="c3641-120">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3641-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="c3641-121">Parametry: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3641-121">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="c3641-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3641-122">OUTPUTS</span></span>

### <span data-ttu-id="c3641-123">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3641-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c3641-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3641-124">NOTES</span></span>

## <span data-ttu-id="c3641-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3641-125">RELATED LINKS</span></span>

[<span data-ttu-id="c3641-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3641-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c3641-127">Przenieś — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3641-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c3641-128">Nowe — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3641-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c3641-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c3641-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
