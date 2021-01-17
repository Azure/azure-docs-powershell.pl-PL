---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365869"
---
# <span data-ttu-id="79b03-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="79b03-101">New-AzTag</span></span>

## <span data-ttu-id="79b03-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79b03-102">SYNOPSIS</span></span>
<span data-ttu-id="79b03-103">Tworzy wstępnie zdefiniowany tag Azure lub dodaje wartości do istniejącego tagu | Umożliwia utworzenie lub zaktualizowanie całego zestawu tagów zasobu lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="79b03-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="79b03-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79b03-104">SYNTAX</span></span>

### <span data-ttu-id="79b03-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="79b03-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79b03-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79b03-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="79b03-107">Opis</span><span class="sxs-lookup"><span data-stu-id="79b03-107">DESCRIPTION</span></span>

<span data-ttu-id="79b03-108">**CreatePredefinedTagSet**: polecenie cmdlet **New-AzTag** tworzy wstępnie zdefiniowany tag Azure z opcjonalną wstępnie zdefiniowaną wartością.</span><span class="sxs-lookup"><span data-stu-id="79b03-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="79b03-109">Można go również użyć w celu dodania kolejnych wartości do istniejących wstępnie zdefiniowanych znaczników.</span><span class="sxs-lookup"><span data-stu-id="79b03-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="79b03-110">Aby utworzyć wstępnie zdefiniowany znacznik, wprowadź unikatową nazwę znacznika.</span><span class="sxs-lookup"><span data-stu-id="79b03-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="79b03-111">Aby dodać wartość do istniejącego wstępnie zdefiniowanego znacznika, określ nazwę istniejącego znacznika i nową wartość.</span><span class="sxs-lookup"><span data-stu-id="79b03-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="79b03-112">To polecenie cmdlet zwraca obiekt reprezentujący nowy lub zmodyfikowany znacznik wraz z jego wartościami oraz liczbą zasobów, do których został on zastosowany.</span><span class="sxs-lookup"><span data-stu-id="79b03-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="79b03-113">Moduł Tagi platformy Azure, który jest częścią funkcji **New-AzTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79b03-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="79b03-114">Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="79b03-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="79b03-115">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="79b03-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="79b03-116">Aby zastosować wstępnie zdefiniowany znacznik do zasobu lub grupy zasobów, użyj parametru *tag* polecenia cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="79b03-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="79b03-117">Aby wyszukać grupy zasobów o określonej nazwie lub nazwie lub wartości znacznika, użyj parametru *tag* polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="79b03-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="79b03-118">Każdy znacznik ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="79b03-118">Every tag has a name.</span></span>
<span data-ttu-id="79b03-119">Wartości są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="79b03-119">The values are optional.</span></span>
<span data-ttu-id="79b03-120">Wstępnie zdefiniowany tag platformy Azure może mieć wiele wartości, ale po zastosowaniu znacznika do zasobu lub grupy zasobów należy zastosować nazwę znacznika i tylko jedną z jego wartości.</span><span class="sxs-lookup"><span data-stu-id="79b03-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="79b03-121">Możesz na przykład utworzyć wstępnie zdefiniowany tag dział z wartością dla każdego działu, na przykład finanse, zasoby ludzkie i.</span><span class="sxs-lookup"><span data-stu-id="79b03-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="79b03-122">Po zastosowaniu znacznika dział do zasobu należy zastosować tylko pojedynczą wstępnie zdefiniowaną wartość, na przykład finanse.</span><span class="sxs-lookup"><span data-stu-id="79b03-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="79b03-123">**CreateByResourceIdParameterSet**: polecenie cmdlet **New-AzTag** z identyfikatorem **ResourceID** powoduje utworzenie lub zaktualizowanie całego zestawu tagów w zasobie lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="79b03-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="79b03-124">Ta operacja umożliwia dodawanie lub zamienianie całego zestawu tagów w określonym zasobie lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="79b03-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="79b03-125">Określona encja może zawierać maksymalnie 50 tagów.</span><span class="sxs-lookup"><span data-stu-id="79b03-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="79b03-126">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79b03-126">EXAMPLES</span></span>

### <span data-ttu-id="79b03-127">Przykład 1. Tworzenie wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="79b03-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="79b03-128">To polecenie tworzy wstępnie zdefiniowany znacznik o nazwie FY2015.</span><span class="sxs-lookup"><span data-stu-id="79b03-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="79b03-129">Ten tag nie zawiera wartości.</span><span class="sxs-lookup"><span data-stu-id="79b03-129">This tag has no values.</span></span>
<span data-ttu-id="79b03-130">Aby dodać wartości do znacznika, możesz zastosować tag bez wartości do zasobu lub grupy zasobów albo użyć przycisku **New-AzTag** .</span><span class="sxs-lookup"><span data-stu-id="79b03-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="79b03-131">Wartość można również określić po zastosowaniu znacznika do grupy zasobów lub zasobów.</span><span class="sxs-lookup"><span data-stu-id="79b03-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="79b03-132">Przykład 2: Tworzenie wstępnie zdefiniowanego znacznika z wartością</span><span class="sxs-lookup"><span data-stu-id="79b03-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="79b03-133">To polecenie umożliwia utworzenie wstępnie zdefiniowanego tagu o nazwie dział z wartością finansową.</span><span class="sxs-lookup"><span data-stu-id="79b03-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="79b03-134">Przykład 3: Dodawanie wartości do wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="79b03-134">Example 3: Add a value to a predefined tag</span></span>
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

