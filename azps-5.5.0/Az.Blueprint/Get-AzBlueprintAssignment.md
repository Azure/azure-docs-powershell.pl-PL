---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239159"
---
# <span data-ttu-id="b0aca-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="b0aca-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="b0aca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0aca-102">SYNOPSIS</span></span>
<span data-ttu-id="b0aca-103">Pobierz co najmniej jedno zadanie planu.</span><span class="sxs-lookup"><span data-stu-id="b0aca-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="b0aca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0aca-104">SYNTAX</span></span>

### <span data-ttu-id="b0aca-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b0aca-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0aca-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="b0aca-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0aca-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="b0aca-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0aca-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="b0aca-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0aca-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0aca-109">DESCRIPTION</span></span>
<span data-ttu-id="b0aca-110">Pobierz co najmniej jedno zadanie planu.</span><span class="sxs-lookup"><span data-stu-id="b0aca-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="b0aca-111">Przydziały planu znajdują się w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b0aca-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="b0aca-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0aca-112">EXAMPLES</span></span>

### <span data-ttu-id="b0aca-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0aca-113">Example 1</span></span>
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

<span data-ttu-id="b0aca-114">Pobierz zadania planu w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b0aca-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="b0aca-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b0aca-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="b0aca-116">Pobierz przypisanie planu z podaną nazwą w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b0aca-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="b0aca-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b0aca-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="b0aca-118">Pobierz przydziały planu w obrębie określonej grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="b0aca-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="b0aca-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b0aca-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="b0aca-120">Pobierz przypisanie planu z podaną nazwą w obrębie określonej grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="b0aca-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="b0aca-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0aca-121">PARAMETERS</span></span>

### <span data-ttu-id="b0aca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0aca-122">-DefaultProfile</span></span>
<span data-ttu-id="b0aca-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0aca-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0aca-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b0aca-124">-ManagementGroupId</span></span>
<span data-ttu-id="b0aca-125">Identyfikator grupy zarządzania, w której zapisano przydział Plan.</span><span class="sxs-lookup"><span data-stu-id="b0aca-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="b0aca-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b0aca-126">-Name</span></span>
<span data-ttu-id="b0aca-127">Nazwa zadania planu.</span><span class="sxs-lookup"><span data-stu-id="b0aca-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="b0aca-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0aca-128">-SubscriptionId</span></span>
<span data-ttu-id="b0aca-129">Identyfikator subskrypcji, w przypadku których wdrożono przypisanie planu.</span><span class="sxs-lookup"><span data-stu-id="b0aca-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="b0aca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0aca-130">CommonParameters</span></span>
<span data-ttu-id="b0aca-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0aca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0aca-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0aca-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0aca-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0aca-133">INPUTS</span></span>

### <span data-ttu-id="b0aca-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b0aca-134">System.String</span></span>

## <span data-ttu-id="b0aca-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0aca-135">OUTPUTS</span></span>

### <span data-ttu-id="b0aca-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="b0aca-136">System.Object</span></span>
## <span data-ttu-id="b0aca-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0aca-137">NOTES</span></span>

## <span data-ttu-id="b0aca-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0aca-138">RELATED LINKS</span></span>
