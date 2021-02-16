---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: cf854be6ed6dd5a69ba730cf6da60884a493551e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412388"
---
# <span data-ttu-id="79223-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="79223-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="79223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79223-102">SYNOPSIS</span></span>
<span data-ttu-id="79223-103">Usuwa konfigurację połączenia obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="79223-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="79223-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79223-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79223-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="79223-105">DESCRIPTION</span></span>
<span data-ttu-id="79223-106">Polecenie **cmdlet Remove-AzExpressRouteCircuitConnectionConfig** usuwa konfigurację połączenia obwodu usługi ExpressRoute skojarzoną z danym obwodem trasy expressowej.</span><span class="sxs-lookup"><span data-stu-id="79223-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="79223-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79223-107">EXAMPLES</span></span>

### <span data-ttu-id="79223-108">Przykład 1. Usuwanie konfiguracji połączenia obwodu z obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="79223-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="79223-109">Przykład 2. Usuwanie konfiguracji połączenia obwodu za pomocą połączeń rurowych z obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="79223-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="79223-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79223-110">PARAMETERS</span></span>

### <span data-ttu-id="79223-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79223-111">-DefaultProfile</span></span>
<span data-ttu-id="79223-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79223-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79223-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="79223-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="79223-114">Obwód usługi ExpressRoute zawierający konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="79223-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="79223-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="79223-115">-Name</span></span>
<span data-ttu-id="79223-116">Nazwa konfiguracji połączenia obwodu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="79223-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="79223-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79223-117">-Confirm</span></span>
<span data-ttu-id="79223-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="79223-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79223-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79223-119">-WhatIf</span></span>
<span data-ttu-id="79223-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79223-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79223-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="79223-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79223-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79223-122">CommonParameters</span></span>
<span data-ttu-id="79223-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79223-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79223-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79223-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79223-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79223-125">INPUTS</span></span>

### <span data-ttu-id="79223-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="79223-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="79223-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79223-127">OUTPUTS</span></span>

### <span data-ttu-id="79223-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="79223-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="79223-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79223-129">NOTES</span></span>

## <span data-ttu-id="79223-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79223-130">RELATED LINKS</span></span>

[<span data-ttu-id="79223-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="79223-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="79223-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="79223-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="79223-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="79223-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="79223-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="79223-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)



[<span data-ttu-id="79223-135">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="79223-135">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="79223-136">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="79223-136">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