<span data-ttu-id="79b03-135">Te polecenia tworzą wstępnie zdefiniowany tag o nazwie dział z dwiema wartościami.</span><span class="sxs-lookup"><span data-stu-id="79b03-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="79b03-136">Jeśli nazwa znacznika istnieje, polecenie **New-AzTag** dodaje wartość do istniejącego znacznika zamiast tworzyć nowy.</span><span class="sxs-lookup"><span data-stu-id="79b03-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="79b03-137">Przykład 4: stosowanie wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="79b03-137">Example 4: Use a predefined tag</span></span>
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

<span data-ttu-id="79b03-138">Polecenia w tym przykładzie tworzą i używają wstępnie zdefiniowanego znacznika.</span><span class="sxs-lookup"><span data-stu-id="79b03-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="79b03-139">Przykład 5: Tworzenie lub aktualizowanie całego zestawu tagów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="79b03-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="79b03-140">To polecenie powoduje utworzenie lub zaktualizowanie całego zestawu tagów w subskrypcji przy użyciu programu {subId}.</span><span class="sxs-lookup"><span data-stu-id="79b03-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="79b03-141">Przykład 6: Tworzenie lub aktualizowanie całego zestawu tagów w zasobie</span><span class="sxs-lookup"><span data-stu-id="79b03-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

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

<span data-ttu-id="79b03-142">To polecenie umożliwia utworzenie lub zaktualizowanie całego zestawu tagów w zasobie za pomocą zasobu {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="79b03-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="79b03-143">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79b03-143">PARAMETERS</span></span>

### <span data-ttu-id="79b03-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b03-144">-DefaultProfile</span></span>
<span data-ttu-id="79b03-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79b03-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79b03-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79b03-146">-Name</span></span>
<span data-ttu-id="79b03-147">Określa wstępnie zdefiniowaną nazwę znacznika.</span><span class="sxs-lookup"><span data-stu-id="79b03-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="79b03-148">Aby utworzyć nowy wstępnie zdefiniowany znacznik, wprowadź unikatową nazwę.</span><span class="sxs-lookup"><span data-stu-id="79b03-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="79b03-149">Aby dodać wartość do istniejącego znacznika, wprowadź nazwę istniejącego znacznika.</span><span class="sxs-lookup"><span data-stu-id="79b03-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="79b03-150">Jeśli istniejący wstępnie zdefiniowany znacznik ma określoną nazwę, to polecenie **New-AzTag** dodaje określoną wartość (jeśli istnieje) do znacznika o tej nazwie zamiast tworzyć nowy znacznik.</span><span class="sxs-lookup"><span data-stu-id="79b03-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="79b03-151">-Value</span><span class="sxs-lookup"><span data-stu-id="79b03-151">-Value</span></span>
<span data-ttu-id="79b03-152">Określa wstępnie zdefiniowaną wartość znacznika.</span><span class="sxs-lookup"><span data-stu-id="79b03-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="79b03-153">Wstępnie zdefiniowane Tagi mogą zawierać wiele wartości, ale w każdym poleceniu można wprowadzić tylko jedną wartość.</span><span class="sxs-lookup"><span data-stu-id="79b03-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="79b03-154">Ten parametr jest opcjonalny, ponieważ znaczniki mogą zawierać imiona i nazwiska bez wartości.</span><span class="sxs-lookup"><span data-stu-id="79b03-154">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="79b03-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79b03-155">-ResourceId</span></span>
<span data-ttu-id="79b03-156">Identyfikator zasobu oznakowanej jednostki.</span><span class="sxs-lookup"><span data-stu-id="79b03-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="79b03-157">Zasób, Grupa zasobów lub abonament mogą być oznakowane.</span><span class="sxs-lookup"><span data-stu-id="79b03-157">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="79b03-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="79b03-158">-Tag</span></span>
<span data-ttu-id="79b03-159">Tagi, które mają zostać umieszczone w zasobie.</span><span class="sxs-lookup"><span data-stu-id="79b03-159">The tags to put on the resource.</span></span>

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

### <span data-ttu-id="79b03-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79b03-160">-Confirm</span></span>
<span data-ttu-id="79b03-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b03-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b03-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b03-162">-WhatIf</span></span>
<span data-ttu-id="79b03-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b03-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b03-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79b03-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b03-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b03-165">CommonParameters</span></span>
<span data-ttu-id="79b03-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b03-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b03-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79b03-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b03-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79b03-168">INPUTS</span></span>

### <span data-ttu-id="79b03-169">System. String</span><span class="sxs-lookup"><span data-stu-id="79b03-169">System.String</span></span>

### <span data-ttu-id="79b03-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="79b03-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="79b03-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79b03-171">OUTPUTS</span></span>

### <span data-ttu-id="79b03-172">Microsoft. Azure. Commands. resourceName. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="79b03-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="79b03-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79b03-173">NOTES</span></span>

## <span data-ttu-id="79b03-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79b03-174">RELATED LINKS</span></span>

[<span data-ttu-id="79b03-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="79b03-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="79b03-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="79b03-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="79b03-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="79b03-177">Update-AzTag</span></span>](./Update-AzTag.md)