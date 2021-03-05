---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: 4686941a744532ad8d6f48e079e8120b6d6b3a53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985629"
---
# <span data-ttu-id="12441-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="12441-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="12441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12441-102">SYNOPSIS</span></span>
<span data-ttu-id="12441-103">Pobiera grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="12441-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="12441-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="12441-104">SYNTAX</span></span>

### <span data-ttu-id="12441-105">ListOperation (Default)</span><span class="sxs-lookup"><span data-stu-id="12441-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12441-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="12441-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12441-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="12441-107">DESCRIPTION</span></span>
<span data-ttu-id="12441-108">Polecenie Get-AzManagementGroup pobiera wszystkie lub konkretną grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="12441-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="12441-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="12441-109">EXAMPLES</span></span>

### <span data-ttu-id="12441-110">Przykład 1. Pobierz wszystkie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="12441-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzManagementGroup

Id          : /providers/Microsoft.Management/managementGroups/TestGroup
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroup
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupDisplayName

Id          : /providers/Microsoft.Management/managementGroups/TestGroupChild
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroupChild
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupChildDisplayName
```

### <span data-ttu-id="12441-111">Przykład 2. Uzyskiwanie konkretnej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="12441-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName TestGroup

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="12441-112">Przykład 3. Uzyskiwanie konkretnej grupy zarządzania i pierwszego poziomu hierarchii</span><span class="sxs-lookup"><span data-stu-id="12441-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzManagementGroup -GroupName TestGroupParent -Expand
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    :
```

<span data-ttu-id="12441-113">Flagą można poruszać się po tablicy i `Expand` uzyskać szczegółowe informacje dotyczące każdego `Children` dziecka.</span><span class="sxs-lookup"><span data-stu-id="12441-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="12441-114">Na przykład `Children[0]` poda nazwę wyświetlaną `TestGroup1DisplayName` grupy.</span><span class="sxs-lookup"><span data-stu-id="12441-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="12441-115">Przykład 4. Uzyskiwanie konkretnej grupy zarządzania i wszystkich poziomów hierarchii</span><span class="sxs-lookup"><span data-stu-id="12441-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
```
PS C:\> $response = Get-AzManagementGroup -GroupName TestGroupParent -Expand -Recurse
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    : {TestRecurseChild}

PS C:\> $response.Children[0].Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestRecurseChild
Name        : TestRecurseChild
DisplayName : TestRecurseChild
Children    :
```

## <span data-ttu-id="12441-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12441-116">PARAMETERS</span></span>

### <span data-ttu-id="12441-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12441-117">-DefaultProfile</span></span>
<span data-ttu-id="12441-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="12441-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12441-119">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="12441-119">-Expand</span></span>
<span data-ttu-id="12441-120">Rozwiń dane wyjściowe, aby wyświetlić listę dzieci grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="12441-120">Expand the output to list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12441-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="12441-121">-GroupName</span></span>
<span data-ttu-id="12441-122">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="12441-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12441-123">- Rekurencie</span><span class="sxs-lookup"><span data-stu-id="12441-123">-Recurse</span></span>
<span data-ttu-id="12441-124">Rekurencyjnie lista dzieci grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="12441-124">Recursively list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12441-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12441-125">-Confirm</span></span>
<span data-ttu-id="12441-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="12441-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12441-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12441-127">-WhatIf</span></span>
<span data-ttu-id="12441-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12441-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12441-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="12441-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12441-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12441-130">CommonParameters</span></span>
<span data-ttu-id="12441-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12441-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12441-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12441-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12441-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12441-133">INPUTS</span></span>

### <span data-ttu-id="12441-134">Brak</span><span class="sxs-lookup"><span data-stu-id="12441-134">None</span></span>

## <span data-ttu-id="12441-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12441-135">OUTPUTS</span></span>

### <span data-ttu-id="12441-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="12441-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="12441-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="12441-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="12441-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="12441-138">NOTES</span></span>

## <span data-ttu-id="12441-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12441-139">RELATED LINKS</span></span>
