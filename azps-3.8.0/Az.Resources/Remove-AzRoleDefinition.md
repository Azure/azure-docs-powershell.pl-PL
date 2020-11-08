---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: a2bd64daf4b9895de3ef8ca12ff0fec7295cd094
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050756"
---
# <span data-ttu-id="c982a-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c982a-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="c982a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c982a-102">SYNOPSIS</span></span>
<span data-ttu-id="c982a-103">Usuwa rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="c982a-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="c982a-104">Rola do usunięcia jest określona przy użyciu właściwości ID roli.</span><span class="sxs-lookup"><span data-stu-id="c982a-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="c982a-105">Usunięcie nie powiedzie się, jeśli istnieją przypisania ról wprowadzone do roli niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="c982a-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="c982a-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c982a-106">SYNTAX</span></span>

### <span data-ttu-id="c982a-107">RoleDefinitionIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c982a-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c982a-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c982a-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c982a-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c982a-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c982a-110">Opis</span><span class="sxs-lookup"><span data-stu-id="c982a-110">DESCRIPTION</span></span>
<span data-ttu-id="c982a-111">Polecenie cmdlet Remove-AzRoleDefinition usuwa rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="c982a-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="c982a-112">Podaj parametr identyfikatora istniejącej roli niestandardowej, aby usunąć tę rolę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="c982a-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="c982a-113">Domyślnie Remove-AzRoleDefinition monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c982a-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="c982a-114">Aby pominąć monit, należy użyć parametru Force.</span><span class="sxs-lookup"><span data-stu-id="c982a-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="c982a-115">Jeśli do roli niestandardowej zostaną usunięte istniejące przypisania ról, usuwanie zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="c982a-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="c982a-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c982a-116">EXAMPLES</span></span>

### <span data-ttu-id="c982a-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c982a-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="c982a-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c982a-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="c982a-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c982a-119">PARAMETERS</span></span>

### <span data-ttu-id="c982a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c982a-120">-DefaultProfile</span></span>
<span data-ttu-id="c982a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c982a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c982a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c982a-122">-Force</span></span>
<span data-ttu-id="c982a-123">Jeśli jest ustawiona, nie monituje o potwierdzenie przed usunięciem roli niestandardowej</span><span class="sxs-lookup"><span data-stu-id="c982a-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="c982a-124">-ID</span><span class="sxs-lookup"><span data-stu-id="c982a-124">-Id</span></span>
<span data-ttu-id="c982a-125">Identyfikator definicji roli do usunięcia</span><span class="sxs-lookup"><span data-stu-id="c982a-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="c982a-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c982a-126">-InputObject</span></span>
<span data-ttu-id="c982a-127">Obiekt reprezentujący definicję roli, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="c982a-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="c982a-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c982a-128">-Name</span></span>
<span data-ttu-id="c982a-129">Nazwa definicji roli do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c982a-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="c982a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c982a-130">-PassThru</span></span>
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

### <span data-ttu-id="c982a-131">-Zakres</span><span class="sxs-lookup"><span data-stu-id="c982a-131">-Scope</span></span>
<span data-ttu-id="c982a-132">Zakres definicji roli.</span><span class="sxs-lookup"><span data-stu-id="c982a-132">Role definition scope.</span></span>

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

### <span data-ttu-id="c982a-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c982a-133">-Confirm</span></span>
<span data-ttu-id="c982a-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c982a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c982a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c982a-135">-WhatIf</span></span>
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

### <span data-ttu-id="c982a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c982a-136">CommonParameters</span></span>
<span data-ttu-id="c982a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c982a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c982a-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c982a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c982a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c982a-139">INPUTS</span></span>

### <span data-ttu-id="c982a-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c982a-140">System.Guid</span></span>

### <span data-ttu-id="c982a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c982a-141">System.String</span></span>

### <span data-ttu-id="c982a-142">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c982a-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="c982a-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c982a-143">OUTPUTS</span></span>

### <span data-ttu-id="c982a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c982a-144">System.Boolean</span></span>

## <span data-ttu-id="c982a-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c982a-145">NOTES</span></span>
<span data-ttu-id="c982a-146">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="c982a-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c982a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c982a-147">RELATED LINKS</span></span>

[<span data-ttu-id="c982a-148">Nowe — AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c982a-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="c982a-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c982a-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="c982a-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c982a-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

