---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354826"
---
# <span data-ttu-id="05969-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="05969-101">Remove-AzTag</span></span>

## <span data-ttu-id="05969-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05969-102">SYNOPSIS</span></span>
<span data-ttu-id="05969-103">Usuwa wstępnie zdefiniowane Tagi lub wartości platformy Azure | Usuwa cały zestaw tagów zasobu lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="05969-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="05969-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05969-104">SYNTAX</span></span>

### <span data-ttu-id="05969-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="05969-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05969-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05969-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="05969-107">Opis</span><span class="sxs-lookup"><span data-stu-id="05969-107">DESCRIPTION</span></span>

<span data-ttu-id="05969-108">**RemovePredefinedTagSet**: polecenie cmdlet **Remove-AzTag** usuwa wstępnie zdefiniowane Tagi i wartości platformy Azure z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="05969-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="05969-109">Aby usunąć określone wartości ze wstępnie zdefiniowanego znacznika, należy użyć parametru *Value* .</span><span class="sxs-lookup"><span data-stu-id="05969-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="05969-110">Domyślnie polecenie **Remove-AzTag** usuwa określony znacznik i wszystkie jego wartości. Nie można usunąć znacznika lub wartości, która jest obecnie zastosowana do zasobu lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05969-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="05969-111">Przed użyciem polecenia **Remove-AzTag** Użyj parametru *Tag* polecenia cmdlet Set-AzResourceGroup, aby usunąć znacznik lub wartości z grupy zasób lub zasób.</span><span class="sxs-lookup"><span data-stu-id="05969-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="05969-112">Moduł Tagi platformy Azure, który jest częścią funkcji **Remove-AzTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="05969-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="05969-113">Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="05969-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="05969-114">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="05969-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="05969-115">**RemoveByResourceIdParameterSet**: polecenie cmdlet **Remove-AzTag** z identyfikatorem **ResourceID** powoduje usunięcie całego zestawu tagów w zasobie lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="05969-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="05969-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05969-116">EXAMPLES</span></span>

### <span data-ttu-id="05969-117">Przykład 1. Usuń wstępnie zdefiniowany tag</span><span class="sxs-lookup"><span data-stu-id="05969-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="05969-118">To polecenie powoduje usunięcie wstępnie zdefiniowanego tagu o nazwie dział i wszystkich jego wartości.</span><span class="sxs-lookup"><span data-stu-id="05969-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="05969-119">Jeśli znacznik został zastosowany do żadnych zasobów lub grup zasobów, wykonanie polecenia nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="05969-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="05969-120">Przykład 2: usuwanie wartości ze wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="05969-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="05969-121">To polecenie usuwa wartość HumanResources ze znacznika uprzednio zdefiniowanego działu.</span><span class="sxs-lookup"><span data-stu-id="05969-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="05969-122">Nie powoduje usunięcia znacznika.</span><span class="sxs-lookup"><span data-stu-id="05969-122">It does not delete the tag.</span></span>
<span data-ttu-id="05969-123">Jeśli wartość została zastosowana do żadnych zasobów lub grup zasobów, wykonanie polecenia nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="05969-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="05969-124">Przykład 3: usunięcie całego zestawu tagów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="05969-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="05969-125">To polecenie usuwa cały zestaw tagów z subskrypcji przy użyciu programu {subId}.</span><span class="sxs-lookup"><span data-stu-id="05969-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="05969-126">Nie zwróci on usuniętego obiektu, jeśli nie przejdzie w "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="05969-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="05969-127">Przykład 4: usuwanie całego zestawu tagów w zasobie</span><span class="sxs-lookup"><span data-stu-id="05969-127">Example 4: Deletes the entire set of tags on a resource</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="05969-128">To polecenie usuwa cały zestaw tagów z zasobu o identyfikatorze {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="05969-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="05969-129">Funkcja zwraca usunięte oject podczas przekazywania "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="05969-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="05969-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05969-130">PARAMETERS</span></span>

### <span data-ttu-id="05969-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05969-131">-DefaultProfile</span></span>
<span data-ttu-id="05969-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05969-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05969-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05969-133">-Name</span></span>
<span data-ttu-id="05969-134">Określa nazwę wstępnie zdefiniowanego tagu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="05969-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="05969-135">Domyślnie polecenie **Remove-AzTag** usuwa określony znacznik i wszystkie jego wartości.</span><span class="sxs-lookup"><span data-stu-id="05969-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="05969-136">Aby usunąć zaznaczone wartości, ale nie usuwać znacznika, użyj parametru *Value* .</span><span class="sxs-lookup"><span data-stu-id="05969-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05969-137">-Value</span><span class="sxs-lookup"><span data-stu-id="05969-137">-Value</span></span>
<span data-ttu-id="05969-138">Usuwa określone wartości ze wstępnie zdefiniowanego znacznika, ale nie usuwa znacznika.</span><span class="sxs-lookup"><span data-stu-id="05969-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05969-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05969-139">-ResourceId</span></span>
<span data-ttu-id="05969-140">Identyfikator zasobu oznakowanej jednostki.</span><span class="sxs-lookup"><span data-stu-id="05969-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="05969-141">Zasób, Grupa zasobów lub abonament mogą być oznakowane.</span><span class="sxs-lookup"><span data-stu-id="05969-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05969-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05969-142">-PassThru</span></span>
<span data-ttu-id="05969-143">Zwraca obiekt reprezentujący usunięty znacznik lub wynikowy znacznik z usuniętymi wartościami.</span><span class="sxs-lookup"><span data-stu-id="05969-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="05969-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05969-144">-Confirm</span></span>
<span data-ttu-id="05969-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05969-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05969-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05969-146">-WhatIf</span></span>
<span data-ttu-id="05969-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05969-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05969-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05969-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05969-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05969-149">CommonParameters</span></span>
<span data-ttu-id="05969-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05969-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05969-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05969-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05969-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05969-152">INPUTS</span></span>

### <span data-ttu-id="05969-153">System. String</span><span class="sxs-lookup"><span data-stu-id="05969-153">System.String</span></span>

### <span data-ttu-id="05969-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="05969-154">System.String[]</span></span>

### <span data-ttu-id="05969-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="05969-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="05969-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05969-156">OUTPUTS</span></span>

### <span data-ttu-id="05969-157">Microsoft. Azure. Commands. resourceName. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="05969-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="05969-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05969-158">NOTES</span></span>

## <span data-ttu-id="05969-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05969-159">RELATED LINKS</span></span>

[<span data-ttu-id="05969-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="05969-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="05969-161">Nowe — AzTag</span><span class="sxs-lookup"><span data-stu-id="05969-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="05969-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="05969-162">Update-AzTag</span></span>](./Update-AzTag.md)