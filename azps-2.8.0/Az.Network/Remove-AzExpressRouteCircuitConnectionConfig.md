---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bf69b628224baa74014d75b4c687a15d830d13c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869747"
---
# <span data-ttu-id="c43b0-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c43b0-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="c43b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c43b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c43b0-103">Usuwa konfigurację połączenia obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c43b0-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="c43b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c43b0-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c43b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c43b0-105">DESCRIPTION</span></span>
<span data-ttu-id="c43b0-106">Polecenie cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** usuwa konfigurację połączenia obwodu ExpressRoute skojarzoną z danym obwodem usługi Express Route.</span><span class="sxs-lookup"><span data-stu-id="c43b0-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="c43b0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c43b0-107">EXAMPLES</span></span>

### <span data-ttu-id="c43b0-108">Przykład 1: Usuwanie konfiguracji połączenia obwodowego ze obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c43b0-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="c43b0-109">Przykład 2: Usuwanie konfiguracji połączenia obwodowego przy użyciu instalacji rurowej ze obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c43b0-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="c43b0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c43b0-110">PARAMETERS</span></span>

### <span data-ttu-id="c43b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43b0-111">-DefaultProfile</span></span>
<span data-ttu-id="c43b0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c43b0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c43b0-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c43b0-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c43b0-114">Obwód ExpressRoute zawierający konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c43b0-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="c43b0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c43b0-115">-Name</span></span>
<span data-ttu-id="c43b0-116">Nazwa konfiguracji połączenia obwodowego, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="c43b0-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="c43b0-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c43b0-117">-Confirm</span></span>
<span data-ttu-id="c43b0-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c43b0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c43b0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c43b0-119">-WhatIf</span></span>
<span data-ttu-id="c43b0-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c43b0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c43b0-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c43b0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c43b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43b0-122">CommonParameters</span></span>
<span data-ttu-id="c43b0-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c43b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43b0-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c43b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43b0-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c43b0-125">INPUTS</span></span>

### <span data-ttu-id="c43b0-126">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c43b0-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c43b0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c43b0-127">OUTPUTS</span></span>

### <span data-ttu-id="c43b0-128">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c43b0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c43b0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c43b0-129">NOTES</span></span>

## <span data-ttu-id="c43b0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c43b0-130">RELATED LINKS</span></span>

[<span data-ttu-id="c43b0-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c43b0-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c43b0-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c43b0-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c43b0-133">Dodaj-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c43b0-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c43b0-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c43b0-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c43b0-135">Nowe — AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c43b0-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c43b0-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c43b0-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="c43b0-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c43b0-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)