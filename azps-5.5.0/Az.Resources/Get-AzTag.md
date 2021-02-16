---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240075"
---
# <span data-ttu-id="6dce3-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="6dce3-101">Get-AzTag</span></span>

## <span data-ttu-id="6dce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dce3-102">SYNOPSIS</span></span>
<span data-ttu-id="6dce3-103">Pobiera wstępnie zdefiniowane tagi platformy Azure | Pobiera cały zestaw tagów do zasobu lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6dce3-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="6dce3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6dce3-104">SYNTAX</span></span>

### <span data-ttu-id="6dce3-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dce3-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dce3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dce3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dce3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6dce3-107">DESCRIPTION</span></span>

<span data-ttu-id="6dce3-108">**GetPredefinedTagSet:** Polecenie cmdlet **Get-AzTag** pobiera wstępnie zdefiniowane tagi platformy Azure w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6dce3-108">**GetPredefinedTagSet**: The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="6dce3-109">To polecenie cmdlet zwraca podstawowe informacje o tagach lub szczegółowe informacje o tagach i ich wartościach.</span><span class="sxs-lookup"><span data-stu-id="6dce3-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="6dce3-110">Wszystkie obiekty wyjściowe zawierają właściwość Count reprezentującą liczbę zasobów i grup zasobów, do których zastosowano tagi i wartości.</span><span class="sxs-lookup"><span data-stu-id="6dce3-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="6dce3-111">Moduł Azure Tags, do których należy **Get-AzTag,** może ułatwić zarządzanie wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6dce3-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="6dce3-112">Tag Azure to para wartości nazw, za pomocą których można kategoryzować zasoby platformy Azure i grupy zasobów, na przykład według działów lub centrum kosztów, a także śledzić notatki i komentarze dotyczące zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="6dce3-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="6dce3-113">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane tagi pozwalają ustalić standardowe, spójne i przewidywalne nazwy oraz wartości tagów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6dce3-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="6dce3-114">Aby utworzyć wstępnie zdefiniowany tag, użyj New-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dce3-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="6dce3-115">Aby zastosować wstępnie zdefiniowany tag do grupy zasobów, użyj parametru *Tag* New-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dce3-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="6dce3-116">Aby wyszukać określoną nazwę tagu lub nazwę i wartość w grupach zasobów, użyj parametru *Tag* Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dce3-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="6dce3-117">**GetByResourceIdParameterSet:** Polecenie cmdlet **Get-AzTag** z tagiem **ResourceId** pobiera cały zestaw tagów dla zasobu lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6dce3-117">**GetByResourceIdParameterSet**: The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="6dce3-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6dce3-118">EXAMPLES</span></span>

### <span data-ttu-id="6dce3-119">Przykład 1. Pobierz wszystkie wstępnie zdefiniowane tagi</span><span class="sxs-lookup"><span data-stu-id="6dce3-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="6dce3-120">To polecenie pobiera wszystkie wstępnie zdefiniowane tagi w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6dce3-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="6dce3-121">Właściwość Count pokazuje, ile razy tag został zastosowany do zasobów i grup zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6dce3-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="6dce3-122">Przykład 2. Uzyskiwanie tagu według nazwy</span><span class="sxs-lookup"><span data-stu-id="6dce3-122">Example 2: Get a tag by name</span></span>
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="6dce3-123">To polecenie pobiera szczegółowe informacje o tagu Dział i jego wartościach.</span><span class="sxs-lookup"><span data-stu-id="6dce3-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="6dce3-124">Właściwość Count pokazuje, ile razy tag i każda z jego wartości zostały zastosowane do zasobów i grup zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6dce3-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="6dce3-125">Przykład 3. Uzyskiwanie wartości wszystkich tagów</span><span class="sxs-lookup"><span data-stu-id="6dce3-125">Example 3: Get values of all tags</span></span>
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="6dce3-126">To polecenie używa *parametru Szczegółowe* w celu uzyskania szczegółowych informacji o wszystkich wstępnie zdefiniowanych tagach w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6dce3-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="6dce3-127">Użycie *parametru Szczegóły* jest równoważne użyciu *parametru Name* dla każdego tagu.</span><span class="sxs-lookup"><span data-stu-id="6dce3-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="6dce3-128">Przykład 4. Pobierz cały zestaw tagów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6dce3-128">Example 4: Get the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="6dce3-129">To polecenie pobiera cały zestaw tagów subskrypcji za pomocą {subId}.</span><span class="sxs-lookup"><span data-stu-id="6dce3-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="6dce3-130">Przykład 5. Uzyskiwanie całego zestawu tagów dla zasobu</span><span class="sxs-lookup"><span data-stu-id="6dce3-130">Example 5: Get the entire set of tags on a resource</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="6dce3-131">To polecenie pobiera cały zestaw tagów zasobu za pomocą {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="6dce3-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="6dce3-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dce3-132">PARAMETERS</span></span>

### <span data-ttu-id="6dce3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dce3-133">-DefaultProfile</span></span>
<span data-ttu-id="6dce3-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6dce3-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dce3-135">— Szczegóły</span><span class="sxs-lookup"><span data-stu-id="6dce3-135">-Detailed</span></span>
<span data-ttu-id="6dce3-136">Wskazuje, że ta operacja powoduje dodanie do danych wyjściowych informacji o wartościach tagów.</span><span class="sxs-lookup"><span data-stu-id="6dce3-136">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dce3-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6dce3-137">-Name</span></span>
<span data-ttu-id="6dce3-138">Nazwa wstępnie zdefiniowanego tagu.</span><span class="sxs-lookup"><span data-stu-id="6dce3-138">Name of the predefined tag.</span></span>
<span data-ttu-id="6dce3-139">Domyślnie **get-aztag otrzymuje** podstawowe informacje o wszystkich wstępnie zdefiniowanych tagach w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6dce3-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="6dce3-140">Określenie parametru *Name (Nazwa)* nie *ma* wpływu na parametr Szczegóły.</span><span class="sxs-lookup"><span data-stu-id="6dce3-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dce3-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dce3-141">-ResourceId</span></span>
<span data-ttu-id="6dce3-142">Identyfikator zasobu dla otagowanego elementu.</span><span class="sxs-lookup"><span data-stu-id="6dce3-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="6dce3-143">Może zostać otagowany zasób, grupa zasobów lub subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="6dce3-143">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dce3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dce3-144">CommonParameters</span></span>
<span data-ttu-id="6dce3-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dce3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dce3-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dce3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dce3-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dce3-147">INPUTS</span></span>

### <span data-ttu-id="6dce3-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6dce3-148">System.String</span></span>

### <span data-ttu-id="6dce3-149">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="6dce3-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6dce3-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dce3-150">OUTPUTS</span></span>

### <span data-ttu-id="6dce3-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="6dce3-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="6dce3-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6dce3-152">NOTES</span></span>

## <span data-ttu-id="6dce3-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6dce3-153">RELATED LINKS</span></span>

[<span data-ttu-id="6dce3-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="6dce3-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="6dce3-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="6dce3-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="6dce3-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="6dce3-156">Update-AzTag</span></span>](./Update-AzTag.md)
