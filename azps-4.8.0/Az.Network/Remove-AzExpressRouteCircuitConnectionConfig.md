---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: fb82b00f998ed0c2b7473d4a3e0bcb9b3dc60630
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397853"
---
# <span data-ttu-id="ad58f-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ad58f-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="ad58f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad58f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad58f-103">Usuwa konfigurację połączenia obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ad58f-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="ad58f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad58f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad58f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad58f-105">DESCRIPTION</span></span>
<span data-ttu-id="ad58f-106">Polecenie **cmdlet Remove-AzExpressRouteCircuitConnectionConfig** usuwa konfigurację połączenia obwodu usługi ExpressRoute skojarzoną z danym obwodem trasy expressowej.</span><span class="sxs-lookup"><span data-stu-id="ad58f-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="ad58f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad58f-107">EXAMPLES</span></span>

### <span data-ttu-id="ad58f-108">Przykład 1. Usuwanie konfiguracji połączenia obwodu z obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ad58f-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="ad58f-109">Przykład 2. Usuwanie konfiguracji połączenia obwodu za pomocą połączeń rurowych z obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ad58f-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="ad58f-110">Przykład 3. Usuwanie konfiguracji połączenia obwodu z obwodu usługi ExpressRoute dla określonej rodziny adresów</span><span class="sxs-lookup"><span data-stu-id="ad58f-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="ad58f-111">Przykład 4. Usuwanie konfiguracji połączenia obwodu za pomocą połączeń rurowych z obwodu usługi ExpressRoute dla określonej rodziny adresów</span><span class="sxs-lookup"><span data-stu-id="ad58f-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="ad58f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad58f-112">PARAMETERS</span></span>

### <span data-ttu-id="ad58f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad58f-113">-DefaultProfile</span></span>
<span data-ttu-id="ad58f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad58f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad58f-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ad58f-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ad58f-116">Obwód usługi ExpressRoute zawierający konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ad58f-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ad58f-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad58f-117">-Name</span></span>
<span data-ttu-id="ad58f-118">Nazwa konfiguracji połączenia obwodu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ad58f-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="ad58f-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="ad58f-119">-AddressPrefixType</span></span>
<span data-ttu-id="ad58f-120">Określa rodzinę adresów, która musi zostać usunięta z konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ad58f-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad58f-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad58f-121">-Confirm</span></span>
<span data-ttu-id="ad58f-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ad58f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad58f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad58f-123">-WhatIf</span></span>
<span data-ttu-id="ad58f-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad58f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad58f-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ad58f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad58f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad58f-126">CommonParameters</span></span>
<span data-ttu-id="ad58f-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad58f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad58f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad58f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad58f-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad58f-129">INPUTS</span></span>

### <span data-ttu-id="ad58f-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ad58f-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ad58f-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad58f-131">OUTPUTS</span></span>

### <span data-ttu-id="ad58f-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ad58f-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ad58f-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad58f-133">NOTES</span></span>

## <span data-ttu-id="ad58f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad58f-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad58f-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ad58f-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ad58f-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ad58f-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ad58f-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ad58f-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ad58f-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ad58f-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)



[<span data-ttu-id="ad58f-139">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ad58f-139">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="ad58f-140">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ad58f-140">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
