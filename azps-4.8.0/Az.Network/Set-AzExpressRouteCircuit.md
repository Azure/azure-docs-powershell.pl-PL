---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223755"
---
# <span data-ttu-id="ae327-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ae327-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="ae327-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae327-102">SYNOPSIS</span></span>
<span data-ttu-id="ae327-103">Modyfikuje obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ae327-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ae327-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae327-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae327-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae327-105">DESCRIPTION</span></span>
<span data-ttu-id="ae327-106">Polecenie cmdlet **Set-AzExpressRouteCircuit** zapisuje zmodyfikowany obwód ExpressRoute na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ae327-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="ae327-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae327-107">EXAMPLES</span></span>

### <span data-ttu-id="ae327-108">Przykład 1: Zmienianie ServiceKeyu obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ae327-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="ae327-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae327-109">PARAMETERS</span></span>

### <span data-ttu-id="ae327-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae327-110">-AsJob</span></span>
<span data-ttu-id="ae327-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ae327-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae327-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae327-112">-DefaultProfile</span></span>
<span data-ttu-id="ae327-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae327-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae327-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ae327-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ae327-115">Określa obiekt **ExpressRouteCircuit** , który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae327-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ae327-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae327-116">CommonParameters</span></span>
<span data-ttu-id="ae327-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae327-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae327-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae327-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae327-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae327-119">INPUTS</span></span>

### <span data-ttu-id="ae327-120">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ae327-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ae327-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae327-121">OUTPUTS</span></span>

### <span data-ttu-id="ae327-122">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ae327-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ae327-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae327-123">NOTES</span></span>

## <span data-ttu-id="ae327-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae327-124">RELATED LINKS</span></span>

[<span data-ttu-id="ae327-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ae327-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ae327-126">Przenieś — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ae327-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="ae327-127">Nowe — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ae327-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="ae327-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ae327-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
