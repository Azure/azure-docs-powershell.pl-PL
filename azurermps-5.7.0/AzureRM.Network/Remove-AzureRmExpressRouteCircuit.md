---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 3ea8e43710d9e195218cc1b96a2656af2a7e2adf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528030"
---
# <span data-ttu-id="f8dc6-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8dc6-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="f8dc6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="f8dc6-103">Usuwa obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8dc6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8dc6-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8dc6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8dc6-105">DESCRIPTION</span></span>
<span data-ttu-id="f8dc6-106">Polecenie cmdlet **Remove-AzureRmExpressRouteCircuit** usuwa obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f8dc6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8dc6-107">EXAMPLES</span></span>

### <span data-ttu-id="f8dc6-108">Przykład 1: usuwanie obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f8dc6-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="f8dc6-109">Przykład 2: usuwanie obwodu ExpressRoute przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="f8dc6-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="f8dc6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8dc6-110">PARAMETERS</span></span>

### <span data-ttu-id="f8dc6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8dc6-111">-AsJob</span></span>
<span data-ttu-id="f8dc6-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f8dc6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8dc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8dc6-113">-DefaultProfile</span></span>
<span data-ttu-id="f8dc6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8dc6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f8dc6-115">-Force</span></span>
<span data-ttu-id="f8dc6-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f8dc6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8dc6-117">-Name</span></span>
<span data-ttu-id="f8dc6-118">Nazwa obwodu ExpressRoute, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="f8dc6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8dc6-119">-PassThru</span></span>
<span data-ttu-id="f8dc6-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f8dc6-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8dc6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8dc6-122">-ResourceGroupName</span></span>
<span data-ttu-id="f8dc6-123">Określa nazwę grupy zasobów, do której należy ten obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="f8dc6-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8dc6-124">-Confirm</span></span>
<span data-ttu-id="f8dc6-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8dc6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8dc6-126">-WhatIf</span></span>
<span data-ttu-id="f8dc6-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8dc6-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8dc6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8dc6-129">CommonParameters</span></span>
<span data-ttu-id="f8dc6-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8dc6-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8dc6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8dc6-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8dc6-132">INPUTS</span></span>

### <span data-ttu-id="f8dc6-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f8dc6-133">None</span></span>
<span data-ttu-id="f8dc6-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f8dc6-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8dc6-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8dc6-135">OUTPUTS</span></span>

## <span data-ttu-id="f8dc6-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8dc6-136">NOTES</span></span>

## <span data-ttu-id="f8dc6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8dc6-137">RELATED LINKS</span></span>

[<span data-ttu-id="f8dc6-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8dc6-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f8dc6-139">Przenieś — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8dc6-139">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f8dc6-140">Nowe — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8dc6-140">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f8dc6-141">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8dc6-141">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)