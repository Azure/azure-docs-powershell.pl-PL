---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 7998772b1a8e6a510e1eaec5daefaf4203259ab2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895809"
---
# <span data-ttu-id="a52cf-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a52cf-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="a52cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a52cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a52cf-103">Tworzy grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="a52cf-103">Creates a Management Group</span></span>

## <span data-ttu-id="a52cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a52cf-104">SYNTAX</span></span>

### <span data-ttu-id="a52cf-105">GroupOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a52cf-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a52cf-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="a52cf-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a52cf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a52cf-107">DESCRIPTION</span></span>
<span data-ttu-id="a52cf-108">Polecenie cmdlet **New-AzManagementGroup** tworzy grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="a52cf-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="a52cf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a52cf-109">EXAMPLES</span></span>

### <span data-ttu-id="a52cf-110">Przykład 1. Tworzenie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="a52cf-110">Example 1: Create a Management Group</span></span>
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

<span data-ttu-id="a52cf-111">Tworzenie nowej grupy `DisplayName` i `ParentId` Ustawianie jej `null` .</span><span class="sxs-lookup"><span data-stu-id="a52cf-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="a52cf-112">Ta `DisplayName` Grupa będzie taka sama jak ta, `GroupName` a jej nadrzędna grupa będzie dzierżawą.</span><span class="sxs-lookup"><span data-stu-id="a52cf-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="a52cf-113">Przykład 2: Tworzenie grupy zarządzania o nazwie wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="a52cf-113">Example 2: Create a Management Group with a display name</span></span>
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

<span data-ttu-id="a52cf-114">W tym przypadku element nadrzędny grupy będzie dzierżawą, a w polu `DisplayName` zostanie ustawiona wartość podanej.</span><span class="sxs-lookup"><span data-stu-id="a52cf-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="a52cf-115">Przykład 3: Tworzenie grupy zarządzania z elementem nadrzędnym i nazwą wyświetlaną</span><span class="sxs-lookup"><span data-stu-id="a52cf-115">Example 3: Create a Management Group with a parent and a display name</span></span>
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

### <span data-ttu-id="a52cf-116">Przykład 4: Tworzenie grupy zarządzania z elementem nadrzędnym (przy użyciu obiektu nadrzędnego)</span><span class="sxs-lookup"><span data-stu-id="a52cf-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
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

## <span data-ttu-id="a52cf-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a52cf-117">PARAMETERS</span></span>

### <span data-ttu-id="a52cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52cf-118">-DefaultProfile</span></span>
<span data-ttu-id="a52cf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a52cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a52cf-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a52cf-120">-DisplayName</span></span>
<span data-ttu-id="a52cf-121">Nazwa wyświetlana grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="a52cf-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="a52cf-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a52cf-122">-GroupName</span></span>
<span data-ttu-id="a52cf-123">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="a52cf-123">Management Group Id</span></span>

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

### <span data-ttu-id="a52cf-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="a52cf-124">-ParentId</span></span>
<span data-ttu-id="a52cf-125">Identyfikator elementu nadrzędnego grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="a52cf-125">Parent Id of the management group</span></span>

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

### <span data-ttu-id="a52cf-126">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="a52cf-126">-ParentObject</span></span>
<span data-ttu-id="a52cf-127">Obiekt nadrzędny</span><span class="sxs-lookup"><span data-stu-id="a52cf-127">Parent Object</span></span>

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

### <span data-ttu-id="a52cf-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a52cf-128">-Confirm</span></span>
<span data-ttu-id="a52cf-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a52cf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a52cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a52cf-130">-WhatIf</span></span>
<span data-ttu-id="a52cf-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a52cf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a52cf-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a52cf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a52cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52cf-133">CommonParameters</span></span>
<span data-ttu-id="a52cf-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52cf-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a52cf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52cf-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a52cf-136">INPUTS</span></span>

### <span data-ttu-id="a52cf-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a52cf-137">None</span></span>

## <span data-ttu-id="a52cf-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a52cf-138">OUTPUTS</span></span>

### <span data-ttu-id="a52cf-139">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a52cf-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="a52cf-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a52cf-140">NOTES</span></span>

## <span data-ttu-id="a52cf-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a52cf-141">RELATED LINKS</span></span>

[<span data-ttu-id="a52cf-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a52cf-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="a52cf-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a52cf-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="a52cf-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a52cf-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)