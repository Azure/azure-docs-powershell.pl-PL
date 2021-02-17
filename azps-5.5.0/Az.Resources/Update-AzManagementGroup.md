---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: bdef58db8dcda735a7a8c08350b806c9fd00cf21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178683"
---
# <span data-ttu-id="67fb0-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="67fb0-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="67fb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="67fb0-103">Aktualizacje grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="67fb0-103">Updates a Management Group</span></span>

## <span data-ttu-id="67fb0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67fb0-104">SYNTAX</span></span>

### <span data-ttu-id="67fb0-105">GroupOperations (Default)</span><span class="sxs-lookup"><span data-stu-id="67fb0-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67fb0-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="67fb0-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67fb0-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="67fb0-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67fb0-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="67fb0-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67fb0-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="67fb0-109">DESCRIPTION</span></span>
<span data-ttu-id="67fb0-110">Polecenie **cmdlet Update-AzManagementGroup** aktualizuje element **ParentId** lub **DisplayName** grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="67fb0-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="67fb0-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67fb0-111">EXAMPLES</span></span>

### <span data-ttu-id="67fb0-112">Przykład 1. Aktualizowanie nazwy wyświetlanej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="67fb0-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : New Display Name
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
```

### <span data-ttu-id="67fb0-113">Przykład 2. Aktualizowanie elementu nadrzędnego grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="67fb0-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="67fb0-114">Przykład 3. Aktualizowanie grupy zarządzania przez rurowe obiekty PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="67fb0-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Update-AzManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestDisplayName
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="67fb0-115">Przykład 4. Aktualizowanie elementu nadrzędnego grupy zarządzania przy użyciu elementu nadrzędnego</span><span class="sxs-lookup"><span data-stu-id="67fb0-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="67fb0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67fb0-116">PARAMETERS</span></span>

### <span data-ttu-id="67fb0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67fb0-117">-DefaultProfile</span></span>
<span data-ttu-id="67fb0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67fb0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67fb0-119">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="67fb0-119">-DisplayName</span></span>
<span data-ttu-id="67fb0-120">Nazwa wyświetlana grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="67fb0-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="67fb0-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="67fb0-121">-GroupName</span></span>
<span data-ttu-id="67fb0-122">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="67fb0-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67fb0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67fb0-123">-InputObject</span></span>
<span data-ttu-id="67fb0-124">Input Object from the Get call</span><span class="sxs-lookup"><span data-stu-id="67fb0-124">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67fb0-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="67fb0-125">-ParentId</span></span>
<span data-ttu-id="67fb0-126">Identyfikator nadrzędny grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="67fb0-126">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ManagementGroupObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67fb0-127">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="67fb0-127">-ParentObject</span></span>
<span data-ttu-id="67fb0-128">Input Object from the Get call</span><span class="sxs-lookup"><span data-stu-id="67fb0-128">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67fb0-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67fb0-129">-Confirm</span></span>
<span data-ttu-id="67fb0-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="67fb0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67fb0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67fb0-131">-WhatIf</span></span>
<span data-ttu-id="67fb0-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67fb0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67fb0-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="67fb0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67fb0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67fb0-134">CommonParameters</span></span>
<span data-ttu-id="67fb0-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67fb0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67fb0-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67fb0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67fb0-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67fb0-137">INPUTS</span></span>

### <span data-ttu-id="67fb0-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="67fb0-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="67fb0-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67fb0-139">OUTPUTS</span></span>

### <span data-ttu-id="67fb0-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="67fb0-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="67fb0-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67fb0-141">NOTES</span></span>

## <span data-ttu-id="67fb0-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67fb0-142">RELATED LINKS</span></span>
