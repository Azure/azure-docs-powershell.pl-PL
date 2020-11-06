---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroup.md
ms.openlocfilehash: 20cfc2ef6b4b59e8cdd605dd14302aa1a172acb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524282"
---
# <span data-ttu-id="53737-101">New-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="53737-101">New-AzureRmManagementGroup</span></span>

## <span data-ttu-id="53737-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53737-102">SYNOPSIS</span></span>
<span data-ttu-id="53737-103">Tworzy grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="53737-103">Creates a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53737-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53737-104">SYNTAX</span></span>

### <span data-ttu-id="53737-105">GroupOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="53737-105">GroupOperations (Default)</span></span>
```
New-AzureRmManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53737-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="53737-106">ParentGroupObject</span></span>
```
New-AzureRmManagementGroup [-GroupName] <String> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53737-107">Opis</span><span class="sxs-lookup"><span data-stu-id="53737-107">DESCRIPTION</span></span>
<span data-ttu-id="53737-108">Polecenie cmdlet **New-AzureRMManagementGroup** tworzy grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="53737-108">The **New-AzureRMManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="53737-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53737-109">EXAMPLES</span></span>

### <span data-ttu-id="53737-110">Przykład 1. Tworzenie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="53737-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup"

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

<span data-ttu-id="53737-111">Tworzenie nowej grupy `DisplayName` i `ParentId` Ustawianie jej `null` .</span><span class="sxs-lookup"><span data-stu-id="53737-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="53737-112">Ta `DisplayName` Grupa będzie taka sama jak ta, `GroupName` a jej nadrzędna grupa będzie dzierżawą.</span><span class="sxs-lookup"><span data-stu-id="53737-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="53737-113">Przykład 2: Tworzenie grupy zarządzania o nazwie wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="53737-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

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

<span data-ttu-id="53737-114">W tym przypadku element nadrzędny grupy będzie dzierżawą, a w polu `DisplayName` zostanie ustawiona wartość podanej.</span><span class="sxs-lookup"><span data-stu-id="53737-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="53737-115">Przykład 3: Tworzenie grupy zarządzania z elementem nadrzędnym i nazwą wyświetlaną</span><span class="sxs-lookup"><span data-stu-id="53737-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

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

### <span data-ttu-id="53737-116">Przykład 4: Tworzenie grupy zarządzania z elementem nadrzędnym (przy użyciu obiektu nadrzędnego)</span><span class="sxs-lookup"><span data-stu-id="53737-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzureRmManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="53737-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53737-117">PARAMETERS</span></span>

### <span data-ttu-id="53737-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53737-118">-DefaultProfile</span></span>
<span data-ttu-id="53737-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53737-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53737-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="53737-120">-DisplayName</span></span>
<span data-ttu-id="53737-121">Nazwa wyświetlana grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="53737-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="53737-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="53737-122">-GroupName</span></span>
<span data-ttu-id="53737-123">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="53737-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53737-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="53737-124">-ParentId</span></span>
<span data-ttu-id="53737-125">Identyfikator elementu nadrzędnego grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="53737-125">Parent Id of the management group</span></span>

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

### <span data-ttu-id="53737-126">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="53737-126">-ParentObject</span></span>
<span data-ttu-id="53737-127">Obiekt nadrzędny</span><span class="sxs-lookup"><span data-stu-id="53737-127">Parent Object</span></span>

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

### <span data-ttu-id="53737-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53737-128">-Confirm</span></span>
<span data-ttu-id="53737-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53737-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53737-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53737-130">-WhatIf</span></span>
<span data-ttu-id="53737-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53737-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53737-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53737-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53737-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53737-133">CommonParameters</span></span>
<span data-ttu-id="53737-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53737-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53737-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53737-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53737-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53737-136">INPUTS</span></span>

### <span data-ttu-id="53737-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="53737-137">None</span></span>

## <span data-ttu-id="53737-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53737-138">OUTPUTS</span></span>

### <span data-ttu-id="53737-139">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="53737-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="53737-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53737-140">NOTES</span></span>

## <span data-ttu-id="53737-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53737-141">RELATED LINKS</span></span>

[<span data-ttu-id="53737-142">Remove-AzureRMManagementGroup</span><span class="sxs-lookup"><span data-stu-id="53737-142">Remove-AzureRMManagementGroup</span></span>](./Remove-AzureRMManagementGroup.md)

[<span data-ttu-id="53737-143">Update-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="53737-143">Update-AzureRmManagementGroup</span></span>](./Update-AzureRmManagementGroup.md)

[<span data-ttu-id="53737-144">Get-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="53737-144">Get-AzureRmManagementGroup</span></span>](./Get-AzureRmManagementGroup.md)
