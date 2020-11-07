---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 51e84639808859a74d2070eff3a9cab984deb21c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871216"
---
# <span data-ttu-id="07c60-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="07c60-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="07c60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07c60-102">SYNOPSIS</span></span>
<span data-ttu-id="07c60-103">Usuwanie zasobu bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="07c60-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="07c60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07c60-104">SYNTAX</span></span>

### <span data-ttu-id="07c60-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="07c60-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c60-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c60-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c60-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07c60-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07c60-108">Opis</span><span class="sxs-lookup"><span data-stu-id="07c60-108">DESCRIPTION</span></span>
<span data-ttu-id="07c60-109">Usuwanie zasobu bramy NAT</span><span class="sxs-lookup"><span data-stu-id="07c60-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="07c60-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07c60-110">EXAMPLES</span></span>

### <span data-ttu-id="07c60-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="07c60-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="07c60-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07c60-112">PARAMETERS</span></span>

### <span data-ttu-id="07c60-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07c60-113">-AsJob</span></span>
<span data-ttu-id="07c60-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="07c60-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07c60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c60-115">-DefaultProfile</span></span>
<span data-ttu-id="07c60-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="07c60-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07c60-117">-Force</span><span class="sxs-lookup"><span data-stu-id="07c60-117">-Force</span></span>
<span data-ttu-id="07c60-118">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób.</span><span class="sxs-lookup"><span data-stu-id="07c60-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="07c60-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="07c60-119">-InputObject</span></span>
<span data-ttu-id="07c60-120">Określa zasób bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="07c60-120">Specifies the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="07c60-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="07c60-121">-Name</span></span>
<span data-ttu-id="07c60-122">Nazwa zasobu bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="07c60-122">Name of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="07c60-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07c60-123">-PassThru</span></span>
<span data-ttu-id="07c60-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="07c60-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="07c60-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="07c60-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="07c60-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07c60-126">-ResourceGroupName</span></span>
<span data-ttu-id="07c60-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="07c60-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="07c60-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07c60-128">-ResourceId</span></span>
<span data-ttu-id="07c60-129">Identyfikator zasobu skojarzony z bramą NAT.</span><span class="sxs-lookup"><span data-stu-id="07c60-129">Resource Id associated with the Nat Gateway.</span></span>

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

### <span data-ttu-id="07c60-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07c60-130">-Confirm</span></span>
<span data-ttu-id="07c60-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07c60-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07c60-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07c60-132">-WhatIf</span></span>
<span data-ttu-id="07c60-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07c60-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07c60-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="07c60-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07c60-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c60-135">CommonParameters</span></span>
<span data-ttu-id="07c60-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c60-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c60-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07c60-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c60-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07c60-138">INPUTS</span></span>

### <span data-ttu-id="07c60-139">Microsoft. Azure. Commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="07c60-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="07c60-140">System. String</span><span class="sxs-lookup"><span data-stu-id="07c60-140">System.String</span></span>

## <span data-ttu-id="07c60-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07c60-141">OUTPUTS</span></span>

### <span data-ttu-id="07c60-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07c60-142">System.Boolean</span></span>

## <span data-ttu-id="07c60-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07c60-143">NOTES</span></span>

## <span data-ttu-id="07c60-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07c60-144">RELATED LINKS</span></span>
