---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: d65a94e104b7a5b3e5503b30aefe87fd7b1fa531
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894981"
---
# <span data-ttu-id="e1320-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1320-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="e1320-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1320-102">SYNOPSIS</span></span>
<span data-ttu-id="e1320-103">Aktualizuje grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="e1320-103">Updates a Management Group</span></span>

## <span data-ttu-id="e1320-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1320-104">SYNTAX</span></span>

### <span data-ttu-id="e1320-105">GroupOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e1320-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1320-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="e1320-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1320-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="e1320-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1320-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="e1320-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1320-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e1320-109">DESCRIPTION</span></span>
<span data-ttu-id="e1320-110">Polecenie cmdlet **Update-AzManagementGroup** aktualizuje **parentID** lub **DisplayName** grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e1320-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="e1320-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1320-111">EXAMPLES</span></span>

### <span data-ttu-id="e1320-112">Przykład 1: aktualizowanie nazwy wyświetlanej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="e1320-112">Example 1: Update a Management Group's Display Name</span></span>
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

### <span data-ttu-id="e1320-113">Przykład 2: aktualizowanie elementu nadrzędnego grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="e1320-113">Example 2: Update a Management Group's Parent</span></span>
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

### <span data-ttu-id="e1320-114">Przykład 3: aktualizowanie grupy zarządzania za pomocą obiektu PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1320-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
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

### <span data-ttu-id="e1320-115">Przykład 4: aktualizowanie elementu nadrzędnego grupy zarządzania przy użyciu obiektu Nadrzędnegoobject</span><span class="sxs-lookup"><span data-stu-id="e1320-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
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

## <span data-ttu-id="e1320-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1320-116">PARAMETERS</span></span>

### <span data-ttu-id="e1320-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1320-117">-DefaultProfile</span></span>
<span data-ttu-id="e1320-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1320-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1320-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e1320-119">-DisplayName</span></span>
<span data-ttu-id="e1320-120">Nazwa wyświetlana grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="e1320-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="e1320-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="e1320-121">-GroupName</span></span>
<span data-ttu-id="e1320-122">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="e1320-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1320-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e1320-123">-InputObject</span></span>
<span data-ttu-id="e1320-124">Obiekt wejściowy z rozmowy Get</span><span class="sxs-lookup"><span data-stu-id="e1320-124">Input Object from the Get call</span></span>

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

### <span data-ttu-id="e1320-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="e1320-125">-ParentId</span></span>
<span data-ttu-id="e1320-126">Identyfikator elementu nadrzędnego grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="e1320-126">Parent Id of the management group</span></span>

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

### <span data-ttu-id="e1320-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="e1320-127">-ParentObject</span></span>
<span data-ttu-id="e1320-128">Obiekt wejściowy z rozmowy Get</span><span class="sxs-lookup"><span data-stu-id="e1320-128">Input Object from the Get call</span></span>

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

### <span data-ttu-id="e1320-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1320-129">-Confirm</span></span>
<span data-ttu-id="e1320-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1320-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1320-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1320-131">-WhatIf</span></span>
<span data-ttu-id="e1320-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1320-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1320-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1320-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1320-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1320-134">CommonParameters</span></span>
<span data-ttu-id="e1320-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1320-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1320-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1320-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1320-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1320-137">INPUTS</span></span>

### <span data-ttu-id="e1320-138">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1320-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="e1320-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1320-139">OUTPUTS</span></span>

### <span data-ttu-id="e1320-140">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1320-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="e1320-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1320-141">NOTES</span></span>

## <span data-ttu-id="e1320-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1320-142">RELATED LINKS</span></span>
