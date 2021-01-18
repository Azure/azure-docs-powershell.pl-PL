---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503189"
---
# <span data-ttu-id="76cf6-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="76cf6-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="76cf6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="76cf6-103">Modyfikuje obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="76cf6-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="76cf6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76cf6-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76cf6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76cf6-105">DESCRIPTION</span></span>
<span data-ttu-id="76cf6-106">Polecenie cmdlet **Set-AzExpressRouteCircuit** zapisuje zmodyfikowany obwód ExpressRoute na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="76cf6-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="76cf6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76cf6-107">EXAMPLES</span></span>

### <span data-ttu-id="76cf6-108">Przykład 1: Zmienianie ServiceKeyu obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="76cf6-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="76cf6-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76cf6-109">PARAMETERS</span></span>

### <span data-ttu-id="76cf6-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76cf6-110">-AsJob</span></span>
<span data-ttu-id="76cf6-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="76cf6-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76cf6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76cf6-112">-DefaultProfile</span></span>
<span data-ttu-id="76cf6-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76cf6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76cf6-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="76cf6-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="76cf6-115">Określa obiekt **ExpressRouteCircuit** , który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76cf6-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="76cf6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76cf6-116">CommonParameters</span></span>
<span data-ttu-id="76cf6-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76cf6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76cf6-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76cf6-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76cf6-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76cf6-119">INPUTS</span></span>

### <span data-ttu-id="76cf6-120">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="76cf6-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="76cf6-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76cf6-121">OUTPUTS</span></span>

### <span data-ttu-id="76cf6-122">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="76cf6-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="76cf6-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76cf6-123">NOTES</span></span>

## <span data-ttu-id="76cf6-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76cf6-124">RELATED LINKS</span></span>

[<span data-ttu-id="76cf6-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="76cf6-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="76cf6-126">Przenieś — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="76cf6-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="76cf6-127">Nowe — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="76cf6-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="76cf6-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="76cf6-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
