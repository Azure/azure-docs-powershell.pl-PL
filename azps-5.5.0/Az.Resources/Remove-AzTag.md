---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189219"
---
# <span data-ttu-id="81c31-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="81c31-101">Remove-AzTag</span></span>

## <span data-ttu-id="81c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81c31-102">SYNOPSIS</span></span>
<span data-ttu-id="81c31-103">Usuwa wstępnie zdefiniowane tagi lub wartości | Usuwa cały zestaw tagów dla zasobu lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="81c31-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="81c31-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="81c31-104">SYNTAX</span></span>

### <span data-ttu-id="81c31-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="81c31-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81c31-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81c31-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="81c31-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="81c31-107">DESCRIPTION</span></span>

<span data-ttu-id="81c31-108">**RemovePredefinedTagSet:** Polecenie cmdlet **Remove-AzTag** usuwa wstępnie zdefiniowane tagi i wartości platformy Azure z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="81c31-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="81c31-109">Aby usunąć określone wartości ze wstępnie zdefiniowanego tagu, użyj *parametru Value.*</span><span class="sxs-lookup"><span data-stu-id="81c31-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="81c31-110">Domyślnie **remove-aztag** usuwa określony tag i wszystkie jego wartości. Nie można usunąć tagu ani wartości, które są obecnie stosowane do zasobu lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81c31-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="81c31-111">Przed użyciem **polecenia Remove-AzTag** użyj parametru *Tag* Set-AzResourceGroup cmdlet, aby usunąć tag lub wartości z zasobu lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81c31-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="81c31-112">Moduł Tagi platformy Azure, do których należy **remove-aztag,** może ułatwić zarządzanie wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="81c31-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="81c31-113">Tag Azure to para wartości nazw, za pomocą których można kategoryzować zasoby platformy Azure i grupy zasobów, na przykład według działów lub centrum kosztów, a także śledzić notatki i komentarze dotyczące zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="81c31-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="81c31-114">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane tagi pozwalają ustalić standardowe, spójne i przewidywalne nazwy oraz wartości tagów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="81c31-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="81c31-115">**RemoveByResourceIdParameterSet:** Polecenie cmdlet **Remove-AzTag** z tagiem **ResourceId** usuwa cały zestaw tagów zasobu lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="81c31-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="81c31-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="81c31-116">EXAMPLES</span></span>

### <span data-ttu-id="81c31-117">Przykład 1. Usuwanie wstępnie zdefiniowanego tagu</span><span class="sxs-lookup"><span data-stu-id="81c31-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="81c31-118">To polecenie usuwa wstępnie zdefiniowany tag o nazwie Dział i wszystkie jego wartości.</span><span class="sxs-lookup"><span data-stu-id="81c31-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="81c31-119">Jeśli tag został zastosowany do jakichkolwiek zasobów lub grup zasobów, polecenie kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="81c31-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="81c31-120">Przykład 2. Usuwanie wartości ze wstępnie zdefiniowanego tagu</span><span class="sxs-lookup"><span data-stu-id="81c31-120">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="81c31-121">To polecenie usuwa wartość HumanResources ze wstępnie zdefiniowanego tagu Department (Dział).</span><span class="sxs-lookup"><span data-stu-id="81c31-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="81c31-122">Tag nie jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="81c31-122">It does not delete the tag.</span></span>
<span data-ttu-id="81c31-123">Jeśli wartość została zastosowana do jakichkolwiek zasobów lub grup zasobów, polecenie kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="81c31-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="81c31-124">Przykład 3. Usuwanie całego zestawu tagów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="81c31-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="81c31-125">To polecenie spowoduje usunięcie całego zestawu tagów w subskrypcji za pomocą {subId}.</span><span class="sxs-lookup"><span data-stu-id="81c31-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="81c31-126">Nie zwróci on usuniętego obiektu, jeśli nie przejdzie w "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="81c31-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="81c31-127">Przykład 4. Usuwanie całego zestawu tagów zasobu</span><span class="sxs-lookup"><span data-stu-id="81c31-127">Example 4: Deletes the entire set of tags on a resource</span></span>

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

<span data-ttu-id="81c31-128">To polecenie usuwa cały zestaw tagów zasobu za pomocą {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="81c31-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="81c31-129">Zwraca usunięty oject podczas przechodzenia w "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="81c31-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="81c31-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81c31-130">PARAMETERS</span></span>

### <span data-ttu-id="81c31-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c31-131">-DefaultProfile</span></span>
<span data-ttu-id="81c31-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="81c31-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c31-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="81c31-133">-Name</span></span>
<span data-ttu-id="81c31-134">Określa nazwę wstępnie zdefiniowanego tagu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="81c31-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="81c31-135">Domyślnie **remove-aztag** usuwa określony tag i wszystkie jego wartości.</span><span class="sxs-lookup"><span data-stu-id="81c31-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="81c31-136">Aby usunąć wybrane wartości, ale nie usunąć tagu, użyj *parametru Value.*</span><span class="sxs-lookup"><span data-stu-id="81c31-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="81c31-137">— Wartość</span><span class="sxs-lookup"><span data-stu-id="81c31-137">-Value</span></span>
<span data-ttu-id="81c31-138">Usuwa określone wartości ze wstępnie zdefiniowanego tagu, ale nie usuwa tagu.</span><span class="sxs-lookup"><span data-stu-id="81c31-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="81c31-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81c31-139">-ResourceId</span></span>
<span data-ttu-id="81c31-140">Identyfikator zasobu dla otagowanego elementu.</span><span class="sxs-lookup"><span data-stu-id="81c31-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="81c31-141">Może zostać otagowany zasób, grupa zasobów lub subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="81c31-141">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="81c31-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81c31-142">-PassThru</span></span>
<span data-ttu-id="81c31-143">Zwraca obiekt reprezentujący usunięty tag lub końcowy tag z usuniętymi wartościami.</span><span class="sxs-lookup"><span data-stu-id="81c31-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="81c31-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81c31-144">-Confirm</span></span>
<span data-ttu-id="81c31-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="81c31-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c31-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c31-146">-WhatIf</span></span>
<span data-ttu-id="81c31-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81c31-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81c31-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="81c31-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c31-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c31-149">CommonParameters</span></span>
<span data-ttu-id="81c31-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81c31-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c31-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81c31-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c31-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81c31-152">INPUTS</span></span>

### <span data-ttu-id="81c31-153">System.String</span><span class="sxs-lookup"><span data-stu-id="81c31-153">System.String</span></span>

### <span data-ttu-id="81c31-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="81c31-154">System.String[]</span></span>

### <span data-ttu-id="81c31-155">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="81c31-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81c31-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81c31-156">OUTPUTS</span></span>

### <span data-ttu-id="81c31-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="81c31-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="81c31-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="81c31-158">NOTES</span></span>

## <span data-ttu-id="81c31-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81c31-159">RELATED LINKS</span></span>

[<span data-ttu-id="81c31-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="81c31-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="81c31-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="81c31-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="81c31-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="81c31-162">Update-AzTag</span></span>](./Update-AzTag.md)