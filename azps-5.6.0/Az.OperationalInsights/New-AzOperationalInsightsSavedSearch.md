---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: cba56fd21263d4accba296cd7aab181f18b09200
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989906"
---
# <span data-ttu-id="7944e-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="7944e-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="7944e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7944e-102">SYNOPSIS</span></span>
<span data-ttu-id="7944e-103">Tworzy nowe zapisane wyszukiwanie z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="7944e-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="7944e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7944e-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7944e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7944e-105">DESCRIPTION</span></span>
<span data-ttu-id="7944e-106">Polecenie **cmdlet New-AzOperationalInsightsSavedSearch** tworzy nowe zapisane wyszukiwanie z określonymi parametrami dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7944e-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="7944e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7944e-107">EXAMPLES</span></span>

### <span data-ttu-id="7944e-108">Przykład 1. Tworzenie nowego zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="7944e-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="7944e-109">To polecenie tworzy nowe zapisane wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="7944e-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="7944e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7944e-110">PARAMETERS</span></span>

### <span data-ttu-id="7944e-111">— Kategoria</span><span class="sxs-lookup"><span data-stu-id="7944e-111">-Category</span></span>
<span data-ttu-id="7944e-112">Określa nazwę kategorii.</span><span class="sxs-lookup"><span data-stu-id="7944e-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7944e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7944e-113">-DefaultProfile</span></span>
<span data-ttu-id="7944e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7944e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7944e-115">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="7944e-115">-DisplayName</span></span>
<span data-ttu-id="7944e-116">Określa zapisaną nazwę wyświetlaną wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="7944e-116">Specifies the saved search display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7944e-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7944e-117">-Force</span></span>
<span data-ttu-id="7944e-118">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7944e-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7944e-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="7944e-119">-FunctionAlias</span></span>
<span data-ttu-id="7944e-120">Alias funkcji, jeśli zapytanie pełni funkcję.</span><span class="sxs-lookup"><span data-stu-id="7944e-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7944e-121">-FunctionParameters</span><span class="sxs-lookup"><span data-stu-id="7944e-121">-FunctionParameter</span></span>
<span data-ttu-id="7944e-122">Opcjonalne parametry funkcji, jeśli zapytanie pełni funkcję.</span><span class="sxs-lookup"><span data-stu-id="7944e-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="7944e-123">Wartość powinna być w następującym formacie: 'nazwa-argumentu1:typ1 = default_value1; param-nazwa2:typ2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="7944e-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="7944e-124">Aby uzyskać więcej przykładów i prawidłową składnię, zobacz https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="7944e-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7944e-125">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="7944e-125">-Query</span></span>
<span data-ttu-id="7944e-126">Określa wyrażenie zapytania dla zapisanego wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="7944e-126">Specifies the query expression for the saved search.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7944e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7944e-127">-ResourceGroupName</span></span>
<span data-ttu-id="7944e-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7944e-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="7944e-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="7944e-129">-SavedSearchId</span></span>
<span data-ttu-id="7944e-130">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="7944e-130">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7944e-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="7944e-131">-Tag</span></span>
<span data-ttu-id="7944e-132">Zapisane tagi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="7944e-132">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7944e-133">— Wersja</span><span class="sxs-lookup"><span data-stu-id="7944e-133">-Version</span></span>
<span data-ttu-id="7944e-134">Określa wersję.</span><span class="sxs-lookup"><span data-stu-id="7944e-134">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7944e-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7944e-135">-WorkspaceName</span></span>
<span data-ttu-id="7944e-136">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7944e-136">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7944e-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7944e-137">-Confirm</span></span>
<span data-ttu-id="7944e-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7944e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7944e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7944e-139">-WhatIf</span></span>
<span data-ttu-id="7944e-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7944e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7944e-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7944e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7944e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7944e-142">CommonParameters</span></span>
<span data-ttu-id="7944e-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7944e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7944e-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7944e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7944e-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7944e-145">INPUTS</span></span>

### <span data-ttu-id="7944e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7944e-146">System.String</span></span>

### <span data-ttu-id="7944e-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7944e-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7944e-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="7944e-148">System.Int64</span></span>

## <span data-ttu-id="7944e-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7944e-149">OUTPUTS</span></span>

### <span data-ttu-id="7944e-150">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="7944e-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="7944e-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7944e-151">NOTES</span></span>

## <span data-ttu-id="7944e-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7944e-152">RELATED LINKS</span></span>

[<span data-ttu-id="7944e-153">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="7944e-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


