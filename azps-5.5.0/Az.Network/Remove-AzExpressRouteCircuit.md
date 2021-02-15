---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202575"
---
# <span data-ttu-id="6a7c4-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a7c4-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="6a7c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7c4-103">Usuwa obwód w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="6a7c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a7c4-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a7c4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a7c4-105">DESCRIPTION</span></span>
<span data-ttu-id="6a7c4-106">Polecenie **cmdlet Remove-AzExpressRouteCircuit** usuwa obwód expressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="6a7c4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a7c4-107">EXAMPLES</span></span>

### <span data-ttu-id="6a7c4-108">Przykład 1. Usuwanie obwodu w układzie ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6a7c4-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="6a7c4-109">Przykład 2. Usuwanie obwodu usługi ExpressRoute przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="6a7c4-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="6a7c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a7c4-110">PARAMETERS</span></span>

### <span data-ttu-id="6a7c4-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6a7c4-111">-AsJob</span></span>
<span data-ttu-id="6a7c4-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6a7c4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a7c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7c4-113">-DefaultProfile</span></span>
<span data-ttu-id="6a7c4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a7c4-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6a7c4-115">-Force</span></span>
<span data-ttu-id="6a7c4-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a7c4-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6a7c4-117">-Name</span></span>
<span data-ttu-id="6a7c4-118">Nazwa obwodu expressRoute do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="6a7c4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a7c4-119">-PassThru</span></span>
<span data-ttu-id="6a7c4-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6a7c4-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a7c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a7c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a7c4-123">Określa nazwę grupy zasobów, do której należy ten obwód expressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="6a7c4-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a7c4-124">-Confirm</span></span>
<span data-ttu-id="6a7c4-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a7c4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a7c4-126">-WhatIf</span></span>
<span data-ttu-id="6a7c4-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a7c4-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a7c4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7c4-129">CommonParameters</span></span>
<span data-ttu-id="6a7c4-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a7c4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7c4-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a7c4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7c4-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a7c4-132">INPUTS</span></span>

### <span data-ttu-id="6a7c4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6a7c4-133">System.String</span></span>

## <span data-ttu-id="6a7c4-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a7c4-134">OUTPUTS</span></span>

### <span data-ttu-id="6a7c4-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a7c4-135">System.Boolean</span></span>

## <span data-ttu-id="6a7c4-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a7c4-136">NOTES</span></span>

## <span data-ttu-id="6a7c4-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a7c4-137">RELATED LINKS</span></span>

[<span data-ttu-id="6a7c4-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a7c4-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="6a7c4-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a7c4-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="6a7c4-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a7c4-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="6a7c4-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a7c4-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
