---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327782"
---
# <span data-ttu-id="9ad92-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="9ad92-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="9ad92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ad92-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad92-103">Uzyskaj jeden lub więcej zadań dotyczących projektów.</span><span class="sxs-lookup"><span data-stu-id="9ad92-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="9ad92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ad92-104">SYNTAX</span></span>

### <span data-ttu-id="9ad92-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ad92-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad92-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="9ad92-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad92-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="9ad92-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad92-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="9ad92-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ad92-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9ad92-109">DESCRIPTION</span></span>
<span data-ttu-id="9ad92-110">Uzyskaj jeden lub więcej zadań dotyczących projektów.</span><span class="sxs-lookup"><span data-stu-id="9ad92-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="9ad92-111">W zakresie subskrypcji istnieją zadania dotyczące planów.</span><span class="sxs-lookup"><span data-stu-id="9ad92-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="9ad92-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ad92-112">EXAMPLES</span></span>

### <span data-ttu-id="9ad92-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ad92-113">Example 1</span></span>
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

<span data-ttu-id="9ad92-114">Uzyskaj zadania tworzenia planów w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9ad92-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="9ad92-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9ad92-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="9ad92-116">Uzyskaj zadanie Kup na podstawie podanej nazwy w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9ad92-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="9ad92-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9ad92-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="9ad92-118">Uzyskaj zadania tworzenia planów w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="9ad92-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="9ad92-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="9ad92-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="9ad92-120">Uzyskaj zadanie Kup na podstawie podanej nazwy w określonej grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="9ad92-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="9ad92-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ad92-121">PARAMETERS</span></span>

### <span data-ttu-id="9ad92-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad92-122">-DefaultProfile</span></span>
<span data-ttu-id="9ad92-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ad92-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ad92-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="9ad92-124">-ManagementGroupId</span></span>
<span data-ttu-id="9ad92-125">Identyfikator grupy zarządzania, w której jest zapisywane zadanie tworzenia pozycji plan.</span><span class="sxs-lookup"><span data-stu-id="9ad92-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="9ad92-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ad92-126">-Name</span></span>
<span data-ttu-id="9ad92-127">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="9ad92-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="9ad92-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9ad92-128">-SubscriptionId</span></span>
<span data-ttu-id="9ad92-129">Identyfikator subskrypcji, do której jest wdrażane zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="9ad92-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="9ad92-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad92-130">CommonParameters</span></span>
<span data-ttu-id="9ad92-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad92-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad92-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ad92-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad92-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ad92-133">INPUTS</span></span>

### <span data-ttu-id="9ad92-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad92-134">System.String</span></span>

## <span data-ttu-id="9ad92-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ad92-135">OUTPUTS</span></span>

### <span data-ttu-id="9ad92-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="9ad92-136">System.Object</span></span>
## <span data-ttu-id="9ad92-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ad92-137">NOTES</span></span>

## <span data-ttu-id="9ad92-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ad92-138">RELATED LINKS</span></span>
