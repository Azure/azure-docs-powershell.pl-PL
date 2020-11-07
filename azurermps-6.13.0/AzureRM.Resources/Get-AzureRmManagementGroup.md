---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagementGroup.md
ms.openlocfilehash: 275b13efa25bbffd2c104a1e9cfa3baf04fffe89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717603"
---
# <span data-ttu-id="6368f-101">Get-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6368f-101">Get-AzureRmManagementGroup</span></span>

## <span data-ttu-id="6368f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6368f-102">SYNOPSIS</span></span>
<span data-ttu-id="6368f-103">Pobiera grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6368f-103">Gets Management Group(s)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6368f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6368f-104">SYNTAX</span></span>

### <span data-ttu-id="6368f-105">ListOperation (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6368f-105">ListOperation (Default)</span></span>
```
Get-AzureRmManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6368f-106">Getoperation</span><span class="sxs-lookup"><span data-stu-id="6368f-106">GetOperation</span></span>
```
Get-AzureRmManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand]
 [-Recurse] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6368f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6368f-107">DESCRIPTION</span></span>
<span data-ttu-id="6368f-108">Polecenie cmdlet Get-AzureRMManagementGroup pobiera wszystkie lub określoną grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="6368f-108">The Get-AzureRMManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="6368f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6368f-109">EXAMPLES</span></span>

### <span data-ttu-id="6368f-110">Przykład 1: pobieranie wszystkich grup zarządzania</span><span class="sxs-lookup"><span data-stu-id="6368f-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzureRmManagementGroup

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

### <span data-ttu-id="6368f-111">Przykład 2: uzyskiwanie określonej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6368f-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzureRmManagementGroup -GroupName TestGroup

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

### <span data-ttu-id="6368f-112">Przykład 3: uzyskiwanie określonej grupy zarządzania i pierwszego poziomu hierarchii</span><span class="sxs-lookup"><span data-stu-id="6368f-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzureRmManagementGroup -GroupName TestGroupParent -Expand
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

<span data-ttu-id="6368f-113">Dzięki `Expand` fladze może poruszać się po `Children` tablicy i uzyskać szczegółowe informacje dotyczące poszczególnych elementów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="6368f-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="6368f-114">Na przykład `Children[0]` dane zostaną podane dla grupy z nazwą wyświetlaną `TestGroup1DisplayName` .</span><span class="sxs-lookup"><span data-stu-id="6368f-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="6368f-115">Przykład 4: uzyskiwanie określonej grupy zarządzania i wszystkich poziomów hiearchy</span><span class="sxs-lookup"><span data-stu-id="6368f-115">Example 4: Get specific Management Group and all levels of hiearchy</span></span>
```
PS C:\> $response = Get-AzureRmManagementGroup -GroupName TestGroupParent -Expand -Recurse
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

## <span data-ttu-id="6368f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6368f-116">PARAMETERS</span></span>

### <span data-ttu-id="6368f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6368f-117">-DefaultProfile</span></span>
<span data-ttu-id="6368f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6368f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6368f-119">-Expand</span><span class="sxs-lookup"><span data-stu-id="6368f-119">-Expand</span></span>
<span data-ttu-id="6368f-120">Rozwijanie wyników do listy elementów podrzędnych grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6368f-120">Expand the output to list the children of the management group</span></span>

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

### <span data-ttu-id="6368f-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="6368f-121">-GroupName</span></span>
<span data-ttu-id="6368f-122">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6368f-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6368f-123">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="6368f-123">-Recurse</span></span>
<span data-ttu-id="6368f-124">Cykliczne wyświetlanie listy elementów podrzędnych grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="6368f-124">Recursively list the children of the management group</span></span>

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

### <span data-ttu-id="6368f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6368f-125">-Confirm</span></span>
<span data-ttu-id="6368f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6368f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6368f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6368f-127">-WhatIf</span></span>
<span data-ttu-id="6368f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6368f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6368f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6368f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6368f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6368f-130">CommonParameters</span></span>
<span data-ttu-id="6368f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6368f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6368f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6368f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6368f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6368f-133">INPUTS</span></span>

### <span data-ttu-id="6368f-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6368f-134">None</span></span>

## <span data-ttu-id="6368f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6368f-135">OUTPUTS</span></span>

### <span data-ttu-id="6368f-136">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="6368f-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="6368f-137">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6368f-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6368f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6368f-138">NOTES</span></span>

## <span data-ttu-id="6368f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6368f-139">RELATED LINKS</span></span>
