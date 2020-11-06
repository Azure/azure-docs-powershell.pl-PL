---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: ae4f8e11ac213943d8cfcec162b43abde60fe753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551628"
---
# <span data-ttu-id="b441d-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b441d-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="b441d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b441d-102">SYNOPSIS</span></span>
<span data-ttu-id="b441d-103">Usuwa rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b441d-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="b441d-104">Rola do usunięcia jest określona przy użyciu właściwości ID roli.</span><span class="sxs-lookup"><span data-stu-id="b441d-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="b441d-105">Usunięcie nie powiedzie się, jeśli istnieją przypisania ról wprowadzone do roli niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="b441d-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b441d-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b441d-106">SYNTAX</span></span>

### <span data-ttu-id="b441d-107">RoleDefinitionIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b441d-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b441d-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b441d-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b441d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b441d-109">DESCRIPTION</span></span>
<span data-ttu-id="b441d-110">Polecenie cmdlet Remove-AzureRmRoleDefinition usuwa rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="b441d-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="b441d-111">Podaj parametr identyfikatora istniejącej roli niestandardowej, aby usunąć tę rolę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="b441d-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="b441d-112">Domyślnie Remove-AzureRmRoleDefinition monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b441d-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="b441d-113">Aby pominąć monit, należy użyć parametru Force.</span><span class="sxs-lookup"><span data-stu-id="b441d-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="b441d-114">Jeśli do roli niestandardowej zostaną usunięte istniejące przypisania ról, usuwanie zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="b441d-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="b441d-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b441d-115">EXAMPLES</span></span>

### <span data-ttu-id="b441d-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b441d-116">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="b441d-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b441d-117">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="b441d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b441d-118">PARAMETERS</span></span>

### <span data-ttu-id="b441d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b441d-119">-DefaultProfile</span></span>
<span data-ttu-id="b441d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b441d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b441d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b441d-121">-Force</span></span>
<span data-ttu-id="b441d-122">Jeśli jest ustawiona, nie monituje o potwierdzenie przed usunięciem roli niestandardowej</span><span class="sxs-lookup"><span data-stu-id="b441d-122">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="b441d-123">-ID</span><span class="sxs-lookup"><span data-stu-id="b441d-123">-Id</span></span>
<span data-ttu-id="b441d-124">Identyfikator definicji roli do usunięcia</span><span class="sxs-lookup"><span data-stu-id="b441d-124">Id of the Role definition to be deleted</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b441d-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b441d-125">-Name</span></span>
<span data-ttu-id="b441d-126">Nazwa definicji roli do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b441d-126">Name of the Role definition to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b441d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b441d-127">-PassThru</span></span>
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

### <span data-ttu-id="b441d-128">-Zakres</span><span class="sxs-lookup"><span data-stu-id="b441d-128">-Scope</span></span>
<span data-ttu-id="b441d-129">Zakres definicji roli.</span><span class="sxs-lookup"><span data-stu-id="b441d-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b441d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b441d-130">-Confirm</span></span>
<span data-ttu-id="b441d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b441d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b441d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b441d-132">-WhatIf</span></span>
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

### <span data-ttu-id="b441d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b441d-133">CommonParameters</span></span>
<span data-ttu-id="b441d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b441d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b441d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b441d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b441d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b441d-136">INPUTS</span></span>

### <span data-ttu-id="b441d-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b441d-137">None</span></span>
<span data-ttu-id="b441d-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b441d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b441d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b441d-139">OUTPUTS</span></span>

### <span data-ttu-id="b441d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b441d-140">System.Boolean</span></span>

## <span data-ttu-id="b441d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b441d-141">NOTES</span></span>
<span data-ttu-id="b441d-142">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="b441d-142">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b441d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b441d-143">RELATED LINKS</span></span>

[<span data-ttu-id="b441d-144">Nowe — AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b441d-144">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="b441d-145">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b441d-145">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="b441d-146">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b441d-146">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

