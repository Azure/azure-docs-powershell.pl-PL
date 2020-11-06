---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 945af88df11e210c3af3a11bd69123dd32befe4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553400"
---
# <span data-ttu-id="1b1ef-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1b1ef-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="1b1ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1ef-103">Pobiera wstępnie zdefiniowane Tagi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b1ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b1ef-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b1ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b1ef-105">DESCRIPTION</span></span>
<span data-ttu-id="1b1ef-106">Polecenie cmdlet **Get-AzureRmTag** pobiera wstępnie zdefiniowane Tagi platformy Azure w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="1b1ef-107">To polecenie cmdlet zwraca podstawowe informacje o tagach lub szczegółowych informacjach na temat znaczników oraz ich wartości.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="1b1ef-108">Wszystkie obiekty wyjściowe zawierają Właściwość Count oznaczającą liczbę zasobów i grup zasobów, do których zastosowano znaczniki i wartości.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="1b1ef-109">Moduł Tagi platformy Azure, który jest częścią programu **AzureRMTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="1b1ef-110">Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="1b1ef-111">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="1b1ef-112">Aby utworzyć wstępnie zdefiniowany znacznik, użyj polecenia cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-112">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="1b1ef-113">Aby zastosować wstępnie zdefiniowany znacznik do grupy zasobów, użyj parametru *tag* polecenia cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="1b1ef-114">Aby wyszukać grupy zasobów dla konkretnej nazwy lub nazwy lub wartości znacznika, użyj parametru *tag* polecenia cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="1b1ef-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b1ef-115">EXAMPLES</span></span>

### <span data-ttu-id="1b1ef-116">Przykład 1. Pobierz wszystkie wstępnie zdefiniowane Tagi</span><span class="sxs-lookup"><span data-stu-id="1b1ef-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="1b1ef-117">To polecenie pobiera wszystkie wstępnie zdefiniowane Tagi w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="1b1ef-118">Właściwość Count wskazuje, ile razy znacznik został zastosowany do zasobów i grup zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="1b1ef-119">Przykład 2: uzyskiwanie tagu według nazwy</span><span class="sxs-lookup"><span data-stu-id="1b1ef-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="1b1ef-120">To polecenie pobiera szczegółowe informacje na temat znacznika działu i jego wartości.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="1b1ef-121">Właściwość Count wskazuje, ile razy znacznik i każda z jego wartości została zastosowana do zasobów i grup zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="1b1ef-122">Przykład 3: pobieranie wartości ze wszystkich znaczników</span><span class="sxs-lookup"><span data-stu-id="1b1ef-122">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzureRmTag -Detailed

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

<span data-ttu-id="1b1ef-123">To polecenie używa parametru *szczegółowy* , aby uzyskać szczegółowe informacje na temat wszystkich wstępnie zdefiniowanych znaczników w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="1b1ef-124">Użycie parametru *Szczegółowa* jest równoznaczne z użyciem parametru *name* dla każdego znacznika.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="1b1ef-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b1ef-125">PARAMETERS</span></span>

### <span data-ttu-id="1b1ef-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1ef-126">-DefaultProfile</span></span>
<span data-ttu-id="1b1ef-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b1ef-128">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="1b1ef-128">-Detailed</span></span>
<span data-ttu-id="1b1ef-129">Wskazuje, że ta operacja dodaje informacje o wartościach znaczników do danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-129">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1ef-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b1ef-130">-Name</span></span>
<span data-ttu-id="1b1ef-131">Określa nazwę znacznika, który ma być wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="1b1ef-132">Domyślnie polecenie **Get-AzureRmTag** pobiera podstawowe informacje o wszystkich wstępnie zdefiniowanych znacznikach w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-132">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="1b1ef-133">Gdy jest określany parametr *name* , parametr *szczegółowy* nie ma żadnego wpływu.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1ef-134">CommonParameters</span></span>
<span data-ttu-id="1b1ef-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1ef-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b1ef-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1ef-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b1ef-137">INPUTS</span></span>

### <span data-ttu-id="1b1ef-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1b1ef-138">System.String</span></span>

### <span data-ttu-id="1b1ef-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1b1ef-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1b1ef-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b1ef-140">OUTPUTS</span></span>

### <span data-ttu-id="1b1ef-141">Microsoft. Azure. Commands. resourceName. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="1b1ef-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="1b1ef-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b1ef-142">NOTES</span></span>

## <span data-ttu-id="1b1ef-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b1ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="1b1ef-144">Nowe — AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1b1ef-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="1b1ef-145">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1b1ef-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


