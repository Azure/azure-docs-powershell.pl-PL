---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 741b182f6da1b9afc3433e5a79b3f174f239af23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008625"
---
# <span data-ttu-id="2a81d-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2a81d-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="2a81d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a81d-102">SYNOPSIS</span></span>
<span data-ttu-id="2a81d-103">Tworzy grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="2a81d-103">Creates a Management Group</span></span>

## <span data-ttu-id="2a81d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2a81d-104">SYNTAX</span></span>

### <span data-ttu-id="2a81d-105">GroupOperations (Default)</span><span class="sxs-lookup"><span data-stu-id="2a81d-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a81d-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="2a81d-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a81d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2a81d-107">DESCRIPTION</span></span>
<span data-ttu-id="2a81d-108">Polecenie **cmdlet New-AzManagementGroup** tworzy grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="2a81d-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="2a81d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2a81d-109">EXAMPLES</span></span>

### <span data-ttu-id="2a81d-110">Przykład 1. Tworzenie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="2a81d-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="2a81d-111">Tworzenie nowej grupy z `DisplayName` `ParentId` ustawieniem `null` .</span><span class="sxs-lookup"><span data-stu-id="2a81d-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="2a81d-112">Będzie taki sam jak element nadrzędny grupy i `DisplayName` `GroupName` będzie dzierżawą.</span><span class="sxs-lookup"><span data-stu-id="2a81d-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="2a81d-113">Przykład 2. Tworzenie grupy zarządzania z nazwą wyświetlaną</span><span class="sxs-lookup"><span data-stu-id="2a81d-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="2a81d-114">W tym przypadku element nadrzędny grupy będzie dzierżawą i zostanie ustawiona `DisplayName` wartość.</span><span class="sxs-lookup"><span data-stu-id="2a81d-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="2a81d-115">Przykład 3. Tworzenie grupy zarządzania z elementem nadrzędnym i nazwą wyświetlaną</span><span class="sxs-lookup"><span data-stu-id="2a81d-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="2a81d-116">Przykład 4. Tworzenie grupy zarządzania z elementem nadrzędnym (przy użyciu obiektu nadrzędnego)</span><span class="sxs-lookup"><span data-stu-id="2a81d-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="2a81d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a81d-117">PARAMETERS</span></span>

### <span data-ttu-id="2a81d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a81d-118">-DefaultProfile</span></span>
<span data-ttu-id="2a81d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a81d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a81d-120">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="2a81d-120">-DisplayName</span></span>
<span data-ttu-id="2a81d-121">Nazwa wyświetlana grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="2a81d-121">Display Name of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a81d-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="2a81d-122">-GroupName</span></span>
<span data-ttu-id="2a81d-123">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="2a81d-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a81d-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="2a81d-124">-ParentId</span></span>
<span data-ttu-id="2a81d-125">Identyfikator nadrzędny grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="2a81d-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a81d-126">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="2a81d-126">-ParentObject</span></span>
<span data-ttu-id="2a81d-127">Obiekt nadrzędny</span><span class="sxs-lookup"><span data-stu-id="2a81d-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a81d-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a81d-128">-Confirm</span></span>
<span data-ttu-id="2a81d-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2a81d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a81d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a81d-130">-WhatIf</span></span>
<span data-ttu-id="2a81d-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a81d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a81d-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2a81d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a81d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a81d-133">CommonParameters</span></span>
<span data-ttu-id="2a81d-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a81d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a81d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a81d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a81d-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a81d-136">INPUTS</span></span>

### <span data-ttu-id="2a81d-137">Brak</span><span class="sxs-lookup"><span data-stu-id="2a81d-137">None</span></span>

## <span data-ttu-id="2a81d-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a81d-138">OUTPUTS</span></span>

### <span data-ttu-id="2a81d-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2a81d-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="2a81d-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2a81d-140">NOTES</span></span>

## <span data-ttu-id="2a81d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a81d-141">RELATED LINKS</span></span>

[<span data-ttu-id="2a81d-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2a81d-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="2a81d-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2a81d-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="2a81d-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2a81d-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)