---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: bdccb01293f60c876470d2ac443c8e85f354e2d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708252"
---
# <span data-ttu-id="3e6b9-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e6b9-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="3e6b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6b9-103">Aktualizuje grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="3e6b9-103">Updates a Management Group</span></span>

## <span data-ttu-id="3e6b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e6b9-104">SYNTAX</span></span>

### <span data-ttu-id="3e6b9-105">GroupOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e6b9-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e6b9-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="3e6b9-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e6b9-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="3e6b9-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e6b9-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="3e6b9-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e6b9-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3e6b9-109">DESCRIPTION</span></span>
<span data-ttu-id="3e6b9-110">Polecenie cmdlet **Update-AzManagementGroup** aktualizuje **parentID** lub **DisplayName** grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="3e6b9-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="3e6b9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e6b9-111">EXAMPLES</span></span>

### <span data-ttu-id="3e6b9-112">Przykład 1: aktualizowanie nazwy wyświetlanej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="3e6b9-112">Example 1: Update a Management Group's Display Name</span></span>
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

### <span data-ttu-id="3e6b9-113">Przykład 2: aktualizowanie elementu nadrzędnego grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="3e6b9-113">Example 2: Update a Management Group's Parent</span></span>
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

### <span data-ttu-id="3e6b9-114">Przykład 3: aktualizowanie grupy zarządzania za pomocą obiektu PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e6b9-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
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

### <span data-ttu-id="3e6b9-115">Przykład 4: aktualizowanie elementu nadrzędnego grupy zarządzania przy użyciu obiektu Nadrzędnegoobject</span><span class="sxs-lookup"><span data-stu-id="3e6b9-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
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

## <span data-ttu-id="3e6b9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e6b9-116">PARAMETERS</span></span>

### <span data-ttu-id="3e6b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6b9-117">-DefaultProfile</span></span>
<span data-ttu-id="3e6b9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e6b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e6b9-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3e6b9-119">-DisplayName</span></span>
<span data-ttu-id="3e6b9-120">Nazwa wyświetlana grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="3e6b9-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="3e6b9-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="3e6b9-121">-GroupName</span></span>
<span data-ttu-id="3e6b9-122">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="3e6b9-122">Management Group Id</span></span>

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

### <span data-ttu-id="3e6b9-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3e6b9-123">-InputObject</span></span>
<span data-ttu-id="3e6b9-124">Obiekt wejściowy z rozmowy Get</span><span class="sxs-lookup"><span data-stu-id="3e6b9-124">Input Object from the Get call</span></span>

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

### <span data-ttu-id="3e6b9-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="3e6b9-125">-ParentId</span></span>
<span data-ttu-id="3e6b9-126">Identyfikator elementu nadrzędnego grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="3e6b9-126">Parent Id of the management group</span></span>

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

### <span data-ttu-id="3e6b9-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="3e6b9-127">-ParentObject</span></span>
<span data-ttu-id="3e6b9-128">Obiekt wejściowy z rozmowy Get</span><span class="sxs-lookup"><span data-stu-id="3e6b9-128">Input Object from the Get call</span></span>

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

### <span data-ttu-id="3e6b9-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e6b9-129">-Confirm</span></span>
<span data-ttu-id="3e6b9-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e6b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e6b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e6b9-131">-WhatIf</span></span>
<span data-ttu-id="3e6b9-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e6b9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e6b9-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e6b9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e6b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6b9-134">CommonParameters</span></span>
<span data-ttu-id="3e6b9-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6b9-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e6b9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6b9-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e6b9-137">INPUTS</span></span>

### <span data-ttu-id="3e6b9-138">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e6b9-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="3e6b9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e6b9-139">OUTPUTS</span></span>

### <span data-ttu-id="3e6b9-140">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e6b9-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="3e6b9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e6b9-141">NOTES</span></span>

## <span data-ttu-id="3e6b9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e6b9-142">RELATED LINKS</span></span>