---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 262dd4333b2490c5035a00de179b9b2092ccb71e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892805"
---
# <span data-ttu-id="52375-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52375-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="52375-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52375-102">SYNOPSIS</span></span>
<span data-ttu-id="52375-103">Modyfikuje obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="52375-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="52375-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52375-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52375-105">Opis</span><span class="sxs-lookup"><span data-stu-id="52375-105">DESCRIPTION</span></span>
<span data-ttu-id="52375-106">Polecenie cmdlet **Set-AzExpressRouteCircuit** zapisuje zmodyfikowany obwód ExpressRoute na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="52375-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="52375-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52375-107">EXAMPLES</span></span>

### <span data-ttu-id="52375-108">Przykład 1: Zmienianie ServiceKeyu obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="52375-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="52375-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52375-109">PARAMETERS</span></span>

### <span data-ttu-id="52375-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52375-110">-AsJob</span></span>
<span data-ttu-id="52375-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="52375-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52375-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52375-112">-DefaultProfile</span></span>
<span data-ttu-id="52375-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="52375-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52375-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52375-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="52375-115">Określa obiekt **ExpressRouteCircuit** , który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52375-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52375-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52375-116">CommonParameters</span></span>
<span data-ttu-id="52375-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52375-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52375-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52375-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52375-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52375-119">INPUTS</span></span>

### <span data-ttu-id="52375-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52375-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="52375-121">Parametr "ExpressRouteCircuit" akceptuje wartość typu "PSExpressRouteCircuit" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="52375-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="52375-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52375-122">OUTPUTS</span></span>

### <span data-ttu-id="52375-123">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52375-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="52375-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52375-124">NOTES</span></span>

## <span data-ttu-id="52375-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52375-125">RELATED LINKS</span></span>

[<span data-ttu-id="52375-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52375-126">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="52375-127">Przenieś — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52375-127">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="52375-128">Nowe — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52375-128">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="52375-129">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52375-129">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
