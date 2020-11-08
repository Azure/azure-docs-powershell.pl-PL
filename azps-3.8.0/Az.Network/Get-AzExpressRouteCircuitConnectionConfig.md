---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: f4aabb68fd1f508651406d7ccf7be91ff646d46c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052350"
---
# <span data-ttu-id="a130f-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a130f-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="a130f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a130f-102">SYNOPSIS</span></span>
<span data-ttu-id="a130f-103">Pobiera konfigurację połączenia obwodu ExpressRoute powiązaną z prywatnym elementem równorzędnym ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="a130f-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="a130f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a130f-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a130f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a130f-105">DESCRIPTION</span></span>
<span data-ttu-id="a130f-106">Polecenie cmdlet **Get-AzExpressRouteCircuitConnectionConfig** Pobiera konfigurację połączenia obwodu powiązanego z prywatnym łączem równorzędnym na obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a130f-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a130f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a130f-107">EXAMPLES</span></span>

### <span data-ttu-id="a130f-108">Przykład 1: Wyświetlanie konfiguracji połączenia obwodowego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a130f-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="a130f-109">Przykład 2: Pobieranie zasobu połączenia obwodowego skojarzonego ze obwodem ExpressRoute przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="a130f-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="a130f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a130f-110">PARAMETERS</span></span>

### <span data-ttu-id="a130f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a130f-111">-DefaultProfile</span></span>
<span data-ttu-id="a130f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a130f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a130f-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a130f-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a130f-114">Obiekt obwodu ExpressRoute zawierający konfigurację połączenia obwodowego.</span><span class="sxs-lookup"><span data-stu-id="a130f-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a130f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a130f-115">-Name</span></span>
<span data-ttu-id="a130f-116">Nazwa konfiguracji połączenia obwodowego, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="a130f-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a130f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a130f-117">CommonParameters</span></span>
<span data-ttu-id="a130f-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a130f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a130f-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a130f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a130f-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a130f-120">INPUTS</span></span>

### <span data-ttu-id="a130f-121">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a130f-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a130f-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a130f-122">OUTPUTS</span></span>

### <span data-ttu-id="a130f-123">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="a130f-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="a130f-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a130f-124">NOTES</span></span>

## <span data-ttu-id="a130f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a130f-125">RELATED LINKS</span></span>

[<span data-ttu-id="a130f-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a130f-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a130f-127">Dodaj-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a130f-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a130f-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a130f-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a130f-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a130f-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a130f-130">Nowe — AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a130f-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)