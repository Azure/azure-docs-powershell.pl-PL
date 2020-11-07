---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: e9a93b66f62f6a42ba400dd84b6890cdf9f81cec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897282"
---
# <span data-ttu-id="18910-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18910-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="18910-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18910-102">SYNOPSIS</span></span>
<span data-ttu-id="18910-103">Usuwa obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="18910-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18910-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18910-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18910-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18910-105">DESCRIPTION</span></span>
<span data-ttu-id="18910-106">Polecenie cmdlet **Remove-AzureRmExpressRouteCircuit** usuwa obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="18910-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="18910-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18910-107">EXAMPLES</span></span>

### <span data-ttu-id="18910-108">Przykład 1: usuwanie obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="18910-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="18910-109">Przykład 2: usuwanie obwodu ExpressRoute przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="18910-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="18910-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18910-110">PARAMETERS</span></span>

### <span data-ttu-id="18910-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18910-111">-AsJob</span></span>
<span data-ttu-id="18910-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="18910-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18910-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18910-113">-DefaultProfile</span></span>
<span data-ttu-id="18910-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18910-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18910-115">-Force</span><span class="sxs-lookup"><span data-stu-id="18910-115">-Force</span></span>
<span data-ttu-id="18910-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="18910-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18910-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="18910-117">-Name</span></span>
<span data-ttu-id="18910-118">Nazwa obwodu ExpressRoute, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="18910-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18910-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18910-119">-PassThru</span></span>
<span data-ttu-id="18910-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="18910-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="18910-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="18910-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18910-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18910-122">-ResourceGroupName</span></span>
<span data-ttu-id="18910-123">Określa nazwę grupy zasobów, do której należy ten obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="18910-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18910-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18910-124">-Confirm</span></span>
<span data-ttu-id="18910-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18910-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18910-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18910-126">-WhatIf</span></span>
<span data-ttu-id="18910-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18910-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18910-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="18910-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18910-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18910-129">CommonParameters</span></span>
<span data-ttu-id="18910-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18910-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18910-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18910-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18910-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18910-132">INPUTS</span></span>

## <span data-ttu-id="18910-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18910-133">OUTPUTS</span></span>

## <span data-ttu-id="18910-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18910-134">NOTES</span></span>

## <span data-ttu-id="18910-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18910-135">RELATED LINKS</span></span>

[<span data-ttu-id="18910-136">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18910-136">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="18910-137">Przenieś — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18910-137">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="18910-138">Nowe — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18910-138">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="18910-139">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="18910-139">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
