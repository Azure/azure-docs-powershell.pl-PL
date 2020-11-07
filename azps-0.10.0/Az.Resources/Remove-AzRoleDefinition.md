---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: f31a09f0d148d25796e157eb300a6f5918dade44
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892378"
---
# <span data-ttu-id="f38f0-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f38f0-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="f38f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f38f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f38f0-103">Usuwa rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="f38f0-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="f38f0-104">Rola do usunięcia jest określona przy użyciu właściwości ID roli.</span><span class="sxs-lookup"><span data-stu-id="f38f0-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="f38f0-105">Usunięcie nie powiedzie się, jeśli istnieją przypisania ról wprowadzone do roli niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="f38f0-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="f38f0-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f38f0-106">SYNTAX</span></span>

### <span data-ttu-id="f38f0-107">RoleDefinitionIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f38f0-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f38f0-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f38f0-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f38f0-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f38f0-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f38f0-110">Opis</span><span class="sxs-lookup"><span data-stu-id="f38f0-110">DESCRIPTION</span></span>
<span data-ttu-id="f38f0-111">Polecenie cmdlet Remove-AzRoleDefinition usuwa rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="f38f0-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="f38f0-112">Podaj parametr identyfikatora istniejącej roli niestandardowej, aby usunąć tę rolę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="f38f0-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="f38f0-113">Domyślnie Remove-AzRoleDefinition monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f38f0-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="f38f0-114">Aby pominąć monit, należy użyć parametru Force.</span><span class="sxs-lookup"><span data-stu-id="f38f0-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="f38f0-115">Jeśli do roli niestandardowej zostaną usunięte istniejące przypisania ról, usuwanie zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="f38f0-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="f38f0-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f38f0-116">EXAMPLES</span></span>

### <span data-ttu-id="f38f0-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f38f0-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="f38f0-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f38f0-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="f38f0-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f38f0-119">PARAMETERS</span></span>

### <span data-ttu-id="f38f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f38f0-120">-DefaultProfile</span></span>
<span data-ttu-id="f38f0-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f38f0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38f0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f38f0-122">-Force</span></span>
<span data-ttu-id="f38f0-123">Jeśli jest ustawiona, nie monituje o potwierdzenie przed usunięciem roli niestandardowej</span><span class="sxs-lookup"><span data-stu-id="f38f0-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="f38f0-124">-ID</span><span class="sxs-lookup"><span data-stu-id="f38f0-124">-Id</span></span>
<span data-ttu-id="f38f0-125">Identyfikator definicji roli do usunięcia</span><span class="sxs-lookup"><span data-stu-id="f38f0-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="f38f0-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f38f0-126">-InputObject</span></span>
<span data-ttu-id="f38f0-127">Obiekt reprezentujący definicję roli, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f38f0-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="f38f0-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f38f0-128">-Name</span></span>
<span data-ttu-id="f38f0-129">Nazwa definicji roli do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f38f0-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="f38f0-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f38f0-130">-PassThru</span></span>
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

### <span data-ttu-id="f38f0-131">-Zakres</span><span class="sxs-lookup"><span data-stu-id="f38f0-131">-Scope</span></span>
<span data-ttu-id="f38f0-132">Zakres definicji roli.</span><span class="sxs-lookup"><span data-stu-id="f38f0-132">Role definition scope.</span></span>

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

### <span data-ttu-id="f38f0-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f38f0-133">-Confirm</span></span>
<span data-ttu-id="f38f0-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f38f0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f38f0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f38f0-135">-WhatIf</span></span>
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

### <span data-ttu-id="f38f0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f38f0-136">CommonParameters</span></span>
<span data-ttu-id="f38f0-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f38f0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f38f0-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f38f0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f38f0-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f38f0-139">INPUTS</span></span>

### <span data-ttu-id="f38f0-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f38f0-140">System.Guid</span></span>

### <span data-ttu-id="f38f0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f38f0-141">System.String</span></span>

### <span data-ttu-id="f38f0-142">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f38f0-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="f38f0-143">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f38f0-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f38f0-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f38f0-144">OUTPUTS</span></span>

### <span data-ttu-id="f38f0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f38f0-145">System.Boolean</span></span>

## <span data-ttu-id="f38f0-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f38f0-146">NOTES</span></span>
<span data-ttu-id="f38f0-147">Słowa kluczowe: Azure, AZ, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="f38f0-147">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f38f0-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f38f0-148">RELATED LINKS</span></span>

[<span data-ttu-id="f38f0-149">Nowe — AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f38f0-149">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="f38f0-150">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f38f0-150">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="f38f0-151">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f38f0-151">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

