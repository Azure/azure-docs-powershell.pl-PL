---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 6383a1fb0a6dbaa20bee50a268d8f78abf59de65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979409"
---
# <span data-ttu-id="d6ddd-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="d6ddd-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="d6ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ddd-103">Usuwa specyfikację szablonu</span><span class="sxs-lookup"><span data-stu-id="d6ddd-103">Removes a Template Spec</span></span>

## <span data-ttu-id="d6ddd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6ddd-104">SYNTAX</span></span>

### <span data-ttu-id="d6ddd-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d6ddd-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6ddd-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6ddd-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6ddd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6ddd-107">DESCRIPTION</span></span>
<span data-ttu-id="d6ddd-108">Usuwa określoną specyfikację szablonu. Jeśli parametr version **-Version** jest podany, zostanie usunięta tylko określona wersja.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="d6ddd-109">Jeśli nie podano konkretnej wersji, specyfikacja szablonu i wszystkie jej wersje zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="d6ddd-110">Jeśli **flaga -Force** jest obecna, nie będzie monitu o potwierdzenie usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="d6ddd-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6ddd-111">EXAMPLES</span></span>

### <span data-ttu-id="d6ddd-112">Przykład 1. Usuwanie określonej wersji według nazwy</span><span class="sxs-lookup"><span data-stu-id="d6ddd-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="d6ddd-113">Usuwa wersję "1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" z grupy zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="d6ddd-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="d6ddd-114">Przykład 2. Usuwanie określonej wersji według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="d6ddd-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="d6ddd-115">Usuwa wersję "1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" \{ podid \} subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="d6ddd-116">Przykład 3. Usuwanie specyfikacji szablonu i wszystkich wersji według nazwy</span><span class="sxs-lookup"><span data-stu-id="d6ddd-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="d6ddd-117">Usuwa specyfikację szablonu o nazwie "MyTemplateSpec" i wszystkie jej wersje w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="d6ddd-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="d6ddd-118">Przykład 3. Usuwanie specyfikacji szablonu i wszystkich wersji według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="d6ddd-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="d6ddd-119">Usuwa specyfikację szablonu o nazwie "MyTemplateSpec" i wszystkie jej wersje w grupie zasobów "myRG" \{ podid \} subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="d6ddd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6ddd-120">PARAMETERS</span></span>

### <span data-ttu-id="d6ddd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ddd-121">-DefaultProfile</span></span>
<span data-ttu-id="d6ddd-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ddd-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d6ddd-123">-Force</span></span>
<span data-ttu-id="d6ddd-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d6ddd-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6ddd-125">-Name</span></span>
<span data-ttu-id="d6ddd-126">Nazwa specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ddd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ddd-127">-ResourceGroupName</span></span>
<span data-ttu-id="d6ddd-128">Nazwa grupy zasobów specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ddd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6ddd-129">-ResourceId</span></span>
<span data-ttu-id="d6ddd-130">W pełni kwalifikowany identyfikator zasobu specyfikacji szablonu. Przykład: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="d6ddd-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ddd-131">— Wersja</span><span class="sxs-lookup"><span data-stu-id="d6ddd-131">-Version</span></span>
<span data-ttu-id="d6ddd-132">Wersja specyfikacji szablonu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ddd-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6ddd-133">-Confirm</span></span>
<span data-ttu-id="d6ddd-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ddd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ddd-135">-WhatIf</span></span>
<span data-ttu-id="d6ddd-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6ddd-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ddd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ddd-138">CommonParameters</span></span>
<span data-ttu-id="d6ddd-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ddd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ddd-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6ddd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ddd-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6ddd-141">INPUTS</span></span>

### <span data-ttu-id="d6ddd-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d6ddd-142">System.String</span></span>

## <span data-ttu-id="d6ddd-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6ddd-143">OUTPUTS</span></span>

### <span data-ttu-id="d6ddd-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6ddd-144">System.Boolean</span></span>

## <span data-ttu-id="d6ddd-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6ddd-145">NOTES</span></span>

## <span data-ttu-id="d6ddd-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6ddd-146">RELATED LINKS</span></span>
