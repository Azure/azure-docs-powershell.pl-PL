---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: b5f80abac4c114ab60dcb130f229265c4aafd78f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971786"
---
# <span data-ttu-id="a92e8-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="a92e8-101">New-AzTag</span></span>

## <span data-ttu-id="a92e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a92e8-102">SYNOPSIS</span></span>
<span data-ttu-id="a92e8-103">Tworzy wstępnie zdefiniowany tag platformy Azure lub dodaje wartości do istniejącego tagu | Tworzy lub aktualizuje cały zestaw tagów dla zasobu lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a92e8-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="a92e8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a92e8-104">SYNTAX</span></span>

### <span data-ttu-id="a92e8-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="a92e8-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a92e8-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a92e8-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="a92e8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a92e8-107">DESCRIPTION</span></span>

<span data-ttu-id="a92e8-108">**CreatePredefinedTagSet:** polecenie cmdlet **New-AzTag** tworzy wstępnie zdefiniowany tag platformy Azure z opcjonalną wstępnie zdefiniowaną wartością.</span><span class="sxs-lookup"><span data-stu-id="a92e8-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="a92e8-109">Za jego pomocą można również dodawać dodatkowe wartości do istniejących wstępnie zdefiniowanych tagów.</span><span class="sxs-lookup"><span data-stu-id="a92e8-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="a92e8-110">Aby utworzyć wstępnie zdefiniowany tag, wprowadź unikatową nazwę tagu.</span><span class="sxs-lookup"><span data-stu-id="a92e8-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="a92e8-111">Aby dodać wartość do istniejącego wstępnie zdefiniowanego tagu, określ nazwę istniejącego tagu i nową wartość.</span><span class="sxs-lookup"><span data-stu-id="a92e8-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="a92e8-112">To polecenie cmdlet zwraca obiekt reprezentujący nowy lub zmodyfikowany tag wraz z jego wartościami i liczbą zasobów, do których został zastosowany.</span><span class="sxs-lookup"><span data-stu-id="a92e8-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="a92e8-113">Moduł Tagi platformy Azure, do których należy program **New-AzTag,** może ułatwić zarządzanie wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a92e8-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="a92e8-114">Tag Azure to para wartości nazw, za pomocą których można kategoryzować zasoby platformy Azure i grupy zasobów, na przykład według działów lub centrum kosztów, lub do śledzenia notatek lub komentarzy dotyczących zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="a92e8-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="a92e8-115">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane tagi pozwalają ustalić standardowe, spójne i przewidywalne nazwy oraz wartości tagów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a92e8-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="a92e8-116">Aby zastosować wstępnie zdefiniowany tag do zasobu lub grupy zasobów, użyj parametru *Tag* New-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a92e8-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="a92e8-117">Aby wyszukać grupy zasobów z określoną nazwą tagu lub nazwą i wartością, użyj parametru *Tag* Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a92e8-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a92e8-118">Każdy tag ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="a92e8-118">Every tag has a name.</span></span>
<span data-ttu-id="a92e8-119">Wartości są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="a92e8-119">The values are optional.</span></span>
<span data-ttu-id="a92e8-120">Wstępnie zdefiniowany tag platformy Azure może mieć wiele wartości, ale po zastosowaniu tagu do zasobu lub grupy zasobów należy zastosować nazwę tagu i tylko jedną z jej wartości.</span><span class="sxs-lookup"><span data-stu-id="a92e8-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="a92e8-121">Można na przykład utworzyć wstępnie zdefiniowany tag Dział z wartością dla każdego działu, takiego jak Finanse, Kadry i DZIAŁ IT.</span><span class="sxs-lookup"><span data-stu-id="a92e8-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="a92e8-122">Po zastosowaniu tagu Dział do zasobu stosuje się tylko jedną wstępnie zdefiniowaną wartość, na przykład Finanse.</span><span class="sxs-lookup"><span data-stu-id="a92e8-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="a92e8-123">**CreateByResourceIdParameterSet:** Polecenie cmdlet **New-AzTag** z tagiem **ResourceId** tworzy lub aktualizuje cały zestaw tagów dla zasobu lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a92e8-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="a92e8-124">Ta operacja umożliwia dodanie lub zastąpienie całego zestawu tagów dla określonego zasobu lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a92e8-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="a92e8-125">Określona jednostka może mieć maksymalnie 50 tagów.</span><span class="sxs-lookup"><span data-stu-id="a92e8-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="a92e8-126">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a92e8-126">EXAMPLES</span></span>

