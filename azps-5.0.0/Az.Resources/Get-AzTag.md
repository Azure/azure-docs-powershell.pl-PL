---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308820"
---
# <span data-ttu-id="25367-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="25367-101">Get-AzTag</span></span>

## <span data-ttu-id="25367-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25367-102">SYNOPSIS</span></span>
<span data-ttu-id="25367-103">Pobiera wstępnie zdefiniowane Tagi platformy Azure | Pobiera cały zestaw tagów zasobu lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="25367-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="25367-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25367-104">SYNTAX</span></span>

### <span data-ttu-id="25367-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="25367-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25367-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25367-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25367-107">Opis</span><span class="sxs-lookup"><span data-stu-id="25367-107">DESCRIPTION</span></span>

<span data-ttu-id="25367-108">**GetPredefinedTagSet** : polecenie cmdlet **Get-AzTag** pobiera wstępnie zdefiniowane Tagi platformy Azure w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="25367-108">**GetPredefinedTagSet** : The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="25367-109">To polecenie cmdlet zwraca podstawowe informacje o tagach lub szczegółowych informacjach na temat znaczników oraz ich wartości.</span><span class="sxs-lookup"><span data-stu-id="25367-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="25367-110">Wszystkie obiekty wyjściowe zawierają Właściwość Count oznaczającą liczbę zasobów i grup zasobów, do których zastosowano znaczniki i wartości.</span><span class="sxs-lookup"><span data-stu-id="25367-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="25367-111">Moduł Tagi platformy Azure, który jest częścią programu **AzTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="25367-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="25367-112">Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="25367-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="25367-113">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="25367-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="25367-114">Aby utworzyć wstępnie zdefiniowany znacznik, użyj polecenia cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="25367-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="25367-115">Aby zastosować wstępnie zdefiniowany znacznik do grupy zasobów, użyj parametru *tag* polecenia cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="25367-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="25367-116">Aby wyszukać grupy zasobów dla konkretnej nazwy lub nazwy lub wartości znacznika, użyj parametru *tag* polecenia cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="25367-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="25367-117">**GetByResourceIdParameterSet** : polecenie cmdlet **Get-AzTag** z identyfikatorem zasobu zasobu lub abonamentem **Pobiera cały** zestaw tagów.</span><span class="sxs-lookup"><span data-stu-id="25367-117">**GetByResourceIdParameterSet** : The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="25367-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25367-118">EXAMPLES</span></span>

### <span data-ttu-id="25367-119">Przykład 1. Pobierz wszystkie wstępnie zdefiniowane Tagi</span><span class="sxs-lookup"><span data-stu-id="25367-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="25367-120">To polecenie pobiera wszystkie wstępnie zdefiniowane Tagi w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="25367-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="25367-121">Właściwość Count wskazuje, ile razy znacznik został zastosowany do zasobów i grup zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="25367-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="25367-122">Przykład 2: uzyskiwanie tagu według nazwy</span><span class="sxs-lookup"><span data-stu-id="25367-122">Example 2: Get a tag by name</span></span>
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

<span data-ttu-id="25367-123">To polecenie pobiera szczegółowe informacje na temat znacznika działu i jego wartości.</span><span class="sxs-lookup"><span data-stu-id="25367-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="25367-124">Właściwość Count wskazuje, ile razy znacznik i każda z jego wartości została zastosowana do zasobów i grup zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="25367-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="25367-125">Przykład 3: pobieranie wartości ze wszystkich znaczników</span><span class="sxs-lookup"><span data-stu-id="25367-125">Example 3: Get values of all tags</span></span>
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

<span data-ttu-id="25367-126">To polecenie używa parametru *szczegółowy* , aby uzyskać szczegółowe informacje na temat wszystkich wstępnie zdefiniowanych znaczników w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="25367-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="25367-127">Użycie parametru *Szczegółowa* jest równoznaczne z użyciem parametru *name* dla każdego znacznika.</span><span class="sxs-lookup"><span data-stu-id="25367-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="25367-128">Przykład 4: pobieranie całego zestawu tagów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="25367-128">Example 4: Get the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="25367-129">To polecenie pobiera cały zestaw tagów w subskrypcji przy użyciu programu {subId}.</span><span class="sxs-lookup"><span data-stu-id="25367-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="25367-130">Przykład 5: pobieranie całego zestawu tagów w zasobie</span><span class="sxs-lookup"><span data-stu-id="25367-130">Example 5: Get the entire set of tags on a resource</span></span>

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

<span data-ttu-id="25367-131">To polecenie pobiera cały zestaw tagów z zasobu o identyfikatorze {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="25367-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="25367-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25367-132">PARAMETERS</span></span>

### <span data-ttu-id="25367-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25367-133">-DefaultProfile</span></span>
<span data-ttu-id="25367-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25367-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25367-135">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="25367-135">-Detailed</span></span>
<span data-ttu-id="25367-136">Wskazuje, że ta operacja dodaje informacje o wartościach znaczników do danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="25367-136">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="25367-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25367-137">-Name</span></span>
<span data-ttu-id="25367-138">Nazwa wstępnie zdefiniowanego znacznika.</span><span class="sxs-lookup"><span data-stu-id="25367-138">Name of the predefined tag.</span></span>
<span data-ttu-id="25367-139">Domyślnie polecenie **Get-AzTag** pobiera podstawowe informacje o wszystkich wstępnie zdefiniowanych znacznikach w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="25367-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="25367-140">Gdy jest określany parametr *name* , parametr *szczegółowy* nie ma żadnego wpływu.</span><span class="sxs-lookup"><span data-stu-id="25367-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="25367-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25367-141">-ResourceId</span></span>
<span data-ttu-id="25367-142">Identyfikator zasobu oznakowanej jednostki.</span><span class="sxs-lookup"><span data-stu-id="25367-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="25367-143">Zasób, Grupa zasobów lub abonament mogą być oznakowane.</span><span class="sxs-lookup"><span data-stu-id="25367-143">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="25367-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25367-144">CommonParameters</span></span>
<span data-ttu-id="25367-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25367-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25367-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25367-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25367-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25367-147">INPUTS</span></span>

### <span data-ttu-id="25367-148">System. String</span><span class="sxs-lookup"><span data-stu-id="25367-148">System.String</span></span>

### <span data-ttu-id="25367-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25367-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="25367-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25367-150">OUTPUTS</span></span>

### <span data-ttu-id="25367-151">Microsoft. Azure. Commands. resourceName. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="25367-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="25367-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25367-152">NOTES</span></span>

## <span data-ttu-id="25367-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25367-153">RELATED LINKS</span></span>

[<span data-ttu-id="25367-154">Nowe — AzTag</span><span class="sxs-lookup"><span data-stu-id="25367-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="25367-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="25367-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="25367-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="25367-156">Update-AzTag</span></span>](./Update-AzTag.md)
