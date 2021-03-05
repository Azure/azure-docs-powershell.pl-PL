---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 430ea183d618779045aaf5d13554edac2ce98626
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996255"
---
# <span data-ttu-id="27396-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27396-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="27396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27396-102">SYNOPSIS</span></span>
<span data-ttu-id="27396-103">Usuń zasób Brama Nat.</span><span class="sxs-lookup"><span data-stu-id="27396-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="27396-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="27396-104">SYNTAX</span></span>

### <span data-ttu-id="27396-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="27396-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27396-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27396-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27396-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27396-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27396-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="27396-108">DESCRIPTION</span></span>
<span data-ttu-id="27396-109">Usuwanie zasobu bramy nat</span><span class="sxs-lookup"><span data-stu-id="27396-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="27396-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="27396-110">EXAMPLES</span></span>

### <span data-ttu-id="27396-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="27396-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="27396-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27396-112">PARAMETERS</span></span>

### <span data-ttu-id="27396-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="27396-113">-AsJob</span></span>
<span data-ttu-id="27396-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="27396-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27396-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27396-115">-DefaultProfile</span></span>
<span data-ttu-id="27396-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="27396-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27396-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="27396-117">-Force</span></span>
<span data-ttu-id="27396-118">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób.</span><span class="sxs-lookup"><span data-stu-id="27396-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="27396-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27396-119">-InputObject</span></span>
<span data-ttu-id="27396-120">Określa zasób Brama Nat.</span><span class="sxs-lookup"><span data-stu-id="27396-120">Specifies the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="27396-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="27396-121">-Name</span></span>
<span data-ttu-id="27396-122">Nazwa zasobu Brama nat.</span><span class="sxs-lookup"><span data-stu-id="27396-122">Name of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="27396-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27396-123">-PassThru</span></span>
<span data-ttu-id="27396-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="27396-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="27396-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="27396-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="27396-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27396-126">-ResourceGroupName</span></span>
<span data-ttu-id="27396-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="27396-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="27396-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27396-128">-ResourceId</span></span>
<span data-ttu-id="27396-129">Identyfikator zasobu skojarzony z bramą nat.</span><span class="sxs-lookup"><span data-stu-id="27396-129">Resource Id associated with the Nat Gateway.</span></span>

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

### <span data-ttu-id="27396-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27396-130">-Confirm</span></span>
<span data-ttu-id="27396-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="27396-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27396-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27396-132">-WhatIf</span></span>
<span data-ttu-id="27396-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27396-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27396-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="27396-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27396-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27396-135">CommonParameters</span></span>
<span data-ttu-id="27396-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27396-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27396-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27396-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27396-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27396-138">INPUTS</span></span>

### <span data-ttu-id="27396-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="27396-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="27396-140">System.String</span><span class="sxs-lookup"><span data-stu-id="27396-140">System.String</span></span>

## <span data-ttu-id="27396-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27396-141">OUTPUTS</span></span>

### <span data-ttu-id="27396-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27396-142">System.Boolean</span></span>

## <span data-ttu-id="27396-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="27396-143">NOTES</span></span>

## <span data-ttu-id="27396-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27396-144">RELATED LINKS</span></span>
