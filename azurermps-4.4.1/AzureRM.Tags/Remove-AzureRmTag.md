---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 909781b8cd441daab8bf5f567404a5e99e88cd0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718670"
---
# <span data-ttu-id="9a7a4-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="9a7a4-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="9a7a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7a4-103">Usuwa wstępnie zdefiniowane Tagi lub wartości platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a7a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a7a4-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a7a4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9a7a4-105">DESCRIPTION</span></span>
<span data-ttu-id="9a7a4-106">Polecenie cmdlet **Remove-AzureRmTag** usuwa wstępnie zdefiniowane Tagi i wartości platformy Azure z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="9a7a4-107">Aby usunąć określone wartości ze wstępnie zdefiniowanego znacznika, należy użyć parametru *Value* .</span><span class="sxs-lookup"><span data-stu-id="9a7a4-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="9a7a4-108">Domyślnie polecenie **Remove-AzureRmTag** usuwa określony znacznik i wszystkie jego wartości. Nie można usunąć znacznika lub wartości, która jest obecnie zastosowana do zasobu lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>

<span data-ttu-id="9a7a4-109">Przed użyciem polecenia **Remove-AzureRmTag** Użyj parametru *Tag* polecenia cmdlet Set-AzureRMResourceGroup, aby usunąć znacznik lub wartości z grupy zasób lub zasób.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>

<span data-ttu-id="9a7a4-110">Moduł Tagi platformy Azure, który jest częścią funkcji **Remove-AzureRmTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="9a7a4-111">Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="9a7a4-112">Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="9a7a4-113">Jeśli subskrypcja zawiera wszystkie wstępnie zdefiniowane Tagi, nie można stosować niezdefiniowanych tagów ani wartości do żadnych zasobów lub grup zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-113">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

## <span data-ttu-id="9a7a4-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a7a4-114">EXAMPLES</span></span>

### <span data-ttu-id="9a7a4-115">Przykład 1. Usuń wstępnie zdefiniowany tag</span><span class="sxs-lookup"><span data-stu-id="9a7a4-115">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="9a7a4-116">To polecenie powoduje usunięcie wstępnie zdefiniowanego tagu o nazwie dział i wszystkich jego zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-116">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="9a7a4-117">Jeśli znacznik został zastosowany do żadnych zasobów lub grup zasobów, wykonanie polecenia nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-117">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="9a7a4-118">Przykład 2: usuwanie wartości ze wstępnie zdefiniowanego znacznika</span><span class="sxs-lookup"><span data-stu-id="9a7a4-118">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="9a7a4-119">To polecenie usuwa wartość HumanResources ze znacznika uprzednio zdefiniowanego działu.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-119">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="9a7a4-120">Nie powoduje usunięcia znacznika.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-120">It does not delete the tag.</span></span>
<span data-ttu-id="9a7a4-121">Jeśli wartość została zastosowana do żadnych zasobów lub grup zasobów, wykonanie polecenia nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-121">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="9a7a4-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a7a4-122">PARAMETERS</span></span>

### <span data-ttu-id="9a7a4-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a7a4-123">-Name</span></span>
<span data-ttu-id="9a7a4-124">Określa nazwę znacznika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-124">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="9a7a4-125">Domyślnie polecenie **Remove-AzureRmTag** usuwa określony znacznik i wszystkie jego wartości.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-125">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="9a7a4-126">Aby usunąć zaznaczone wartości, ale nie usuwać znacznika, użyj parametru *Value* .</span><span class="sxs-lookup"><span data-stu-id="9a7a4-126">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="9a7a4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a7a4-127">-PassThru</span></span>
<span data-ttu-id="9a7a4-128">Zwraca obiekt reprezentujący usunięty znacznik lub wynikowy znacznik z usuniętymi wartościami.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-128">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="9a7a4-129">-Value</span><span class="sxs-lookup"><span data-stu-id="9a7a4-129">-Value</span></span>
<span data-ttu-id="9a7a4-130">Usuwa określone wartości ze wstępnie zdefiniowanego znacznika, ale nie usuwa znacznika.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-130">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="9a7a4-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a7a4-131">-Confirm</span></span>
<span data-ttu-id="9a7a4-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a7a4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a7a4-133">-WhatIf</span></span>
<span data-ttu-id="9a7a4-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a7a4-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a7a4-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a7a4-136">-DefaultProfile</span></span>
<span data-ttu-id="9a7a4-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a7a4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7a4-138">CommonParameters</span></span>
<span data-ttu-id="9a7a4-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a7a4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7a4-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a7a4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7a4-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a7a4-141">INPUTS</span></span>

### <span data-ttu-id="9a7a4-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9a7a4-142">None</span></span>

## <span data-ttu-id="9a7a4-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a7a4-143">OUTPUTS</span></span>

### <span data-ttu-id="9a7a4-144">Brak lub Microsoft. Azure. Commands. Tags. model. PSTag</span><span class="sxs-lookup"><span data-stu-id="9a7a4-144">None or Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="9a7a4-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a7a4-145">NOTES</span></span>

## <span data-ttu-id="9a7a4-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a7a4-146">RELATED LINKS</span></span>

[<span data-ttu-id="9a7a4-147">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="9a7a4-147">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="9a7a4-148">Nowe — AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="9a7a4-148">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


