---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: cd9700a633f1a9c09c5fafd060d318b35eaeaabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553399"
---
# <span data-ttu-id="af2a5-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="af2a5-101">New-AzureRmTag</span></span>

## <span data-ttu-id="af2a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="af2a5-103">Tworzy wstępnie zdefiniowany tag Azure lub dodaje wartości do istniejącego znacznika.</span><span class="sxs-lookup"><span data-stu-id="af2a5-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af2a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af2a5-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af2a5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af2a5-105">DESCRIPTION</span></span>
<span data-ttu-id="af2a5-106">Polecenie cmdlet **New-AzureRmTag** tworzy wstępnie zdefiniowany tag Azure z opcjonalną wstępnie zdefiniowaną wartością.</span><span class="sxs-lookup"><span data-stu-id="af2a5-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="af2a5-107">Można go również użyć w celu dodania kolejnych wartości do istniejących wstępnie zdefiniowanych znaczników.</span><span class="sxs-lookup"><span data-stu-id="af2a5-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="af2a5-108">Aby utworzyć wstępnie zdefiniowany znacznik, wprowadź unikatową nazwę znacznika.</span><span class="sxs-lookup"><span data-stu-id="af2a5-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="af2a5-109">Aby dodać wartość do istniejącego wstępnie zdefiniowanego znacznika, określ nazwę istniejącego znacznika i nową wartość.</span><span class="sxs-lookup"><span data-stu-id="af2a5-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="af2a5-110">To polecenie cmdlet zwraca obiekt reprezentujący nowy lub zmodyfikowany znacznik wraz z jego wartościami oraz liczbą zasobów, do których został on zastosowany.</span><span class="sxs-lookup"><span data-stu-id="af2a5-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="af2a5-111">Moduł Tagi platformy Azure, który jest częścią funkcji **New-AzureRmTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="af2a5-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="af2a5-112">Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="af2a5-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="af2a5-113">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="af2a5-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="af2a5-114">Aby zastosować wstępnie zdefiniowany znacznik do zasobu lub grupy zasobów, użyj parametru *tag* polecenia cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="af2a5-114">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="af2a5-115">Aby wyszukać grupy zasobów o określonej nazwie lub nazwie lub wartości znacznika, użyj parametru *tag* polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="af2a5-115">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="af2a5-116">Każdy znacznik ma nazwę.</span><span class="sxs-lookup"><span data-stu-id="af2a5-116">Every tag has a name.</span></span>
<span data-ttu-id="af2a5-117">Wartości są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="af2a5-117">The values are optional.</span></span>
<span data-ttu-id="af2a5-118">Wstępnie zdefiniowany tag platformy Azure może mieć wiele wartości, ale po zastosowaniu znacznika do zasobu lub grupy zasobów należy zastosować nazwę znacznika i tylko jedną z jego wartości.</span><span class="sxs-lookup"><span data-stu-id="af2a5-118">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="af2a5-119">Możesz na przykład utworzyć wstępnie zdefiniowany tag dział z wartością dla każdego działu, na przykład finanse, zasoby ludzkie i.</span><span class="sxs-lookup"><span data-stu-id="af2a5-119">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="af2a5-120">Po zastosowaniu znacznika dział do zasobu należy zastosować tylko pojedynczą wstępnie zdefiniowaną wartość, na przykład finanse.</span><span class="sxs-lookup"><span data-stu-id="af2a5-120">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="af2a5-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af2a5-121">EXAMPLES</span></span>

