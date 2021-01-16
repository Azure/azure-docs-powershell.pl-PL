---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366886"
---
# <span data-ttu-id="0b71f-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b71f-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="0b71f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b71f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b71f-103">Usuwa konfigurację połączenia obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0b71f-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="0b71f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b71f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b71f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b71f-105">DESCRIPTION</span></span>
<span data-ttu-id="0b71f-106">Polecenie cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** usuwa konfigurację połączenia obwodu ExpressRoute skojarzoną z danym obwodem usługi Express Route.</span><span class="sxs-lookup"><span data-stu-id="0b71f-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="0b71f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b71f-107">EXAMPLES</span></span>

### <span data-ttu-id="0b71f-108">Przykład 1: Usuwanie konfiguracji połączenia obwodowego ze obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="0b71f-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="0b71f-109">Przykład 2: Usuwanie konfiguracji połączenia obwodowego przy użyciu instalacji rurowej ze obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="0b71f-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="0b71f-110">Przykład 3: Usuwanie konfiguracji połączenia obwodowego z obwodu ExpressRoute dla określonej rodziny adresów</span><span class="sxs-lookup"><span data-stu-id="0b71f-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="0b71f-111">Przykład 4: Usuwanie konfiguracji połączenia obwodowego przy użyciu instalacji rurowej z obwodu ExpressRoute dla określonej rodziny adresów</span><span class="sxs-lookup"><span data-stu-id="0b71f-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="0b71f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b71f-112">PARAMETERS</span></span>

### <span data-ttu-id="0b71f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b71f-113">-DefaultProfile</span></span>
<span data-ttu-id="0b71f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b71f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b71f-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b71f-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0b71f-116">Obwód ExpressRoute zawierający konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0b71f-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="0b71f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0b71f-117">-Name</span></span>
<span data-ttu-id="0b71f-118">Nazwa konfiguracji połączenia obwodowego, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="0b71f-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="0b71f-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="0b71f-119">-AddressPrefixType</span></span>
<span data-ttu-id="0b71f-120">Określa rodzinę adresów, które należy usunąć z konfiguracji</span><span class="sxs-lookup"><span data-stu-id="0b71f-120">Specifies the address family that needs to be removed from the config</span></span> 

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

### <span data-ttu-id="0b71f-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b71f-121">-Confirm</span></span>
<span data-ttu-id="0b71f-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b71f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b71f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b71f-123">-WhatIf</span></span>
<span data-ttu-id="0b71f-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b71f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b71f-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0b71f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b71f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b71f-126">CommonParameters</span></span>
<span data-ttu-id="0b71f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b71f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b71f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b71f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b71f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b71f-129">INPUTS</span></span>

### <span data-ttu-id="0b71f-130">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b71f-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0b71f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b71f-131">OUTPUTS</span></span>

### <span data-ttu-id="0b71f-132">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b71f-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0b71f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b71f-133">NOTES</span></span>

## <span data-ttu-id="0b71f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b71f-134">RELATED LINKS</span></span>

[<span data-ttu-id="0b71f-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b71f-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0b71f-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b71f-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0b71f-137">Dodaj-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b71f-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0b71f-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b71f-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0b71f-139">Nowe — AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b71f-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0b71f-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b71f-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="0b71f-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b71f-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)