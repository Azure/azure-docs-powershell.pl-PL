---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062950"
---
# <span data-ttu-id="da993-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="da993-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="da993-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da993-102">SYNOPSIS</span></span>
<span data-ttu-id="da993-103">Pobierz co najmniej jeden z definicji planów.</span><span class="sxs-lookup"><span data-stu-id="da993-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="da993-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da993-104">SYNTAX</span></span>

### <span data-ttu-id="da993-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da993-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da993-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="da993-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da993-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="da993-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da993-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="da993-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da993-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="da993-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da993-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="da993-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da993-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="da993-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da993-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="da993-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da993-113">Opis</span><span class="sxs-lookup"><span data-stu-id="da993-113">DESCRIPTION</span></span>
<span data-ttu-id="da993-114">Pobierz co najmniej jeden z definicji planów.</span><span class="sxs-lookup"><span data-stu-id="da993-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="da993-115">Definicje planów istnieją w grupie zarządzania lub w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da993-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="da993-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da993-116">EXAMPLES</span></span>

### <span data-ttu-id="da993-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da993-117">Example 1</span></span>
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

<span data-ttu-id="da993-118">Pobierz definicje planów w ramach bieżącego abonamentu i hierarchii grupy zarządzania subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da993-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="da993-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="da993-119">Example 2</span></span>
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

<span data-ttu-id="da993-120">Pobierz definicje planów w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="da993-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="da993-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="da993-121">Example 3</span></span>
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

<span data-ttu-id="da993-122">Pobieranie definicji planów w ramach określonego abonamentu i hierarchii grupy zarządzania subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da993-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="da993-123">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="da993-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="da993-124">Zapoznaj się z definicją plany o podanej nazwie w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da993-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="da993-125">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="da993-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="da993-126">Pobierz definicję plany o podaną nazwę i wersję w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="da993-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="da993-127">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="da993-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="da993-128">Uzyskaj najnowszą opublikowaną definicję usługi o podanej nazwie w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="da993-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="da993-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da993-129">PARAMETERS</span></span>

### <span data-ttu-id="da993-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da993-130">-DefaultProfile</span></span>
<span data-ttu-id="da993-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da993-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da993-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="da993-132">-LatestPublished</span></span>
<span data-ttu-id="da993-133">Najnowsza opublikowana flaga definicji planów.</span><span class="sxs-lookup"><span data-stu-id="da993-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="da993-134">Po ustawieniu funkcja wykonywanie zwraca najnowszą opublikowaną wersję definicji.</span><span class="sxs-lookup"><span data-stu-id="da993-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="da993-135">Wartość domyślna to FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="da993-135">Defaults to false.</span></span>

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

### <span data-ttu-id="da993-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="da993-136">-ManagementGroupId</span></span>
<span data-ttu-id="da993-137">Identyfikator grupy zarządzania, gdzie jest zapisywana definicja programu.</span><span class="sxs-lookup"><span data-stu-id="da993-137">Management Group Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="da993-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da993-138">-Name</span></span>
<span data-ttu-id="da993-139">Nazwa definicji plany.</span><span class="sxs-lookup"><span data-stu-id="da993-139">Blueprint definition name.</span></span>

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

### <span data-ttu-id="da993-140">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="da993-140">-SubscriptionId</span></span>
<span data-ttu-id="da993-141">Identyfikator abonamentu, w którym jest zapisywana definicja programu.</span><span class="sxs-lookup"><span data-stu-id="da993-141">Subscription Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="da993-142">-Version</span><span class="sxs-lookup"><span data-stu-id="da993-142">-Version</span></span>
<span data-ttu-id="da993-143">Opublikowana wersja definicji planów.</span><span class="sxs-lookup"><span data-stu-id="da993-143">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="da993-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da993-144">CommonParameters</span></span>
<span data-ttu-id="da993-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da993-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da993-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da993-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da993-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da993-147">INPUTS</span></span>

### <span data-ttu-id="da993-148">System. String</span><span class="sxs-lookup"><span data-stu-id="da993-148">System.String</span></span>

## <span data-ttu-id="da993-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da993-149">OUTPUTS</span></span>

### <span data-ttu-id="da993-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="da993-150">System.Object</span></span>
## <span data-ttu-id="da993-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da993-151">NOTES</span></span>

## <span data-ttu-id="da993-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da993-152">RELATED LINKS</span></span>
