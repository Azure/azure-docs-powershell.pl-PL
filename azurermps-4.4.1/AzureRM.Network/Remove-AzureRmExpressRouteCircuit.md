---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: dd47e858132dbe77556d82ce234d41bc2c990f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546211"
---
# <span data-ttu-id="0046b-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0046b-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="0046b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0046b-102">SYNOPSIS</span></span>
<span data-ttu-id="0046b-103">Usuwa obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0046b-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0046b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0046b-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0046b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0046b-105">DESCRIPTION</span></span>
<span data-ttu-id="0046b-106">Polecenie cmdlet **Remove-AzureRmExpressRouteCircuit** usuwa obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0046b-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="0046b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0046b-107">EXAMPLES</span></span>

### <span data-ttu-id="0046b-108">Przykład 1: usuwanie obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="0046b-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="0046b-109">Przykład 2: usuwanie obwodu ExpressRoute przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="0046b-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="0046b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0046b-110">PARAMETERS</span></span>

### <span data-ttu-id="0046b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0046b-111">-Force</span></span>
<span data-ttu-id="0046b-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0046b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0046b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0046b-113">-Name</span></span>
<span data-ttu-id="0046b-114">Nazwa obwodu ExpressRoute, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="0046b-114">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="0046b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0046b-115">-PassThru</span></span>
<span data-ttu-id="0046b-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0046b-116">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="0046b-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0046b-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0046b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0046b-118">-ResourceGroupName</span></span>
<span data-ttu-id="0046b-119">Określa nazwę grupy zasobów, do której należy ten obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0046b-119">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="0046b-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0046b-120">-Confirm</span></span>
<span data-ttu-id="0046b-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0046b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0046b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0046b-122">-WhatIf</span></span>
<span data-ttu-id="0046b-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0046b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0046b-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0046b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0046b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0046b-125">-DefaultProfile</span></span>
<span data-ttu-id="0046b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0046b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0046b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0046b-127">CommonParameters</span></span>
<span data-ttu-id="0046b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0046b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0046b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0046b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0046b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0046b-130">INPUTS</span></span>

## <span data-ttu-id="0046b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0046b-131">OUTPUTS</span></span>

## <span data-ttu-id="0046b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0046b-132">NOTES</span></span>

## <span data-ttu-id="0046b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0046b-133">RELATED LINKS</span></span>

[<span data-ttu-id="0046b-134">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0046b-134">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0046b-135">Przenieś — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0046b-135">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0046b-136">Nowe — AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0046b-136">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0046b-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0046b-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
