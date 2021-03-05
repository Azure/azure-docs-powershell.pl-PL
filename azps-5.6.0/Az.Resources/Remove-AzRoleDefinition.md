---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: d4ce9ef88f7043a369d8e566de75651944ea1e88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014897"
---
# <span data-ttu-id="9cece-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9cece-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="9cece-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cece-102">SYNOPSIS</span></span>
<span data-ttu-id="9cece-103">Usuwa niestandardową rolę w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="9cece-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="9cece-104">Rola do usunięcia jest określana przy użyciu właściwości Identyfikator roli.</span><span class="sxs-lookup"><span data-stu-id="9cece-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="9cece-105">Usunięcie nie powiedzie się, jeśli istnieją istniejące przypisania ról wprowadzone do roli niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="9cece-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="9cece-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9cece-106">SYNTAX</span></span>

### <span data-ttu-id="9cece-107">RoleDefinitionIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9cece-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cece-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cece-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cece-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cece-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cece-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="9cece-110">DESCRIPTION</span></span>
<span data-ttu-id="9cece-111">Polecenie Remove-AzRoleDefinition usuwa niestandardową rolę w usłudze Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="9cece-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="9cece-112">Podaj parametr Id istniejącej roli niestandardowej, aby usunąć tę rolę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="9cece-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="9cece-113">Domyślnie program Remove-AzRoleDefinition monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9cece-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="9cece-114">Aby pominąć monit, użyj parametru Force.</span><span class="sxs-lookup"><span data-stu-id="9cece-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="9cece-115">Jeśli istnieją istniejące przypisania ról do roli niestandardowej do usunięcia, usunięcie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="9cece-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="9cece-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9cece-116">EXAMPLES</span></span>

### <span data-ttu-id="9cece-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9cece-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="9cece-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9cece-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="9cece-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cece-119">PARAMETERS</span></span>

### <span data-ttu-id="9cece-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cece-120">-DefaultProfile</span></span>
<span data-ttu-id="9cece-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9cece-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cece-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9cece-122">-Force</span></span>
<span data-ttu-id="9cece-123">Jeśli ta wartość jest ustawiona, nie wyświetla monitu o potwierdzenie przed usunięciem roli niestandardowej</span><span class="sxs-lookup"><span data-stu-id="9cece-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="9cece-124">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="9cece-124">-Id</span></span>
<span data-ttu-id="9cece-125">Identyfikator definicji roli do usunięcia</span><span class="sxs-lookup"><span data-stu-id="9cece-125">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cece-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cece-126">-InputObject</span></span>
<span data-ttu-id="9cece-127">Obiekt reprezentujący definicję roli do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9cece-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cece-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9cece-128">-Name</span></span>
<span data-ttu-id="9cece-129">Nazwa definicji roli do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9cece-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cece-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cece-130">-PassThru</span></span>
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

### <span data-ttu-id="9cece-131">— Zakres</span><span class="sxs-lookup"><span data-stu-id="9cece-131">-Scope</span></span>
<span data-ttu-id="9cece-132">Zakres definicji ról.</span><span class="sxs-lookup"><span data-stu-id="9cece-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cece-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cece-133">-Confirm</span></span>
<span data-ttu-id="9cece-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9cece-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cece-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cece-135">-WhatIf</span></span>
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

### <span data-ttu-id="9cece-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cece-136">CommonParameters</span></span>
<span data-ttu-id="9cece-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cece-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cece-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cece-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cece-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cece-139">INPUTS</span></span>

### <span data-ttu-id="9cece-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9cece-140">System.Guid</span></span>

### <span data-ttu-id="9cece-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9cece-141">System.String</span></span>

### <span data-ttu-id="9cece-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9cece-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="9cece-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cece-143">OUTPUTS</span></span>

### <span data-ttu-id="9cece-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9cece-144">System.Boolean</span></span>

## <span data-ttu-id="9cece-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9cece-145">NOTES</span></span>
<span data-ttu-id="9cece-146">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="9cece-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9cece-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cece-147">RELATED LINKS</span></span>

[<span data-ttu-id="9cece-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9cece-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="9cece-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9cece-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="9cece-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9cece-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

