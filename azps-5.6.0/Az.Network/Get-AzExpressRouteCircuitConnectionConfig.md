---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c8d35373c2891b9f0d3ac76ded8b4e9808f32f33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993819"
---
# <span data-ttu-id="74fe5-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="74fe5-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="74fe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="74fe5-103">Pobiera konfigurację połączenia obwodu usługi ExpressRoute skojarzoną z prywatną komunikacji równorzędnej usługi ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="74fe5-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="74fe5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74fe5-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74fe5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="74fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="74fe5-106">Polecenie **cmdlet Get-AzExpressRouteCircuitConnectionConfig** pobiera konfigurację połączenia obwodu skojarzonego z prywatną komunikacji równorzędnej dla obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="74fe5-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="74fe5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74fe5-107">EXAMPLES</span></span>

### <span data-ttu-id="74fe5-108">Przykład 1. Wyświetlanie konfiguracji połączenia obwodu dla obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="74fe5-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="74fe5-109">Przykład 2. Uzyskiwanie zasobu połączenia obwodu skojarzonego z obwodem usługi ExpressRoute przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="74fe5-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="74fe5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74fe5-110">PARAMETERS</span></span>

### <span data-ttu-id="74fe5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fe5-111">-DefaultProfile</span></span>
<span data-ttu-id="74fe5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74fe5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74fe5-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="74fe5-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="74fe5-114">Obiekt obwodu usługi ExpressRoute zawierający konfigurację połączenia obwodu.</span><span class="sxs-lookup"><span data-stu-id="74fe5-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="74fe5-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74fe5-115">-Name</span></span>
<span data-ttu-id="74fe5-116">Nazwa konfiguracji połączenia obwodu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="74fe5-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="74fe5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fe5-117">CommonParameters</span></span>
<span data-ttu-id="74fe5-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74fe5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fe5-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74fe5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fe5-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74fe5-120">INPUTS</span></span>

### <span data-ttu-id="74fe5-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="74fe5-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="74fe5-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74fe5-122">OUTPUTS</span></span>

### <span data-ttu-id="74fe5-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="74fe5-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="74fe5-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74fe5-124">NOTES</span></span>

## <span data-ttu-id="74fe5-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74fe5-125">RELATED LINKS</span></span>

[<span data-ttu-id="74fe5-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="74fe5-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="74fe5-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="74fe5-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="74fe5-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="74fe5-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="74fe5-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="74fe5-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="74fe5-130">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="74fe5-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)