---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184099"
---
# <span data-ttu-id="3a8f1-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3a8f1-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="3a8f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a8f1-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8f1-103">Tworzy nowe zapisane wyszukiwanie z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="3a8f1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a8f1-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a8f1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a8f1-105">DESCRIPTION</span></span>
<span data-ttu-id="3a8f1-106">Polecenie **cmdlet New-AzOperationalInsightsSavedSearch** tworzy nowe zapisane wyszukiwanie z określonymi parametrami dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="3a8f1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a8f1-107">EXAMPLES</span></span>

### <span data-ttu-id="3a8f1-108">Przykład 1. Tworzenie nowego zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="3a8f1-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="3a8f1-109">To polecenie tworzy nowe zapisane wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="3a8f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a8f1-110">PARAMETERS</span></span>

### <span data-ttu-id="3a8f1-111">— Kategoria</span><span class="sxs-lookup"><span data-stu-id="3a8f1-111">-Category</span></span>
<span data-ttu-id="3a8f1-112">Określa nazwę kategorii.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="3a8f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8f1-113">-DefaultProfile</span></span>
<span data-ttu-id="3a8f1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3a8f1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a8f1-115">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="3a8f1-115">-DisplayName</span></span>
<span data-ttu-id="3a8f1-116">Określa zapisaną nazwę wyświetlaną wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="3a8f1-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3a8f1-117">-Force</span></span>
<span data-ttu-id="3a8f1-118">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a8f1-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="3a8f1-119">-FunctionAlias</span></span>
<span data-ttu-id="3a8f1-120">Alias funkcji, jeśli zapytanie pełni funkcję.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="3a8f1-121">-FunctionParameters</span><span class="sxs-lookup"><span data-stu-id="3a8f1-121">-FunctionParameter</span></span>
<span data-ttu-id="3a8f1-122">Opcjonalne parametry funkcji, jeśli zapytanie pełni funkcję.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="3a8f1-123">Wartość powinna być w następującym formacie: 'nazwa-argumentu1:typ1 = default_value1; param-nazwa2:typ2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="3a8f1-124">Aby uzyskać więcej przykładów i prawidłową składnię, zobacz https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="3a8f1-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="3a8f1-125">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="3a8f1-125">-Query</span></span>
<span data-ttu-id="3a8f1-126">Określa wyrażenie zapytania dla zapisanego wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="3a8f1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8f1-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a8f1-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="3a8f1-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="3a8f1-129">-SavedSearchId</span></span>
<span data-ttu-id="3a8f1-130">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="3a8f1-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="3a8f1-131">-Tag</span></span>
<span data-ttu-id="3a8f1-132">Zapisane tagi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-132">The saved search tags.</span></span>

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

### <span data-ttu-id="3a8f1-133">— Wersja</span><span class="sxs-lookup"><span data-stu-id="3a8f1-133">-Version</span></span>
<span data-ttu-id="3a8f1-134">Określa wersję.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-134">Specifies the version.</span></span>

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

### <span data-ttu-id="3a8f1-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a8f1-135">-WorkspaceName</span></span>
<span data-ttu-id="3a8f1-136">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="3a8f1-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a8f1-137">-Confirm</span></span>
<span data-ttu-id="3a8f1-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a8f1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8f1-139">-WhatIf</span></span>
<span data-ttu-id="3a8f1-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a8f1-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a8f1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8f1-142">CommonParameters</span></span>
<span data-ttu-id="3a8f1-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a8f1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8f1-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a8f1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8f1-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a8f1-145">INPUTS</span></span>

### <span data-ttu-id="3a8f1-146">System.String</span><span class="sxs-lookup"><span data-stu-id="3a8f1-146">System.String</span></span>

### <span data-ttu-id="3a8f1-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3a8f1-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3a8f1-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="3a8f1-148">System.Int64</span></span>

## <span data-ttu-id="3a8f1-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a8f1-149">OUTPUTS</span></span>

### <span data-ttu-id="3a8f1-150">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="3a8f1-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="3a8f1-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a8f1-151">NOTES</span></span>

## <span data-ttu-id="3a8f1-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a8f1-152">RELATED LINKS</span></span>

[<span data-ttu-id="3a8f1-153">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="3a8f1-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


