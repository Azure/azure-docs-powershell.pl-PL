---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 375eca319a1db467e97addac50faa3f91fe0ecc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954865"
---
# <span data-ttu-id="909a1-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="909a1-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="909a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="909a1-102">SYNOPSIS</span></span>
<span data-ttu-id="909a1-103">Pobierz co najmniej jedno zadanie planu.</span><span class="sxs-lookup"><span data-stu-id="909a1-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="909a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="909a1-104">SYNTAX</span></span>

### <span data-ttu-id="909a1-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="909a1-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="909a1-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="909a1-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="909a1-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="909a1-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="909a1-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="909a1-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="909a1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="909a1-109">DESCRIPTION</span></span>
<span data-ttu-id="909a1-110">Pobierz co najmniej jedno zadanie planu.</span><span class="sxs-lookup"><span data-stu-id="909a1-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="909a1-111">Przydziały planu znajdują się w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="909a1-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="909a1-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="909a1-112">EXAMPLES</span></span>

### <span data-ttu-id="909a1-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="909a1-113">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="909a1-114">Pobierz zadania planu w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="909a1-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="909a1-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="909a1-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="909a1-116">Uzyskaj przypisanie planu z podaną nazwą w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="909a1-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="909a1-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="909a1-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="909a1-118">Pobierz przydziały planu w obrębie określonej grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="909a1-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="909a1-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="909a1-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="909a1-120">Pobierz przypisanie planu z podaną nazwą w obrębie określonej grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="909a1-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="909a1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="909a1-121">PARAMETERS</span></span>

### <span data-ttu-id="909a1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="909a1-122">-DefaultProfile</span></span>
<span data-ttu-id="909a1-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="909a1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="909a1-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="909a1-124">-ManagementGroupId</span></span>
<span data-ttu-id="909a1-125">Identyfikator grupy zarządzania, w której jest zapisywany przydział Plan.</span><span class="sxs-lookup"><span data-stu-id="909a1-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909a1-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="909a1-126">-Name</span></span>
<span data-ttu-id="909a1-127">Nazwa zadania planu.</span><span class="sxs-lookup"><span data-stu-id="909a1-127">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909a1-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="909a1-128">-SubscriptionId</span></span>
<span data-ttu-id="909a1-129">Identyfikator subskrypcji, w ramach których wdrożono przypisanie planu.</span><span class="sxs-lookup"><span data-stu-id="909a1-129">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="909a1-130">CommonParameters</span></span>
<span data-ttu-id="909a1-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="909a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="909a1-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="909a1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="909a1-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="909a1-133">INPUTS</span></span>

### <span data-ttu-id="909a1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="909a1-134">System.String</span></span>

## <span data-ttu-id="909a1-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="909a1-135">OUTPUTS</span></span>

### <span data-ttu-id="909a1-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="909a1-136">System.Object</span></span>
## <span data-ttu-id="909a1-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="909a1-137">NOTES</span></span>

## <span data-ttu-id="909a1-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="909a1-138">RELATED LINKS</span></span>
