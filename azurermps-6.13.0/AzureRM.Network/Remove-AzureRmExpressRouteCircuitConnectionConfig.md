---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 6524e69662f26a993bbc9cdf74eba71ff801f879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543644"
---
# <span data-ttu-id="58174-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="58174-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="58174-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58174-102">SYNOPSIS</span></span>
<span data-ttu-id="58174-103">Usuwa konfigurację połączenia obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="58174-103">Removes an ExpressRoute circuit connection configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58174-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58174-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String>
 [-ExpressRouteCircuit] <PSExpressRouteCircuit> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58174-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58174-105">DESCRIPTION</span></span>
<span data-ttu-id="58174-106">Polecenie cmdlet **Remove-AzureRmExpressRouteCircuitConnectionConfig** usuwa konfigurację połączenia obwodu ExpressRoute skojarzoną z danym obwodem usługi Express Route.</span><span class="sxs-lookup"><span data-stu-id="58174-106">The **Remove-AzureRmExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="58174-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58174-107">EXAMPLES</span></span>

### <span data-ttu-id="58174-108">Przykład 1: Usuwanie konfiguracji połączenia obwodowego ze obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="58174-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="58174-109">Przykład 2: Usuwanie konfiguracji połączenia obwodowego przy użyciu instalacji rurowej ze obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="58174-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="58174-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58174-110">PARAMETERS</span></span>

### <span data-ttu-id="58174-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58174-111">-DefaultProfile</span></span>
<span data-ttu-id="58174-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58174-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58174-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="58174-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="58174-114">Obwód ExpressRoute zawierający konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="58174-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="58174-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58174-115">-Name</span></span>
<span data-ttu-id="58174-116">Nazwa konfiguracji połączenia obwodowego, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="58174-116">The name of the circuit connection configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58174-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58174-117">-Confirm</span></span>
<span data-ttu-id="58174-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58174-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58174-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58174-119">-WhatIf</span></span>
<span data-ttu-id="58174-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58174-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58174-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58174-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58174-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58174-122">CommonParameters</span></span>
<span data-ttu-id="58174-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58174-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58174-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58174-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58174-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58174-125">INPUTS</span></span>

### <span data-ttu-id="58174-126">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="58174-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="58174-127">Parametry: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="58174-127">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="58174-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58174-128">OUTPUTS</span></span>

### <span data-ttu-id="58174-129">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="58174-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="58174-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58174-130">NOTES</span></span>

## <span data-ttu-id="58174-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58174-131">RELATED LINKS</span></span>

[<span data-ttu-id="58174-132">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="58174-132">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="58174-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="58174-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="58174-134">Dodaj-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="58174-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="58174-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="58174-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="58174-136">Nowe — AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="58174-136">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="58174-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="58174-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="58174-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="58174-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
