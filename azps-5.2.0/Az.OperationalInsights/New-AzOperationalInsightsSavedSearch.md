---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366788"
---
# <span data-ttu-id="e4804-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="e4804-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="e4804-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4804-102">SYNOPSIS</span></span>
<span data-ttu-id="e4804-103">Tworzy nowe zapisane wyszukiwanie przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="e4804-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="e4804-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4804-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4804-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4804-105">DESCRIPTION</span></span>
<span data-ttu-id="e4804-106">Polecenie cmdlet **New-AzOperationalInsightsSavedSearch** tworzy nowe zapisane wyszukiwanie przy użyciu określonych parametrów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e4804-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="e4804-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4804-107">EXAMPLES</span></span>

### <span data-ttu-id="e4804-108">Przykład 1. Tworzenie nowego zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="e4804-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="e4804-109">To polecenie tworzy nowe zapisane wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="e4804-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="e4804-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4804-110">PARAMETERS</span></span>

### <span data-ttu-id="e4804-111">-Category</span><span class="sxs-lookup"><span data-stu-id="e4804-111">-Category</span></span>
<span data-ttu-id="e4804-112">Określa nazwę kategorii.</span><span class="sxs-lookup"><span data-stu-id="e4804-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="e4804-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4804-113">-DefaultProfile</span></span>
<span data-ttu-id="e4804-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4804-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4804-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e4804-115">-DisplayName</span></span>
<span data-ttu-id="e4804-116">Określa zapisaną nazwę wyświetlaną wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="e4804-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="e4804-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e4804-117">-Force</span></span>
<span data-ttu-id="e4804-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e4804-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4804-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="e4804-119">-FunctionAlias</span></span>
<span data-ttu-id="e4804-120">Alias funkcji, jeśli kwerenda służy jako funkcja.</span><span class="sxs-lookup"><span data-stu-id="e4804-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="e4804-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="e4804-121">-FunctionParameter</span></span>
<span data-ttu-id="e4804-122">Opcjonalne parametry funkcji, jeśli kwerenda służy jako funkcja.</span><span class="sxs-lookup"><span data-stu-id="e4804-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="e4804-123">Wartość powinna mieć następujący format: "param-Name1: Type1 = default_value1, param-NAME2: Type2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="e4804-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="e4804-124">Więcej przykładów i poprawność składni można znaleźć w sekcji https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="e4804-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="e4804-125">-Query</span><span class="sxs-lookup"><span data-stu-id="e4804-125">-Query</span></span>
<span data-ttu-id="e4804-126">Określa wyrażenie zapytania dotyczącego zapisanego wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="e4804-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="e4804-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4804-127">-ResourceGroupName</span></span>
<span data-ttu-id="e4804-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4804-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="e4804-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="e4804-129">-SavedSearchId</span></span>
<span data-ttu-id="e4804-130">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="e4804-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="e4804-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4804-131">-Tag</span></span>
<span data-ttu-id="e4804-132">Zapisane Tagi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="e4804-132">The saved search tags.</span></span>

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

### <span data-ttu-id="e4804-133">-Version</span><span class="sxs-lookup"><span data-stu-id="e4804-133">-Version</span></span>
<span data-ttu-id="e4804-134">Określa wersję.</span><span class="sxs-lookup"><span data-stu-id="e4804-134">Specifies the version.</span></span>

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

### <span data-ttu-id="e4804-135">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="e4804-135">-WorkspaceName</span></span>
<span data-ttu-id="e4804-136">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e4804-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e4804-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4804-137">-Confirm</span></span>
<span data-ttu-id="e4804-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4804-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4804-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4804-139">-WhatIf</span></span>
<span data-ttu-id="e4804-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4804-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4804-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4804-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4804-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4804-142">CommonParameters</span></span>
<span data-ttu-id="e4804-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4804-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4804-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4804-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4804-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4804-145">INPUTS</span></span>

### <span data-ttu-id="e4804-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e4804-146">System.String</span></span>

### <span data-ttu-id="e4804-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4804-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e4804-148">System. Int64</span><span class="sxs-lookup"><span data-stu-id="e4804-148">System.Int64</span></span>

## <span data-ttu-id="e4804-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4804-149">OUTPUTS</span></span>

### <span data-ttu-id="e4804-150">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="e4804-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="e4804-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4804-151">NOTES</span></span>

## <span data-ttu-id="e4804-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4804-152">RELATED LINKS</span></span>

[<span data-ttu-id="e4804-153">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="e4804-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


