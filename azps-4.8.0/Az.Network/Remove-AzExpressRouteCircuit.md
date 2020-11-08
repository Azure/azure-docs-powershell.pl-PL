---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223760"
---
# <span data-ttu-id="edd5c-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="edd5c-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="edd5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="edd5c-102">SYNOPSIS</span></span>
<span data-ttu-id="edd5c-103">Usuwa obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="edd5c-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="edd5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="edd5c-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edd5c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="edd5c-105">DESCRIPTION</span></span>
<span data-ttu-id="edd5c-106">Polecenie cmdlet **Remove-AzExpressRouteCircuit** usuwa obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="edd5c-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="edd5c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="edd5c-107">EXAMPLES</span></span>

### <span data-ttu-id="edd5c-108">Przykład 1: usuwanie obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="edd5c-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="edd5c-109">Przykład 2: usuwanie obwodu ExpressRoute przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="edd5c-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="edd5c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edd5c-110">PARAMETERS</span></span>

### <span data-ttu-id="edd5c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edd5c-111">-AsJob</span></span>
<span data-ttu-id="edd5c-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="edd5c-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd5c-113">-DefaultProfile</span></span>
<span data-ttu-id="edd5c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="edd5c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edd5c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="edd5c-115">-Force</span></span>
<span data-ttu-id="edd5c-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="edd5c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd5c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="edd5c-117">-Name</span></span>
<span data-ttu-id="edd5c-118">Nazwa obwodu ExpressRoute, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="edd5c-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edd5c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edd5c-119">-PassThru</span></span>
<span data-ttu-id="edd5c-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="edd5c-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="edd5c-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="edd5c-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd5c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd5c-122">-ResourceGroupName</span></span>
<span data-ttu-id="edd5c-123">Określa nazwę grupy zasobów, do której należy ten obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="edd5c-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edd5c-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edd5c-124">-Confirm</span></span>
<span data-ttu-id="edd5c-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edd5c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd5c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edd5c-126">-WhatIf</span></span>
<span data-ttu-id="edd5c-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edd5c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edd5c-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="edd5c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd5c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd5c-129">CommonParameters</span></span>
<span data-ttu-id="edd5c-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd5c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd5c-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd5c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd5c-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edd5c-132">INPUTS</span></span>

### <span data-ttu-id="edd5c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="edd5c-133">System.String</span></span>

## <span data-ttu-id="edd5c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="edd5c-134">OUTPUTS</span></span>

### <span data-ttu-id="edd5c-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="edd5c-135">System.Boolean</span></span>

## <span data-ttu-id="edd5c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="edd5c-136">NOTES</span></span>

## <span data-ttu-id="edd5c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edd5c-137">RELATED LINKS</span></span>

[<span data-ttu-id="edd5c-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="edd5c-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="edd5c-139">Przenieś — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="edd5c-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="edd5c-140">Nowe — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="edd5c-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="edd5c-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="edd5c-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