### <span data-ttu-id="af2a5-122">Przykład 1. Tworzenie wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="af2a5-122">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   FY2015
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="af2a5-123">To polecenie tworzy wstępnie zdefiniowany znacznik o nazwie FY2015.</span><span class="sxs-lookup"><span data-stu-id="af2a5-123">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="af2a5-124">Ten tag nie zawiera wartości.</span><span class="sxs-lookup"><span data-stu-id="af2a5-124">This tag has no values.</span></span>
<span data-ttu-id="af2a5-125">Aby dodać wartości do znacznika, możesz zastosować tag bez wartości do zasobu lub grupy zasobów albo użyć przycisku **New-AzureRmTag** .</span><span class="sxs-lookup"><span data-stu-id="af2a5-125">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="af2a5-126">Wartość można również określić po zastosowaniu znacznika do grupy zasobów lub zasobów.</span><span class="sxs-lookup"><span data-stu-id="af2a5-126">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="af2a5-127">Przykład 2: Tworzenie wstępnie zdefiniowanego znacznika z wartością</span><span class="sxs-lookup"><span data-stu-id="af2a5-127">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="af2a5-128">To polecenie umożliwia utworzenie wstępnie zdefiniowanego tagu o nazwie dział z wartością finansową.</span><span class="sxs-lookup"><span data-stu-id="af2a5-128">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="af2a5-129">Przykład 3: Dodawanie wartości do wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="af2a5-129">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="af2a5-130">Te polecenia tworzą wstępnie zdefiniowany tag o nazwie dział z dwiema wartościami.</span><span class="sxs-lookup"><span data-stu-id="af2a5-130">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="af2a5-131">Jeśli nazwa znacznika istnieje, polecenie **New-AzureRmTag** dodaje wartość do istniejącego znacznika zamiast tworzyć nowy.</span><span class="sxs-lookup"><span data-stu-id="af2a5-131">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="af2a5-132">Przykład 4: stosowanie wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="af2a5-132">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="af2a5-133">Polecenia w tym przykładzie tworzą i używają wstępnie zdefiniowanego znacznika.</span><span class="sxs-lookup"><span data-stu-id="af2a5-133">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="af2a5-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af2a5-134">PARAMETERS</span></span>

### <span data-ttu-id="af2a5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2a5-135">-DefaultProfile</span></span>
<span data-ttu-id="af2a5-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af2a5-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2a5-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af2a5-137">-Name</span></span>
<span data-ttu-id="af2a5-138">Określa nazwę znacznika.</span><span class="sxs-lookup"><span data-stu-id="af2a5-138">Specifies the tag name.</span></span>
<span data-ttu-id="af2a5-139">Aby utworzyć nowy wstępnie zdefiniowany znacznik, wprowadź unikatową nazwę.</span><span class="sxs-lookup"><span data-stu-id="af2a5-139">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="af2a5-140">Aby dodać wartość do istniejącego znacznika, wprowadź nazwę istniejącego znacznika.</span><span class="sxs-lookup"><span data-stu-id="af2a5-140">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="af2a5-141">Jeśli istniejący wstępnie zdefiniowany znacznik ma określoną nazwę, to polecenie **New-AzureRmTag** dodaje określoną wartość (jeśli istnieje) do znacznika o tej nazwie zamiast tworzyć nowy znacznik.</span><span class="sxs-lookup"><span data-stu-id="af2a5-141">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2a5-142">-Value</span><span class="sxs-lookup"><span data-stu-id="af2a5-142">-Value</span></span>
<span data-ttu-id="af2a5-143">Określa wartość znacznika.</span><span class="sxs-lookup"><span data-stu-id="af2a5-143">Specifies a tag value.</span></span>
<span data-ttu-id="af2a5-144">Wstępnie zdefiniowane Tagi mogą zawierać wiele wartości, ale w każdym poleceniu można wprowadzić tylko jedną wartość.</span><span class="sxs-lookup"><span data-stu-id="af2a5-144">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="af2a5-145">Ten parametr jest opcjonalny, ponieważ znaczniki mogą zawierać imiona i nazwiska bez wartości.</span><span class="sxs-lookup"><span data-stu-id="af2a5-145">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2a5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2a5-146">CommonParameters</span></span>
<span data-ttu-id="af2a5-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af2a5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2a5-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af2a5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2a5-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af2a5-149">INPUTS</span></span>

### <span data-ttu-id="af2a5-150">System. String</span><span class="sxs-lookup"><span data-stu-id="af2a5-150">System.String</span></span>

## <span data-ttu-id="af2a5-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af2a5-151">OUTPUTS</span></span>

### <span data-ttu-id="af2a5-152">Microsoft. Azure. Commands. resourceName. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="af2a5-152">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="af2a5-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af2a5-153">NOTES</span></span>

## <span data-ttu-id="af2a5-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af2a5-154">RELATED LINKS</span></span>

[<span data-ttu-id="af2a5-155">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="af2a5-155">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="af2a5-156">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="af2a5-156">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)

