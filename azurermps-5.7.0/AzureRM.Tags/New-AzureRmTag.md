---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: 77bf93905b0cba4e8f8a23cb9f3cb8945fff74f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550464"
---
# <span data-ttu-id="1e339-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1e339-101">New-AzureRmTag</span></span>

## <span data-ttu-id="1e339-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e339-102">SYNOPSIS</span></span>
<span data-ttu-id="1e339-103">Tworzy wstępnie zdefiniowany tag Azure lub dodaje wartości do istniejącego znacznika.</span><span class="sxs-lookup"><span data-stu-id="1e339-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e339-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e339-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e339-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1e339-105">DESCRIPTION</span></span>
<span data-ttu-id="1e339-106">Polecenie cmdlet **New-AzureRmTag** tworzy wstępnie zdefiniowany tag Azure z opcjonalną wstępnie zdefiniowaną wartością.</span><span class="sxs-lookup"><span data-stu-id="1e339-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="1e339-107">Można go również użyć w celu dodania kolejnych wartości do istniejących wstępnie zdefiniowanych znaczników.</span><span class="sxs-lookup"><span data-stu-id="1e339-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="1e339-108">Aby utworzyć wstępnie zdefiniowany znacznik, wprowadź unikatową nazwę znacznika.</span><span class="sxs-lookup"><span data-stu-id="1e339-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="1e339-109">Aby dodać wartość do istniejącego wstępnie zdefiniowanego znacznika, określ nazwę istniejącego znacznika i nową wartość.</span><span class="sxs-lookup"><span data-stu-id="1e339-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>

<span data-ttu-id="1e339-110">To polecenie cmdlet zwraca obiekt reprezentujący nowy lub zmodyfikowany znacznik wraz z jego wartościami oraz liczbą zasobów, do których został on zastosowany.</span><span class="sxs-lookup"><span data-stu-id="1e339-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>

<span data-ttu-id="1e339-111">Moduł Tagi platformy Azure, który jest częścią funkcji **New-AzureRmTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1e339-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="1e339-112">Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="1e339-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="1e339-113">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1e339-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="1e339-114">Jeśli subskrypcja zawiera wszystkie wstępnie zdefiniowane Tagi, nie można stosować niezdefiniowanych tagów ani wartości do żadnych zasobów lub grup zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1e339-114">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="1e339-115">Aby zastosować wstępnie zdefiniowany znacznik do zasobu lub grupy zasobów, użyj parametru *tag* polecenia cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="1e339-115">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="1e339-116">Aby wyszukać grupy zasobów o określonej nazwie lub nazwie lub wartości znacznika, użyj parametru *tag* polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1e339-116">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

<span data-ttu-id="1e339-117">Każdy znacznik ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="1e339-117">Every tag has a name.</span></span>
<span data-ttu-id="1e339-118">Wartości są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="1e339-118">The values are optional.</span></span>
<span data-ttu-id="1e339-119">Wstępnie zdefiniowany tag platformy Azure może mieć wiele wartości, ale po zastosowaniu znacznika do zasobu lub grupy zasobów należy zastosować nazwę znacznika i tylko jedną z jego wartości.</span><span class="sxs-lookup"><span data-stu-id="1e339-119">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="1e339-120">Możesz na przykład utworzyć wstępnie zdefiniowany tag dział z wartością dla każdego działu, na przykład finanse, zasoby ludzkie i.</span><span class="sxs-lookup"><span data-stu-id="1e339-120">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="1e339-121">Po zastosowaniu znacznika dział do zasobu należy zastosować tylko pojedynczą wstępnie zdefiniowaną wartość, na przykład finanse.</span><span class="sxs-lookup"><span data-stu-id="1e339-121">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="1e339-122">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e339-122">EXAMPLES</span></span>

