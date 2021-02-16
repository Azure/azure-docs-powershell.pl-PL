---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179491"
---
# <span data-ttu-id="3201e-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3201e-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="3201e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3201e-102">SYNOPSIS</span></span>
<span data-ttu-id="3201e-103">Usuwa poprawkę CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3201e-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="3201e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3201e-104">SYNTAX</span></span>

### <span data-ttu-id="3201e-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3201e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3201e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3201e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3201e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3201e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3201e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3201e-108">DESCRIPTION</span></span>
<span data-ttu-id="3201e-109">Polecenie **cmdlet Remove-AzCustomIpPrefix** usuwa polecenie CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="3201e-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="3201e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3201e-110">EXAMPLES</span></span>

### <span data-ttu-id="3201e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3201e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="3201e-112">Usuwa poprawkę CustomIpPrefix z polami Nazwa $prefixName z grupy zasobów $rgName</span><span class="sxs-lookup"><span data-stu-id="3201e-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="3201e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3201e-113">PARAMETERS</span></span>

### <span data-ttu-id="3201e-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3201e-114">-AsJob</span></span>
<span data-ttu-id="3201e-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3201e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3201e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3201e-116">-DefaultProfile</span></span>
<span data-ttu-id="3201e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3201e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201e-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3201e-118">-Force</span></span>
<span data-ttu-id="3201e-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3201e-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3201e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3201e-120">-InputObject</span></span>
<span data-ttu-id="3201e-121">Obiekt customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="3201e-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3201e-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3201e-122">-Name</span></span>
<span data-ttu-id="3201e-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3201e-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3201e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3201e-124">-PassThru</span></span>
<span data-ttu-id="3201e-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3201e-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3201e-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3201e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3201e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3201e-127">-ResourceGroupName</span></span>
<span data-ttu-id="3201e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3201e-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3201e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3201e-129">-ResourceId</span></span>
<span data-ttu-id="3201e-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3201e-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3201e-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3201e-131">-Confirm</span></span>
<span data-ttu-id="3201e-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3201e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3201e-133">-WhatIf</span></span>
<span data-ttu-id="3201e-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3201e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3201e-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3201e-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3201e-136">CommonParameters</span></span>
<span data-ttu-id="3201e-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3201e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3201e-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3201e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3201e-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3201e-139">INPUTS</span></span>

### <span data-ttu-id="3201e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3201e-140">System.String</span></span>

### <span data-ttu-id="3201e-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3201e-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="3201e-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3201e-142">OUTPUTS</span></span>

### <span data-ttu-id="3201e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3201e-143">System.Boolean</span></span>

## <span data-ttu-id="3201e-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3201e-144">NOTES</span></span>

## <span data-ttu-id="3201e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3201e-145">RELATED LINKS</span></span>

[<span data-ttu-id="3201e-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3201e-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="3201e-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3201e-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="3201e-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3201e-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)