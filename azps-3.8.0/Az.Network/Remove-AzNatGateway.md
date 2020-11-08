---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052989"
---
# <span data-ttu-id="0a7a5-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a7a5-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="0a7a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="0a7a5-103">Usuwanie zasobu bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="0a7a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a7a5-104">SYNTAX</span></span>

### <span data-ttu-id="0a7a5-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0a7a5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a7a5-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a7a5-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a7a5-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a7a5-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a7a5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0a7a5-108">DESCRIPTION</span></span>
<span data-ttu-id="0a7a5-109">Usuwanie zasobu bramy NAT</span><span class="sxs-lookup"><span data-stu-id="0a7a5-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="0a7a5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a7a5-110">EXAMPLES</span></span>

### <span data-ttu-id="0a7a5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0a7a5-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="0a7a5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a7a5-112">PARAMETERS</span></span>

### <span data-ttu-id="0a7a5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a7a5-113">-AsJob</span></span>
<span data-ttu-id="0a7a5-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0a7a5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a7a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a7a5-115">-DefaultProfile</span></span>
<span data-ttu-id="0a7a5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a7a5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0a7a5-117">-Force</span></span>
<span data-ttu-id="0a7a5-118">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="0a7a5-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0a7a5-119">-InputObject</span></span>
<span data-ttu-id="0a7a5-120">Określa zasób bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7a5-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a7a5-121">-Name</span></span>
<span data-ttu-id="0a7a5-122">Nazwa zasobu bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7a5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a7a5-123">-PassThru</span></span>
<span data-ttu-id="0a7a5-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0a7a5-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a7a5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a7a5-126">-ResourceGroupName</span></span>
<span data-ttu-id="0a7a5-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a7a5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a7a5-128">-ResourceId</span></span>
<span data-ttu-id="0a7a5-129">Identyfikator zasobu skojarzony z bramą NAT.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7a5-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a7a5-130">-Confirm</span></span>
<span data-ttu-id="0a7a5-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a7a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a7a5-132">-WhatIf</span></span>
<span data-ttu-id="0a7a5-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a7a5-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a7a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7a5-135">CommonParameters</span></span>
<span data-ttu-id="0a7a5-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a7a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7a5-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a7a5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7a5-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a7a5-138">INPUTS</span></span>

### <span data-ttu-id="0a7a5-139">Microsoft. Azure. Commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a7a5-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="0a7a5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0a7a5-140">System.String</span></span>

## <span data-ttu-id="0a7a5-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a7a5-141">OUTPUTS</span></span>

### <span data-ttu-id="0a7a5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0a7a5-142">System.Boolean</span></span>

## <span data-ttu-id="0a7a5-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a7a5-143">NOTES</span></span>

## <span data-ttu-id="0a7a5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a7a5-144">RELATED LINKS</span></span>