### <span data-ttu-id="1e339-123">Przykład 1. Tworzenie wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="1e339-123">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="1e339-124">To polecenie tworzy wstępnie zdefiniowany znacznik o nazwie FY2015.</span><span class="sxs-lookup"><span data-stu-id="1e339-124">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="1e339-125">Ten tag nie zawiera wartości.</span><span class="sxs-lookup"><span data-stu-id="1e339-125">This tag has no values.</span></span>
<span data-ttu-id="1e339-126">Aby dodać wartości do znacznika, możesz zastosować tag bez wartości do zasobu lub grupy zasobów albo użyć przycisku **New-AzureRmTag** .</span><span class="sxs-lookup"><span data-stu-id="1e339-126">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="1e339-127">Wartość można również określić po zastosowaniu znacznika do grupy zasobów lub zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e339-127">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="1e339-128">Przykład 2: Tworzenie wstępnie zdefiniowanego znacznika z wartością</span><span class="sxs-lookup"><span data-stu-id="1e339-128">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="1e339-129">To polecenie umożliwia utworzenie wstępnie zdefiniowanego tagu o nazwie dział z wartością finansową.</span><span class="sxs-lookup"><span data-stu-id="1e339-129">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="1e339-130">Przykład 3: Dodawanie wartości do wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="1e339-130">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="1e339-131">Te polecenia tworzą wstępnie zdefiniowany tag o nazwie dział z dwiema wartościami.</span><span class="sxs-lookup"><span data-stu-id="1e339-131">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="1e339-132">Jeśli nazwa znacznika istnieje, polecenie **New-AzureRmTag** dodaje wartość do istniejącego znacznika zamiast tworzyć nowy.</span><span class="sxs-lookup"><span data-stu-id="1e339-132">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="1e339-133">Przykład 4: stosowanie wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="1e339-133">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="1e339-134">Polecenia w tym przykładzie tworzą i używają wstępnie zdefiniowanego znacznika.</span><span class="sxs-lookup"><span data-stu-id="1e339-134">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="1e339-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e339-135">PARAMETERS</span></span>

### <span data-ttu-id="1e339-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e339-136">-DefaultProfile</span></span>
<span data-ttu-id="1e339-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e339-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e339-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e339-138">-Name</span></span>
<span data-ttu-id="1e339-139">Określa nazwę znacznika.</span><span class="sxs-lookup"><span data-stu-id="1e339-139">Specifies the tag name.</span></span>
<span data-ttu-id="1e339-140">Aby utworzyć nowy wstępnie zdefiniowany znacznik, wprowadź unikatową nazwę.</span><span class="sxs-lookup"><span data-stu-id="1e339-140">To create a new predefined tag, enter a unique name.</span></span>

<span data-ttu-id="1e339-141">Aby dodać wartość do istniejącego znacznika, wprowadź nazwę istniejącego znacznika.</span><span class="sxs-lookup"><span data-stu-id="1e339-141">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="1e339-142">Jeśli istniejący wstępnie zdefiniowany znacznik ma określoną nazwę, to polecenie **New-AzureRmTag** dodaje określoną wartość (jeśli istnieje) do znacznika o tej nazwie zamiast tworzyć nowy znacznik.</span><span class="sxs-lookup"><span data-stu-id="1e339-142">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e339-143">-Value</span><span class="sxs-lookup"><span data-stu-id="1e339-143">-Value</span></span>
<span data-ttu-id="1e339-144">Określa wartość znacznika.</span><span class="sxs-lookup"><span data-stu-id="1e339-144">Specifies a tag value.</span></span>
<span data-ttu-id="1e339-145">Wstępnie zdefiniowane Tagi mogą zawierać wiele wartości, ale w każdym poleceniu można wprowadzić tylko jedną wartość.</span><span class="sxs-lookup"><span data-stu-id="1e339-145">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="1e339-146">Ten parametr jest opcjonalny, ponieważ znaczniki mogą zawierać imiona i nazwiska bez wartości.</span><span class="sxs-lookup"><span data-stu-id="1e339-146">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e339-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e339-147">CommonParameters</span></span>
<span data-ttu-id="1e339-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e339-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e339-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e339-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e339-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e339-150">INPUTS</span></span>

### <span data-ttu-id="1e339-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1e339-151">None</span></span>

## <span data-ttu-id="1e339-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e339-152">OUTPUTS</span></span>

### <span data-ttu-id="1e339-153">Microsoft. Azure. Commands. Tags. model. PSTag</span><span class="sxs-lookup"><span data-stu-id="1e339-153">Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="1e339-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e339-154">NOTES</span></span>

## <span data-ttu-id="1e339-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e339-155">RELATED LINKS</span></span>

[<span data-ttu-id="1e339-156">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1e339-156">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="1e339-157">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1e339-157">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


