---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: 6b646e22ff32d9fe361cdedd6dbb6fa5c9fba270
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010842"
---
# <span data-ttu-id="e659e-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="e659e-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="e659e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e659e-102">SYNOPSIS</span></span>
<span data-ttu-id="e659e-103">Pobierz co najmniej jedną definicję planu.</span><span class="sxs-lookup"><span data-stu-id="e659e-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="e659e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e659e-104">SYNTAX</span></span>

### <span data-ttu-id="e659e-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e659e-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e659e-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="e659e-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e659e-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="e659e-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e659e-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="e659e-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e659e-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="e659e-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e659e-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="e659e-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e659e-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="e659e-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e659e-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="e659e-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e659e-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="e659e-113">DESCRIPTION</span></span>
<span data-ttu-id="e659e-114">Pobierz co najmniej jedną definicję planu.</span><span class="sxs-lookup"><span data-stu-id="e659e-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="e659e-115">Definicje planu istnieją w grupie zarządzania lub w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e659e-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="e659e-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e659e-116">EXAMPLES</span></span>

### <span data-ttu-id="e659e-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e659e-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="e659e-118">Pobierz definicje planu w ramach bieżącej subskrypcji i hierarchię grup zarządzania subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e659e-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="e659e-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e659e-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
ManagementGroupId    : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="e659e-120">Pobierz definicje planu w obrębie określonej grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e659e-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="e659e-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e659e-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="e659e-122">Pobierz definicje planu w ramach określonej subskrypcji i hierarchię grup zarządzania subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e659e-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="e659e-123">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="e659e-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="e659e-124">Pobierz definicję planu z nazwą podaną w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e659e-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="e659e-125">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="e659e-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="e659e-126">Pobierz definicję planu z podaną nazwą i wersją w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e659e-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="e659e-127">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="e659e-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="e659e-128">Pobierz najnowszą opublikowaną definicję planu z podaną nazwą w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e659e-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="e659e-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e659e-129">PARAMETERS</span></span>

### <span data-ttu-id="e659e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e659e-130">-DefaultProfile</span></span>
<span data-ttu-id="e659e-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e659e-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e659e-132">- LatestPublished</span><span class="sxs-lookup"><span data-stu-id="e659e-132">-LatestPublished</span></span>
<span data-ttu-id="e659e-133">Flaga definicji planu z najnowszą opublikowaną flagą.</span><span class="sxs-lookup"><span data-stu-id="e659e-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="e659e-134">Po jej skonfigurowaniu wykonanie zwraca najnowszą opublikowaną wersję definicji planu.</span><span class="sxs-lookup"><span data-stu-id="e659e-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="e659e-135">Wartość domyślna to false( fałsz).</span><span class="sxs-lookup"><span data-stu-id="e659e-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e659e-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e659e-136">-ManagementGroupId</span></span>
<span data-ttu-id="e659e-137">Identyfikator grupy zarządzania, w którym jest zapisywana definicja planu.</span><span class="sxs-lookup"><span data-stu-id="e659e-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e659e-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e659e-138">-Name</span></span>
<span data-ttu-id="e659e-139">Nazwa definicji planu.</span><span class="sxs-lookup"><span data-stu-id="e659e-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e659e-140">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e659e-140">-SubscriptionId</span></span>
<span data-ttu-id="e659e-141">Identyfikator subskrypcji, w którym jest zapisywana definicja planu.</span><span class="sxs-lookup"><span data-stu-id="e659e-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e659e-142">— Wersja</span><span class="sxs-lookup"><span data-stu-id="e659e-142">-Version</span></span>
<span data-ttu-id="e659e-143">Opublikowano wersję definicji planu.</span><span class="sxs-lookup"><span data-stu-id="e659e-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e659e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e659e-144">CommonParameters</span></span>
<span data-ttu-id="e659e-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e659e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e659e-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e659e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e659e-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e659e-147">INPUTS</span></span>

### <span data-ttu-id="e659e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e659e-148">System.String</span></span>

## <span data-ttu-id="e659e-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e659e-149">OUTPUTS</span></span>

### <span data-ttu-id="e659e-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="e659e-150">System.Object</span></span>
## <span data-ttu-id="e659e-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e659e-151">NOTES</span></span>

## <span data-ttu-id="e659e-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e659e-152">RELATED LINKS</span></span>
