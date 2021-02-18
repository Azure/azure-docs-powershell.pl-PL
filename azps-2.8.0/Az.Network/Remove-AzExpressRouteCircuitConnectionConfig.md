---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c596dffcef97dfbb1cabbc5ca2c2455a7768c25f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409940"
---
# <span data-ttu-id="f6faa-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f6faa-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="f6faa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6faa-102">SYNOPSIS</span></span>
<span data-ttu-id="f6faa-103">Usuwa konfigurację połączenia obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f6faa-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="f6faa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f6faa-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6faa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f6faa-105">DESCRIPTION</span></span>
<span data-ttu-id="f6faa-106">Polecenie **cmdlet Remove-AzExpressRouteCircuitConnectionConfig** usuwa konfigurację połączenia obwodu usługi ExpressRoute skojarzoną z danym obwodem trasy expressowej.</span><span class="sxs-lookup"><span data-stu-id="f6faa-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="f6faa-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f6faa-107">EXAMPLES</span></span>

### <span data-ttu-id="f6faa-108">Przykład 1. Usuwanie konfiguracji połączenia obwodu z obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f6faa-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="f6faa-109">Przykład 2. Usuwanie konfiguracji połączenia obwodu za pomocą połączeń rurowych z obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f6faa-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="f6faa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6faa-110">PARAMETERS</span></span>

### <span data-ttu-id="f6faa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6faa-111">-DefaultProfile</span></span>
<span data-ttu-id="f6faa-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6faa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6faa-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f6faa-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f6faa-114">Obwód usługi ExpressRoute zawierający konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f6faa-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="f6faa-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f6faa-115">-Name</span></span>
<span data-ttu-id="f6faa-116">Nazwa konfiguracji połączenia obwodu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f6faa-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="f6faa-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6faa-117">-Confirm</span></span>
<span data-ttu-id="f6faa-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f6faa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6faa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6faa-119">-WhatIf</span></span>
<span data-ttu-id="f6faa-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6faa-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6faa-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f6faa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6faa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6faa-122">CommonParameters</span></span>
<span data-ttu-id="f6faa-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6faa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6faa-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6faa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6faa-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6faa-125">INPUTS</span></span>

### <span data-ttu-id="f6faa-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f6faa-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f6faa-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6faa-127">OUTPUTS</span></span>

### <span data-ttu-id="f6faa-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f6faa-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f6faa-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f6faa-129">NOTES</span></span>

## <span data-ttu-id="f6faa-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6faa-130">RELATED LINKS</span></span>

[<span data-ttu-id="f6faa-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f6faa-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f6faa-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f6faa-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f6faa-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f6faa-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="f6faa-134">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f6faa-134">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="f6faa-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f6faa-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
