---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmManagementGroup.md
ms.openlocfilehash: 2542740db9cb8f5b0809bf071e2b960ba8979de8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543472"
---
# <span data-ttu-id="84831-101">Update-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84831-101">Update-AzureRmManagementGroup</span></span>

## <span data-ttu-id="84831-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84831-102">SYNOPSIS</span></span>
<span data-ttu-id="84831-103">Aktualizuje grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="84831-103">Updates a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84831-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84831-104">SYNTAX</span></span>

### <span data-ttu-id="84831-105">GroupOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="84831-105">GroupOperations (Default)</span></span>
```
Update-AzureRmManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84831-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="84831-106">ParentAndManagementGroupObject</span></span>
```
Update-AzureRmManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84831-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="84831-107">ManagementGroupObject</span></span>
```
Update-AzureRmManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84831-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="84831-108">ParentGroupObject</span></span>
```
Update-AzureRmManagementGroup -GroupName <String> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84831-109">Opis</span><span class="sxs-lookup"><span data-stu-id="84831-109">DESCRIPTION</span></span>
<span data-ttu-id="84831-110">Polecenie cmdlet **Update-AzureRMManagementGroup** aktualizuje **parentID** lub **DisplayName** grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="84831-110">The **Update-AzureRMManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="84831-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84831-111">EXAMPLES</span></span>

### <span data-ttu-id="84831-112">Przykład 1: aktualizowanie nazwy wyświetlanej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="84831-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzureRMManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

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

### <span data-ttu-id="84831-113">Przykład 2: aktualizowanie elementu nadrzędnego grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="84831-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzureRMManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

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

### <span data-ttu-id="84831-114">Przykład 3: aktualizowanie grupy zarządzania za pomocą obiektu PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84831-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzureRmManagementGroup -GroupName "TestGroup" | Update-AzureRMManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

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

### <span data-ttu-id="84831-115">Przykład 4: aktualizowanie elementu nadrzędnego grupy zarządzania przy użyciu obiektu Nadrzędnegoobject</span><span class="sxs-lookup"><span data-stu-id="84831-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzureRmManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzureRmManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="84831-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84831-116">PARAMETERS</span></span>

### <span data-ttu-id="84831-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84831-117">-DefaultProfile</span></span>
<span data-ttu-id="84831-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84831-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84831-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="84831-119">-DisplayName</span></span>
<span data-ttu-id="84831-120">Nazwa wyświetlana grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="84831-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="84831-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="84831-121">-GroupName</span></span>
<span data-ttu-id="84831-122">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="84831-122">Management Group Id</span></span>

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

### <span data-ttu-id="84831-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84831-123">-InputObject</span></span>
<span data-ttu-id="84831-124">Obiekt wejściowy z rozmowy Get</span><span class="sxs-lookup"><span data-stu-id="84831-124">Input Object from the Get call</span></span>

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

### <span data-ttu-id="84831-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="84831-125">-ParentId</span></span>
<span data-ttu-id="84831-126">Identyfikator elementu nadrzędnego grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="84831-126">Parent Id of the management group</span></span>

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

### <span data-ttu-id="84831-127">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="84831-127">-ParentObject</span></span>
<span data-ttu-id="84831-128">Obiekt wejściowy z rozmowy Get</span><span class="sxs-lookup"><span data-stu-id="84831-128">Input Object from the Get call</span></span>

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

### <span data-ttu-id="84831-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84831-129">-Confirm</span></span>
<span data-ttu-id="84831-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84831-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84831-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84831-131">-WhatIf</span></span>
<span data-ttu-id="84831-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84831-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84831-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84831-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84831-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84831-134">CommonParameters</span></span>
<span data-ttu-id="84831-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84831-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84831-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84831-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84831-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84831-137">INPUTS</span></span>

### <span data-ttu-id="84831-138">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84831-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="84831-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="84831-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="84831-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84831-140">OUTPUTS</span></span>

### <span data-ttu-id="84831-141">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="84831-141">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="84831-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84831-142">NOTES</span></span>

## <span data-ttu-id="84831-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84831-143">RELATED LINKS</span></span>
