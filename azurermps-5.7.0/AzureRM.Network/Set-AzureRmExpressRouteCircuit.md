---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 71a6ec46cea6cc9d2ba6e6537797657b2124fe01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542523"
---
# <span data-ttu-id="d5c68-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5c68-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="d5c68-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5c68-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c68-103">Modyfikuje obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d5c68-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5c68-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5c68-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5c68-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5c68-105">DESCRIPTION</span></span>
<span data-ttu-id="d5c68-106">Polecenie cmdlet **Set-AzureRmExpressRouteCircuit** zapisuje zmodyfikowany obwód ExpressRoute na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c68-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="d5c68-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5c68-107">EXAMPLES</span></span>

### <span data-ttu-id="d5c68-108">Przykład 1: Zmienianie ServiceKeyu obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d5c68-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="d5c68-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5c68-109">PARAMETERS</span></span>

### <span data-ttu-id="d5c68-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5c68-110">-AsJob</span></span>
<span data-ttu-id="d5c68-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d5c68-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5c68-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c68-112">-DefaultProfile</span></span>
<span data-ttu-id="d5c68-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c68-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5c68-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5c68-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d5c68-115">Określa obiekt **ExpressRouteCircuit** , który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5c68-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d5c68-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c68-116">CommonParameters</span></span>
<span data-ttu-id="d5c68-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c68-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c68-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5c68-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c68-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5c68-119">INPUTS</span></span>

### <span data-ttu-id="d5c68-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5c68-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="d5c68-121">Parametr "ExpressRouteCircuit" akceptuje wartość typu "PSExpressRouteCircuit" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="d5c68-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="d5c68-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5c68-122">OUTPUTS</span></span>

### <span data-ttu-id="d5c68-123">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5c68-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d5c68-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5c68-124">NOTES</span></span>

## <span data-ttu-id="d5c68-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5c68-125">RELATED LINKS</span></span>

[<span data-ttu-id="d5c68-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5c68-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d5c68-127">Przenieś — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5c68-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d5c68-128">Nowe — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5c68-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d5c68-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d5c68-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
