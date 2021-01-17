---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378595"
---
# <span data-ttu-id="57bef-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="57bef-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="57bef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57bef-102">SYNOPSIS</span></span>
<span data-ttu-id="57bef-103">Umożliwia zaktualizowanie zapisanego wyszukiwania, które już istnieje.</span><span class="sxs-lookup"><span data-stu-id="57bef-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="57bef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57bef-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57bef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57bef-105">DESCRIPTION</span></span>
<span data-ttu-id="57bef-106">Polecenie cmdlet **Set-AzOperationalInsightsSavedSearch** umożliwia zaktualizowanie zapisanego wyszukiwania, które już istnieje.</span><span class="sxs-lookup"><span data-stu-id="57bef-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="57bef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57bef-107">EXAMPLES</span></span>

### <span data-ttu-id="57bef-108">Przykład 1. ustawia zapisane wyszukiwanie ze zaktualizowanymi właściwościami</span><span class="sxs-lookup"><span data-stu-id="57bef-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="57bef-109">To polecenie umożliwia ustawienie zapisanego wyszukiwania przy użyciu zaktualizowanych właściwości.</span><span class="sxs-lookup"><span data-stu-id="57bef-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="57bef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57bef-110">PARAMETERS</span></span>

### <span data-ttu-id="57bef-111">-Category</span><span class="sxs-lookup"><span data-stu-id="57bef-111">-Category</span></span>
<span data-ttu-id="57bef-112">Określa nazwę kategorii.</span><span class="sxs-lookup"><span data-stu-id="57bef-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="57bef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57bef-113">-DefaultProfile</span></span>
<span data-ttu-id="57bef-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="57bef-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57bef-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="57bef-115">-DisplayName</span></span>
<span data-ttu-id="57bef-116">Określa nazwę wyświetlaną.</span><span class="sxs-lookup"><span data-stu-id="57bef-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="57bef-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="57bef-117">-ETag</span></span>
<span data-ttu-id="57bef-118">Określa nazwę elementu ETag.</span><span class="sxs-lookup"><span data-stu-id="57bef-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="57bef-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="57bef-119">-FunctionAlias</span></span>
<span data-ttu-id="57bef-120">Alias funkcji, jeśli kwerenda służy jako funkcja.</span><span class="sxs-lookup"><span data-stu-id="57bef-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="57bef-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="57bef-121">-FunctionParameter</span></span>
<span data-ttu-id="57bef-122">Opcjonalne parametry funkcji, jeśli kwerenda służy jako funkcja.</span><span class="sxs-lookup"><span data-stu-id="57bef-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="57bef-123">Wartość powinna mieć następujący format: "param-Name1: Type1 = default_value1, param-NAME2: Type2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="57bef-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="57bef-124">Więcej przykładów i poprawność składni można znaleźć w sekcji https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="57bef-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="57bef-125">-Query</span><span class="sxs-lookup"><span data-stu-id="57bef-125">-Query</span></span>
<span data-ttu-id="57bef-126">Określa nazwę zapytania.</span><span class="sxs-lookup"><span data-stu-id="57bef-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="57bef-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57bef-127">-ResourceGroupName</span></span>
<span data-ttu-id="57bef-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57bef-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="57bef-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="57bef-129">-SavedSearchId</span></span>
<span data-ttu-id="57bef-130">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="57bef-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="57bef-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="57bef-131">-Tag</span></span>
<span data-ttu-id="57bef-132">Zapisane Tagi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="57bef-132">The saved search tags.</span></span>

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

### <span data-ttu-id="57bef-133">-Version</span><span class="sxs-lookup"><span data-stu-id="57bef-133">-Version</span></span>
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

### <span data-ttu-id="57bef-134">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="57bef-134">-WorkspaceName</span></span>
<span data-ttu-id="57bef-135">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="57bef-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="57bef-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57bef-136">CommonParameters</span></span>
<span data-ttu-id="57bef-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57bef-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57bef-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57bef-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57bef-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57bef-139">INPUTS</span></span>

### <span data-ttu-id="57bef-140">System. String</span><span class="sxs-lookup"><span data-stu-id="57bef-140">System.String</span></span>

### <span data-ttu-id="57bef-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="57bef-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="57bef-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="57bef-142">System.Int64</span></span>

## <span data-ttu-id="57bef-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57bef-143">OUTPUTS</span></span>

### <span data-ttu-id="57bef-144">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="57bef-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="57bef-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57bef-145">NOTES</span></span>

## <span data-ttu-id="57bef-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57bef-146">RELATED LINKS</span></span>

[<span data-ttu-id="57bef-147">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="57bef-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


