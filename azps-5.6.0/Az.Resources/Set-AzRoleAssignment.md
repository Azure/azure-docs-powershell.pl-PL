---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 785ddf5dac50a84c678ea995a3b948702b60195b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995982"
---
# <span data-ttu-id="37935-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37935-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="37935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37935-102">SYNOPSIS</span></span>
<span data-ttu-id="37935-103">Aktualizowanie istniejącego przydziału roli.</span><span class="sxs-lookup"><span data-stu-id="37935-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="37935-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37935-104">SYNTAX</span></span>

### <span data-ttu-id="37935-105">RoleAssignmentParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="37935-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37935-106">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="37935-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37935-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="37935-107">DESCRIPTION</span></span>
<span data-ttu-id="37935-108">Użyj polecenia New-AzRoleAssignment, aby zmodyfikować istniejące przypisanie.</span><span class="sxs-lookup"><span data-stu-id="37935-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="37935-109">Opisy mogą być dowolnym prawidłowym ciągiem.</span><span class="sxs-lookup"><span data-stu-id="37935-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="37935-110">Jeśli warunek jest ustawiony, należy również ustawić wersję warunku, ale jeśli aktualizujesz warunek, który nie jest konieczny.</span><span class="sxs-lookup"><span data-stu-id="37935-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="37935-111">Wersję warunku można uaktualnić z wersji 1.0 do 2.0, ale nie można jej ponownie obniżyć.</span><span class="sxs-lookup"><span data-stu-id="37935-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="37935-112">Należy zachować ostrożność, ponieważ program 2.0 nie jest niezgodny z programem 1.0.</span><span class="sxs-lookup"><span data-stu-id="37935-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="37935-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37935-113">EXAMPLES</span></span>

### <span data-ttu-id="37935-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37935-114">Example 1</span></span>
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="37935-115">Aktualizowanie istniejącego przydziału roli przez modyfikowanie obiektu</span><span class="sxs-lookup"><span data-stu-id="37935-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="37935-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="37935-116">Example 2</span></span>
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="37935-117">Aktualizowanie istniejącego przydziału ról przy użyciu pliku</span><span class="sxs-lookup"><span data-stu-id="37935-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="37935-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37935-118">PARAMETERS</span></span>

### <span data-ttu-id="37935-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37935-119">-DefaultProfile</span></span>
<span data-ttu-id="37935-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="37935-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37935-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="37935-121">-InputFile</span></span>
<span data-ttu-id="37935-122">Nazwa pliku zawierająca jedną definicję roli.</span><span class="sxs-lookup"><span data-stu-id="37935-122">File name containing a single role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37935-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37935-123">-InputObject</span></span>
<span data-ttu-id="37935-124">Przypisanie roli.</span><span class="sxs-lookup"><span data-stu-id="37935-124">Role Assignment.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37935-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37935-125">-PassThru</span></span>
<span data-ttu-id="37935-126">Jeśli jest określona, wyświetla zaktualizowane przypisanie roli.</span><span class="sxs-lookup"><span data-stu-id="37935-126">If specified, displays the updated role assignment</span></span>

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

### <span data-ttu-id="37935-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37935-127">-Confirm</span></span>
<span data-ttu-id="37935-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37935-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37935-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37935-129">-WhatIf</span></span>
<span data-ttu-id="37935-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37935-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37935-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37935-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37935-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37935-132">CommonParameters</span></span>
<span data-ttu-id="37935-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37935-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37935-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37935-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37935-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37935-135">INPUTS</span></span>

### <span data-ttu-id="37935-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37935-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="37935-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37935-137">OUTPUTS</span></span>

### <span data-ttu-id="37935-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37935-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="37935-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37935-139">NOTES</span></span>

## <span data-ttu-id="37935-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37935-140">RELATED LINKS</span></span>
