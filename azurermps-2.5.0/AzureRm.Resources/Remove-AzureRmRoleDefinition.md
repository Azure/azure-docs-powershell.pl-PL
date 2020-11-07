---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 90b7b0b1d7909210d86ec1d5ac6b465f6e9fb239
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898860"
---
# <span data-ttu-id="203fc-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="203fc-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="203fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="203fc-102">SYNOPSIS</span></span>
<span data-ttu-id="203fc-103">Usuwa rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="203fc-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="203fc-104">Rola do usunięcia jest określona przy użyciu właściwości ID roli.</span><span class="sxs-lookup"><span data-stu-id="203fc-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="203fc-105">Usunięcie nie powiedzie się, jeśli istnieją przypisania ról wprowadzone do roli niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="203fc-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="203fc-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="203fc-106">SYNTAX</span></span>

### <span data-ttu-id="203fc-107">RoleDefinitionIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="203fc-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="203fc-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="203fc-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="203fc-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="203fc-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="203fc-110">Opis</span><span class="sxs-lookup"><span data-stu-id="203fc-110">DESCRIPTION</span></span>
<span data-ttu-id="203fc-111">Polecenie cmdlet Remove-AzureRmRoleDefinition usuwa rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="203fc-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="203fc-112">Podaj parametr identyfikatora istniejącej roli niestandardowej, aby usunąć tę rolę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="203fc-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="203fc-113">Domyślnie Remove-AzureRmRoleDefinition monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="203fc-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="203fc-114">Aby pominąć monit, należy użyć parametru Force.</span><span class="sxs-lookup"><span data-stu-id="203fc-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="203fc-115">Jeśli do roli niestandardowej zostaną usunięte istniejące przypisania ról, usuwanie zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="203fc-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="203fc-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="203fc-116">EXAMPLES</span></span>

### <span data-ttu-id="203fc-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="203fc-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="203fc-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="203fc-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="203fc-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="203fc-119">PARAMETERS</span></span>

### <span data-ttu-id="203fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203fc-120">-DefaultProfile</span></span>
<span data-ttu-id="203fc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="203fc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="203fc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="203fc-122">-Force</span></span>
<span data-ttu-id="203fc-123">Jeśli jest ustawiona, nie monituje o potwierdzenie przed usunięciem roli niestandardowej</span><span class="sxs-lookup"><span data-stu-id="203fc-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="203fc-124">-ID</span><span class="sxs-lookup"><span data-stu-id="203fc-124">-Id</span></span>
<span data-ttu-id="203fc-125">Identyfikator definicji roli do usunięcia</span><span class="sxs-lookup"><span data-stu-id="203fc-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="203fc-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="203fc-126">-InputObject</span></span>
<span data-ttu-id="203fc-127">Obiekt reprezentujący definicję roli, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="203fc-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="203fc-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="203fc-128">-Name</span></span>
<span data-ttu-id="203fc-129">Nazwa definicji roli do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="203fc-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="203fc-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="203fc-130">-PassThru</span></span>
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

### <span data-ttu-id="203fc-131">-Zakres</span><span class="sxs-lookup"><span data-stu-id="203fc-131">-Scope</span></span>
<span data-ttu-id="203fc-132">Zakres definicji roli.</span><span class="sxs-lookup"><span data-stu-id="203fc-132">Role definition scope.</span></span>

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

### <span data-ttu-id="203fc-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="203fc-133">-Confirm</span></span>
<span data-ttu-id="203fc-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="203fc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="203fc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="203fc-135">-WhatIf</span></span>
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

### <span data-ttu-id="203fc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203fc-136">CommonParameters</span></span>
<span data-ttu-id="203fc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="203fc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203fc-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="203fc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203fc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="203fc-139">INPUTS</span></span>

### <span data-ttu-id="203fc-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="203fc-140">System.Guid</span></span>

### <span data-ttu-id="203fc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="203fc-141">System.String</span></span>

### <span data-ttu-id="203fc-142">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="203fc-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="203fc-143">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="203fc-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="203fc-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="203fc-144">OUTPUTS</span></span>

### <span data-ttu-id="203fc-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="203fc-145">System.Boolean</span></span>

## <span data-ttu-id="203fc-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="203fc-146">NOTES</span></span>
<span data-ttu-id="203fc-147">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="203fc-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="203fc-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="203fc-148">RELATED LINKS</span></span>

[<span data-ttu-id="203fc-149">Nowe — AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="203fc-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="203fc-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="203fc-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="203fc-151">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="203fc-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

