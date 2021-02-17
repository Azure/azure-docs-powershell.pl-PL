---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0adba1dfe453852b0797f40d6cd4d188db87169f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402001"
---
# <span data-ttu-id="2ea29-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2ea29-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="2ea29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ea29-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea29-103">Pobiera konfigurację połączenia obwodu usługi ExpressRoute skojarzoną z prywatną komunikacji równorzędnej usługi ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="2ea29-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="2ea29-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ea29-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ea29-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ea29-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea29-106">Polecenie **cmdlet Get-AzExpressRouteCircuitConnectionConfig** pobiera konfigurację połączenia obwodu skojarzonego z prywatną komunikacji równorzędnej dla obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2ea29-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2ea29-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ea29-107">EXAMPLES</span></span>

### <span data-ttu-id="2ea29-108">Przykład 1. Wyświetlanie konfiguracji połączenia obwodu dla obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2ea29-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="2ea29-109">Przykład 2. Uzyskiwanie zasobu połączenia obwodu skojarzonego z obwodem usługi ExpressRoute przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="2ea29-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="2ea29-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ea29-110">PARAMETERS</span></span>

### <span data-ttu-id="2ea29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea29-111">-DefaultProfile</span></span>
<span data-ttu-id="2ea29-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea29-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ea29-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ea29-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2ea29-114">Obiekt obwodu usługi ExpressRoute zawierający konfigurację połączenia obwodu.</span><span class="sxs-lookup"><span data-stu-id="2ea29-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="2ea29-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ea29-115">-Name</span></span>
<span data-ttu-id="2ea29-116">Nazwa konfiguracji połączenia obwodu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="2ea29-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="2ea29-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea29-117">CommonParameters</span></span>
<span data-ttu-id="2ea29-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea29-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea29-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ea29-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea29-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ea29-120">INPUTS</span></span>

### <span data-ttu-id="2ea29-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ea29-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2ea29-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ea29-122">OUTPUTS</span></span>

### <span data-ttu-id="2ea29-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="2ea29-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="2ea29-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ea29-124">NOTES</span></span>

## <span data-ttu-id="2ea29-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ea29-125">RELATED LINKS</span></span>

[<span data-ttu-id="2ea29-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2ea29-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="2ea29-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2ea29-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="2ea29-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2ea29-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)




