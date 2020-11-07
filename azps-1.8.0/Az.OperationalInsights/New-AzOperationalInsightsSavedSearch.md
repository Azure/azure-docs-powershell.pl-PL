---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 5853447dfc91511782e99ebafae644e14b6649b3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710888"
---
# <span data-ttu-id="a4ef9-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a4ef9-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="a4ef9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ef9-103">Tworzy nowe zapisane wyszukiwanie przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="a4ef9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4ef9-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ef9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="a4ef9-106">Polecenie cmdlet **New-AzOperationalInsightsSavedSearch** tworzy nowe zapisane wyszukiwanie przy użyciu określonych parametrów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="a4ef9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="a4ef9-108">Przykład 1. Tworzenie nowego zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="a4ef9-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="a4ef9-109">To polecenie tworzy nowe zapisane wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="a4ef9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4ef9-110">PARAMETERS</span></span>

### <span data-ttu-id="a4ef9-111">-Category</span><span class="sxs-lookup"><span data-stu-id="a4ef9-111">-Category</span></span>
<span data-ttu-id="a4ef9-112">Określa nazwę kategorii.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="a4ef9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ef9-113">-DefaultProfile</span></span>
<span data-ttu-id="a4ef9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a4ef9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4ef9-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a4ef9-115">-DisplayName</span></span>
<span data-ttu-id="a4ef9-116">Określa zapisaną nazwę wyświetlaną wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="a4ef9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a4ef9-117">-Force</span></span>
<span data-ttu-id="a4ef9-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4ef9-119">-Query</span><span class="sxs-lookup"><span data-stu-id="a4ef9-119">-Query</span></span>
<span data-ttu-id="a4ef9-120">Określa nazwę zapytania.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="a4ef9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ef9-121">-ResourceGroupName</span></span>
<span data-ttu-id="a4ef9-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="a4ef9-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="a4ef9-123">-SavedSearchId</span></span>
<span data-ttu-id="a4ef9-124">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="a4ef9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4ef9-125">-Tag</span></span>
<span data-ttu-id="a4ef9-126">Zapisane Tagi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-126">The saved search tags.</span></span>

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

### <span data-ttu-id="a4ef9-127">-Version</span><span class="sxs-lookup"><span data-stu-id="a4ef9-127">-Version</span></span>
<span data-ttu-id="a4ef9-128">Określa wersję.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ef9-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="a4ef9-129">-WorkspaceName</span></span>
<span data-ttu-id="a4ef9-130">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="a4ef9-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4ef9-131">-Confirm</span></span>
<span data-ttu-id="a4ef9-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ef9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ef9-133">-WhatIf</span></span>
<span data-ttu-id="a4ef9-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ef9-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ef9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ef9-136">CommonParameters</span></span>
<span data-ttu-id="a4ef9-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ef9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ef9-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ef9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ef9-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4ef9-139">INPUTS</span></span>

### <span data-ttu-id="a4ef9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ef9-140">System.String</span></span>

### <span data-ttu-id="a4ef9-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a4ef9-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a4ef9-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="a4ef9-142">System.Int64</span></span>

## <span data-ttu-id="a4ef9-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4ef9-143">OUTPUTS</span></span>

### <span data-ttu-id="a4ef9-144">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="a4ef9-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="a4ef9-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4ef9-145">NOTES</span></span>

## <span data-ttu-id="a4ef9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4ef9-146">RELATED LINKS</span></span>

[<span data-ttu-id="a4ef9-147">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="a4ef9-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


