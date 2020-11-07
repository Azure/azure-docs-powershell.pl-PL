---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: f9afc10613024d99cfa6b03b260324b3e5d22586
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708291"
---
# <span data-ttu-id="85647-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="85647-101">Remove-AzTag</span></span>

## <span data-ttu-id="85647-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85647-102">SYNOPSIS</span></span>
<span data-ttu-id="85647-103">Usuwa wstępnie zdefiniowane Tagi lub wartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85647-103">Deletes predefined Azure tags or values.</span></span>

## <span data-ttu-id="85647-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85647-104">SYNTAX</span></span>

```
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85647-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85647-105">DESCRIPTION</span></span>
<span data-ttu-id="85647-106">Polecenie cmdlet **Remove-AzTag** usuwa wstępnie zdefiniowane Tagi i wartości platformy Azure z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="85647-106">The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="85647-107">Aby usunąć określone wartości ze wstępnie zdefiniowanego znacznika, należy użyć parametru *Value* .</span><span class="sxs-lookup"><span data-stu-id="85647-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="85647-108">Domyślnie polecenie **Remove-AzTag** usuwa określony znacznik i wszystkie jego wartości. Nie można usunąć znacznika lub wartości, która jest obecnie zastosowana do zasobu lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85647-108">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="85647-109">Przed użyciem polecenia **Remove-AzTag** Użyj parametru *Tag* polecenia cmdlet Set-AzResourceGroup, aby usunąć znacznik lub wartości z grupy zasób lub zasób.</span><span class="sxs-lookup"><span data-stu-id="85647-109">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="85647-110">Moduł Tagi platformy Azure, który jest częścią funkcji **Remove-AzTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85647-110">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="85647-111">Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="85647-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="85647-112">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="85647-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="85647-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85647-113">EXAMPLES</span></span>

### <span data-ttu-id="85647-114">Przykład 1. Usuń wstępnie zdefiniowany tag</span><span class="sxs-lookup"><span data-stu-id="85647-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="85647-115">To polecenie powoduje usunięcie wstępnie zdefiniowanego tagu o nazwie dział i wszystkich jego zasobów.</span><span class="sxs-lookup"><span data-stu-id="85647-115">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="85647-116">Jeśli znacznik został zastosowany do żadnych zasobów lub grup zasobów, wykonanie polecenia nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="85647-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="85647-117">Przykład 2: usuwanie wartości ze wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="85647-117">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="85647-118">To polecenie usuwa wartość HumanResources ze znacznika uprzednio zdefiniowanego działu.</span><span class="sxs-lookup"><span data-stu-id="85647-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="85647-119">Nie powoduje usunięcia znacznika.</span><span class="sxs-lookup"><span data-stu-id="85647-119">It does not delete the tag.</span></span>
<span data-ttu-id="85647-120">Jeśli wartość została zastosowana do żadnych zasobów lub grup zasobów, wykonanie polecenia nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="85647-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="85647-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85647-121">PARAMETERS</span></span>

### <span data-ttu-id="85647-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85647-122">-DefaultProfile</span></span>
<span data-ttu-id="85647-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85647-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85647-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85647-124">-Name</span></span>
<span data-ttu-id="85647-125">Określa nazwę znacznika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="85647-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="85647-126">Domyślnie polecenie **Remove-AzTag** usuwa określony znacznik i wszystkie jego wartości.</span><span class="sxs-lookup"><span data-stu-id="85647-126">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="85647-127">Aby usunąć zaznaczone wartości, ale nie usuwać znacznika, użyj parametru *Value* .</span><span class="sxs-lookup"><span data-stu-id="85647-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="85647-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85647-128">-PassThru</span></span>
<span data-ttu-id="85647-129">Zwraca obiekt reprezentujący usunięty znacznik lub wynikowy znacznik z usuniętymi wartościami.</span><span class="sxs-lookup"><span data-stu-id="85647-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="85647-130">-Value</span><span class="sxs-lookup"><span data-stu-id="85647-130">-Value</span></span>
<span data-ttu-id="85647-131">Usuwa określone wartości ze wstępnie zdefiniowanego znacznika, ale nie usuwa znacznika.</span><span class="sxs-lookup"><span data-stu-id="85647-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85647-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85647-132">-Confirm</span></span>
<span data-ttu-id="85647-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85647-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85647-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85647-134">-WhatIf</span></span>
<span data-ttu-id="85647-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85647-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85647-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85647-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85647-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85647-137">CommonParameters</span></span>
<span data-ttu-id="85647-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85647-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85647-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85647-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85647-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85647-140">INPUTS</span></span>

### <span data-ttu-id="85647-141">System. String</span><span class="sxs-lookup"><span data-stu-id="85647-141">System.String</span></span>

### <span data-ttu-id="85647-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="85647-142">System.String[]</span></span>

### <span data-ttu-id="85647-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="85647-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="85647-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85647-144">OUTPUTS</span></span>

### <span data-ttu-id="85647-145">Microsoft. Azure. Commands. resourceName. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="85647-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="85647-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85647-146">NOTES</span></span>

## <span data-ttu-id="85647-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85647-147">RELATED LINKS</span></span>

[<span data-ttu-id="85647-148">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="85647-148">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="85647-149">Nowe — AzTag</span><span class="sxs-lookup"><span data-stu-id="85647-149">New-AzTag</span></span>](./New-AzTag.md)


