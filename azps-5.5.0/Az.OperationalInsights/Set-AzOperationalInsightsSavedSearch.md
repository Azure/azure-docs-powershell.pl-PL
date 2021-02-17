---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189395"
---
# <span data-ttu-id="1450a-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="1450a-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="1450a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1450a-102">SYNOPSIS</span></span>
<span data-ttu-id="1450a-103">Aktualizuje zapisane wyszukiwanie, które już istnieje.</span><span class="sxs-lookup"><span data-stu-id="1450a-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="1450a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1450a-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1450a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1450a-105">DESCRIPTION</span></span>
<span data-ttu-id="1450a-106">Polecenie **cmdlet Set-AzOperationalInsightsSavedSearch** aktualizuje zapisane wyszukiwanie, które już istnieje.</span><span class="sxs-lookup"><span data-stu-id="1450a-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="1450a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1450a-107">EXAMPLES</span></span>

### <span data-ttu-id="1450a-108">Przykład 1. Ustawianie zapisanego wyszukiwania ze zaktualizowanymi właściwościami</span><span class="sxs-lookup"><span data-stu-id="1450a-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="1450a-109">To polecenie ustawia zapisane wyszukiwanie ze zaktualizowanymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="1450a-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="1450a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1450a-110">PARAMETERS</span></span>

### <span data-ttu-id="1450a-111">— Kategoria</span><span class="sxs-lookup"><span data-stu-id="1450a-111">-Category</span></span>
<span data-ttu-id="1450a-112">Określa nazwę kategorii.</span><span class="sxs-lookup"><span data-stu-id="1450a-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="1450a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1450a-113">-DefaultProfile</span></span>
<span data-ttu-id="1450a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1450a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1450a-115">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="1450a-115">-DisplayName</span></span>
<span data-ttu-id="1450a-116">Określa nazwę wyświetlaną.</span><span class="sxs-lookup"><span data-stu-id="1450a-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="1450a-117">— ETag</span><span class="sxs-lookup"><span data-stu-id="1450a-117">-ETag</span></span>
<span data-ttu-id="1450a-118">Określa nazwę tagu ETag.</span><span class="sxs-lookup"><span data-stu-id="1450a-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1450a-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="1450a-119">-FunctionAlias</span></span>
<span data-ttu-id="1450a-120">Alias funkcji, jeśli zapytanie pełni funkcję.</span><span class="sxs-lookup"><span data-stu-id="1450a-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1450a-121">-FunctionParameters</span><span class="sxs-lookup"><span data-stu-id="1450a-121">-FunctionParameter</span></span>
<span data-ttu-id="1450a-122">Opcjonalne parametry funkcji, jeśli zapytanie pełni funkcję.</span><span class="sxs-lookup"><span data-stu-id="1450a-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="1450a-123">Wartość powinna być w następującym formacie: 'nazwa-argumentu1:typ1 = default_value1; param-nazwa2:typ2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="1450a-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="1450a-124">Aby uzyskać więcej przykładów i prawidłową składnię, zobacz https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="1450a-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1450a-125">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="1450a-125">-Query</span></span>
<span data-ttu-id="1450a-126">Określa nazwę zapytania.</span><span class="sxs-lookup"><span data-stu-id="1450a-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="1450a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1450a-127">-ResourceGroupName</span></span>
<span data-ttu-id="1450a-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1450a-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="1450a-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="1450a-129">-SavedSearchId</span></span>
<span data-ttu-id="1450a-130">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="1450a-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="1450a-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="1450a-131">-Tag</span></span>
<span data-ttu-id="1450a-132">Zapisane tagi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="1450a-132">The saved search tags.</span></span>

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

### <span data-ttu-id="1450a-133">— Wersja</span><span class="sxs-lookup"><span data-stu-id="1450a-133">-Version</span></span>
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

### <span data-ttu-id="1450a-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1450a-134">-WorkspaceName</span></span>
<span data-ttu-id="1450a-135">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="1450a-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="1450a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1450a-136">CommonParameters</span></span>
<span data-ttu-id="1450a-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1450a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1450a-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1450a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1450a-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1450a-139">INPUTS</span></span>

### <span data-ttu-id="1450a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1450a-140">System.String</span></span>

### <span data-ttu-id="1450a-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1450a-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1450a-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="1450a-142">System.Int64</span></span>

## <span data-ttu-id="1450a-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1450a-143">OUTPUTS</span></span>

### <span data-ttu-id="1450a-144">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="1450a-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="1450a-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1450a-145">NOTES</span></span>

## <span data-ttu-id="1450a-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1450a-146">RELATED LINKS</span></span>

[<span data-ttu-id="1450a-147">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="1450a-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


