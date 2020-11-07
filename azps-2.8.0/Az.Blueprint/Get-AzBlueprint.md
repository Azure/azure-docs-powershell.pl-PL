---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: cd4cb9f7137d0e6cdd91222c278b6e59c04d7e3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706615"
---
# <span data-ttu-id="d0efa-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="d0efa-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="d0efa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0efa-102">SYNOPSIS</span></span>
<span data-ttu-id="d0efa-103">Pobierz co najmniej jeden z definicji planów.</span><span class="sxs-lookup"><span data-stu-id="d0efa-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="d0efa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0efa-104">SYNTAX</span></span>

### <span data-ttu-id="d0efa-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0efa-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0efa-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="d0efa-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0efa-107">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="d0efa-107">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0efa-108">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="d0efa-108">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0efa-109">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="d0efa-109">ManagementGroupScope</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0efa-110">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="d0efa-110">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0efa-111">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="d0efa-111">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0efa-112">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="d0efa-112">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0efa-113">Opis</span><span class="sxs-lookup"><span data-stu-id="d0efa-113">DESCRIPTION</span></span>
<span data-ttu-id="d0efa-114">Pobierz co najmniej jeden z definicji planów.</span><span class="sxs-lookup"><span data-stu-id="d0efa-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="d0efa-115">Definicje planów istnieją w grupie zarządzania lub w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d0efa-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="d0efa-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0efa-116">EXAMPLES</span></span>

### <span data-ttu-id="d0efa-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0efa-117">Example 1</span></span>
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

<span data-ttu-id="d0efa-118">Pobierz definicje planów w ramach bieżącego abonamentu i hierarchii grupy zarządzania subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d0efa-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="d0efa-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d0efa-119">Example 2</span></span>
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

<span data-ttu-id="d0efa-120">Pobierz definicje planów w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d0efa-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="d0efa-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d0efa-121">Example 3</span></span>
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

<span data-ttu-id="d0efa-122">Pobieranie definicji planów w ramach określonego abonamentu i hierarchii grupy zarządzania subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d0efa-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="d0efa-123">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="d0efa-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="d0efa-124">Zapoznaj się z definicją plany o podanej nazwie w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d0efa-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="d0efa-125">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="d0efa-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="d0efa-126">Pobierz definicję plany o podaną nazwę i wersję w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d0efa-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="d0efa-127">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="d0efa-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="d0efa-128">Uzyskaj najnowszą opublikowaną definicję usługi o podanej nazwie w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d0efa-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="d0efa-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0efa-129">PARAMETERS</span></span>

### <span data-ttu-id="d0efa-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0efa-130">-DefaultProfile</span></span>
<span data-ttu-id="d0efa-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0efa-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0efa-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="d0efa-132">-LatestPublished</span></span>
<span data-ttu-id="d0efa-133">Najnowsza opublikowana flaga definicji planów.</span><span class="sxs-lookup"><span data-stu-id="d0efa-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="d0efa-134">Po ustawieniu funkcja wykonywanie zwraca najnowszą opublikowaną wersję definicji.</span><span class="sxs-lookup"><span data-stu-id="d0efa-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="d0efa-135">Wartość domyślna to FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="d0efa-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySubscriptionNameAndLatestPublished, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0efa-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d0efa-136">-ManagementGroupId</span></span>
<span data-ttu-id="d0efa-137">Identyfikator grupy zarządzania, gdzie jest zapisywana definicja programu.</span><span class="sxs-lookup"><span data-stu-id="d0efa-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0efa-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0efa-138">-Name</span></span>
<span data-ttu-id="d0efa-139">Nazwa definicji plany.</span><span class="sxs-lookup"><span data-stu-id="d0efa-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0efa-140">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d0efa-140">-SubscriptionId</span></span>
<span data-ttu-id="d0efa-141">Identyfikator abonamentu, w którym jest zapisywana definicja programu.</span><span class="sxs-lookup"><span data-stu-id="d0efa-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0efa-142">-Version</span><span class="sxs-lookup"><span data-stu-id="d0efa-142">-Version</span></span>
<span data-ttu-id="d0efa-143">Opublikowana wersja definicji planów.</span><span class="sxs-lookup"><span data-stu-id="d0efa-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionNameAndVersion, ByManagementGroupNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0efa-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0efa-144">CommonParameters</span></span>
<span data-ttu-id="d0efa-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0efa-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0efa-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0efa-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0efa-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0efa-147">INPUTS</span></span>

### <span data-ttu-id="d0efa-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d0efa-148">System.String</span></span>

## <span data-ttu-id="d0efa-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0efa-149">OUTPUTS</span></span>

### <span data-ttu-id="d0efa-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="d0efa-150">System.Object</span></span>
## <span data-ttu-id="d0efa-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0efa-151">NOTES</span></span>

## <span data-ttu-id="d0efa-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0efa-152">RELATED LINKS</span></span>
