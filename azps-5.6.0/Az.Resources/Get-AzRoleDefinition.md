---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 724daa3cce0bd8fe38a645fcdd3acd2d3ce7bf1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990781"
---
# <span data-ttu-id="1b6cd-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b6cd-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="1b6cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6cd-103">Lista wszystkich ról RBAC platformy Azure, które są dostępne do przypisania.</span><span class="sxs-lookup"><span data-stu-id="1b6cd-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="1b6cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1b6cd-104">SYNTAX</span></span>

### <span data-ttu-id="1b6cd-105">Zestaw RoleDefinitionNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1b6cd-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b6cd-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b6cd-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b6cd-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b6cd-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b6cd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1b6cd-108">DESCRIPTION</span></span>
<span data-ttu-id="1b6cd-109">Aby wyświetlić Get-AzRoleDefinition z określoną nazwą roli, użyj tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="1b6cd-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="1b6cd-110">Aby sprawdzić poszczególne operacje, do których rola udziela dostępu, przejrzyj właściwości Akcji i NotActions roli.</span><span class="sxs-lookup"><span data-stu-id="1b6cd-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="1b6cd-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1b6cd-111">EXAMPLES</span></span>

### <span data-ttu-id="1b6cd-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1b6cd-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="1b6cd-113">Uzyskiwanie definicji ról czytnika</span><span class="sxs-lookup"><span data-stu-id="1b6cd-113">Get the Reader role definition</span></span>

### <span data-ttu-id="1b6cd-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1b6cd-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="1b6cd-115">Lista wszystkich definicji ról RBAC</span><span class="sxs-lookup"><span data-stu-id="1b6cd-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="1b6cd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b6cd-116">PARAMETERS</span></span>

### <span data-ttu-id="1b6cd-117">— Niestandardowe</span><span class="sxs-lookup"><span data-stu-id="1b6cd-117">-Custom</span></span>
<span data-ttu-id="1b6cd-118">Jeśli jest to określone, wyświetla w katalogu tylko utworzone niestandardowe role.</span><span class="sxs-lookup"><span data-stu-id="1b6cd-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6cd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6cd-119">-DefaultProfile</span></span>
<span data-ttu-id="1b6cd-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1b6cd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b6cd-121">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="1b6cd-121">-Id</span></span>
<span data-ttu-id="1b6cd-122">Identyfikator definicji roli.</span><span class="sxs-lookup"><span data-stu-id="1b6cd-122">Role definition Id.</span></span>

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

### <span data-ttu-id="1b6cd-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1b6cd-123">-Name</span></span>
<span data-ttu-id="1b6cd-124">Nazwa definicji roli.</span><span class="sxs-lookup"><span data-stu-id="1b6cd-124">Role definition name.</span></span>
<span data-ttu-id="1b6cd-125">Na przykład dla czytnika, współautora, współautora maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="1b6cd-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6cd-126">— Zakres</span><span class="sxs-lookup"><span data-stu-id="1b6cd-126">-Scope</span></span>
<span data-ttu-id="1b6cd-127">Zakres definicji ról.</span><span class="sxs-lookup"><span data-stu-id="1b6cd-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6cd-128">CommonParameters</span></span>
<span data-ttu-id="1b6cd-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6cd-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b6cd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6cd-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b6cd-131">INPUTS</span></span>

### <span data-ttu-id="1b6cd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1b6cd-132">System.String</span></span>

### <span data-ttu-id="1b6cd-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1b6cd-133">System.Guid</span></span>

### <span data-ttu-id="1b6cd-134">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="1b6cd-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1b6cd-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b6cd-135">OUTPUTS</span></span>

### <span data-ttu-id="1b6cd-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b6cd-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="1b6cd-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1b6cd-137">NOTES</span></span>
<span data-ttu-id="1b6cd-138">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="1b6cd-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1b6cd-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b6cd-139">RELATED LINKS</span></span>

[<span data-ttu-id="1b6cd-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1b6cd-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="1b6cd-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1b6cd-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="1b6cd-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b6cd-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="1b6cd-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b6cd-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