### <span data-ttu-id="a92e8-127">Przykład 1. Tworzenie wstępnie zdefiniowanego tagu</span><span class="sxs-lookup"><span data-stu-id="a92e8-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="a92e8-128">To polecenie tworzy wstępnie zdefiniowany tag o nazwie ROK2015.</span><span class="sxs-lookup"><span data-stu-id="a92e8-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="a92e8-129">Ten tag nie ma wartości.</span><span class="sxs-lookup"><span data-stu-id="a92e8-129">This tag has no values.</span></span>
<span data-ttu-id="a92e8-130">Do zasobu lub grupy zasobów można zastosować tag bez wartości albo dodać wartości do tagu za pomocą tagu **Nowy-AzTag.**</span><span class="sxs-lookup"><span data-stu-id="a92e8-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="a92e8-131">Wartość można także określić podczas stosowania tagu do zasobu lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a92e8-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="a92e8-132">Przykład 2. Tworzenie wstępnie zdefiniowanego tagu z wartością</span><span class="sxs-lookup"><span data-stu-id="a92e8-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="a92e8-133">To polecenie tworzy wstępnie zdefiniowany tag o nazwie Dział o wartości Finanse.</span><span class="sxs-lookup"><span data-stu-id="a92e8-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="a92e8-134">Przykład 3. Dodawanie wartości do wstępnie zdefiniowanego tagu</span><span class="sxs-lookup"><span data-stu-id="a92e8-134">Example 3: Add a value to a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="a92e8-135">Te polecenia tworzą wstępnie zdefiniowany tag o nazwie Dział z dwiema wartościami.</span><span class="sxs-lookup"><span data-stu-id="a92e8-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="a92e8-136">Jeśli nazwa tagu istnieje, **nowy-aztag** dodaje wartość do istniejącego tagu, zamiast tworzyć nowy.</span><span class="sxs-lookup"><span data-stu-id="a92e8-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="a92e8-137">Przykład 4. Używanie wstępnie zdefiniowanego tagu</span><span class="sxs-lookup"><span data-stu-id="a92e8-137">Example 4: Use a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="a92e8-138">Polecenia w tym przykładzie tworzą i używają wstępnie zdefiniowanego tagu.</span><span class="sxs-lookup"><span data-stu-id="a92e8-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="a92e8-139">Przykład 5. Tworzenie lub aktualizacja całego zestawu tagów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a92e8-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="a92e8-140">To polecenie tworzy lub aktualizuje cały zestaw tagów subskrypcji za pomocą {subId}.</span><span class="sxs-lookup"><span data-stu-id="a92e8-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="a92e8-141">Przykład 6. Tworzenie lub aktualizacja całego zestawu tagów dla zasobu</span><span class="sxs-lookup"><span data-stu-id="a92e8-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="a92e8-142">To polecenie tworzy lub aktualizuje cały zestaw tagów zasobu za pomocą {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="a92e8-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="a92e8-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a92e8-143">PARAMETERS</span></span>

### <span data-ttu-id="a92e8-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92e8-144">-DefaultProfile</span></span>
<span data-ttu-id="a92e8-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a92e8-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a92e8-146">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a92e8-146">-Name</span></span>
<span data-ttu-id="a92e8-147">Określa wstępnie zdefiniowaną nazwę tagu.</span><span class="sxs-lookup"><span data-stu-id="a92e8-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="a92e8-148">Aby utworzyć nowy wstępnie zdefiniowany tag, wprowadź unikatową nazwę.</span><span class="sxs-lookup"><span data-stu-id="a92e8-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="a92e8-149">Aby dodać wartość do istniejącego tagu, wprowadź nazwę istniejącego tagu.</span><span class="sxs-lookup"><span data-stu-id="a92e8-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="a92e8-150">Jeśli istniejący wstępnie zdefiniowany tag ma określoną nazwę, element **New-AzTag** doda określoną wartość (o ile taki tag się znajduje) do tagu o tej nazwie, zamiast tworzyć nowy tag.</span><span class="sxs-lookup"><span data-stu-id="a92e8-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92e8-151">— Wartość</span><span class="sxs-lookup"><span data-stu-id="a92e8-151">-Value</span></span>
<span data-ttu-id="a92e8-152">Określa wstępnie zdefiniowaną wartość tagu.</span><span class="sxs-lookup"><span data-stu-id="a92e8-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="a92e8-153">Wstępnie zdefiniowane tagi mogą mieć wiele wartości, ale w każdym z poleceń można wprowadzić tylko jedną wartość.</span><span class="sxs-lookup"><span data-stu-id="a92e8-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="a92e8-154">Ten parametr jest opcjonalny, ponieważ tagi mogą mieć nazwy bez wartości.</span><span class="sxs-lookup"><span data-stu-id="a92e8-154">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92e8-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a92e8-155">-ResourceId</span></span>
<span data-ttu-id="a92e8-156">Identyfikator zasobu dla otagowanego podmiotu.</span><span class="sxs-lookup"><span data-stu-id="a92e8-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="a92e8-157">Może zostać otagowany zasób, grupa zasobów lub subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="a92e8-157">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92e8-158">— Tag</span><span class="sxs-lookup"><span data-stu-id="a92e8-158">-Tag</span></span>
<span data-ttu-id="a92e8-159">Tagi, które mają być umieszczane dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="a92e8-159">The tags to put on the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92e8-160">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a92e8-160">-Confirm</span></span>
<span data-ttu-id="a92e8-161">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a92e8-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92e8-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a92e8-162">-WhatIf</span></span>
<span data-ttu-id="a92e8-163">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a92e8-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a92e8-164">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a92e8-164">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92e8-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92e8-165">CommonParameters</span></span>
<span data-ttu-id="a92e8-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92e8-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92e8-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a92e8-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92e8-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a92e8-168">INPUTS</span></span>

### <span data-ttu-id="a92e8-169">System.String</span><span class="sxs-lookup"><span data-stu-id="a92e8-169">System.String</span></span>

### <span data-ttu-id="a92e8-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a92e8-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a92e8-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a92e8-171">OUTPUTS</span></span>

### <span data-ttu-id="a92e8-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="a92e8-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="a92e8-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a92e8-173">NOTES</span></span>

## <span data-ttu-id="a92e8-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a92e8-174">RELATED LINKS</span></span>

[<span data-ttu-id="a92e8-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="a92e8-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="a92e8-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="a92e8-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="a92e8-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="a92e8-177">Update-AzTag</span></span>](./Update-AzTag.md)