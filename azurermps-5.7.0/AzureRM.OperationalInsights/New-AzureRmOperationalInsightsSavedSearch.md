---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: c8ad9196cd0f89670de38f6c99550e397016661e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554097"
---
# <span data-ttu-id="4b20e-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="4b20e-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="4b20e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b20e-102">SYNOPSIS</span></span>
<span data-ttu-id="4b20e-103">Tworzy nowe zapisane wyszukiwanie przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="4b20e-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b20e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b20e-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b20e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4b20e-105">DESCRIPTION</span></span>
<span data-ttu-id="4b20e-106">Polecenie cmdlet **New-AzureRmOperationalInsightsSavedSearch** tworzy nowe zapisane wyszukiwanie przy użyciu określonych parametrów dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4b20e-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="4b20e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b20e-107">EXAMPLES</span></span>

### <span data-ttu-id="4b20e-108">Przykład 1. Tworzenie nowego zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="4b20e-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="4b20e-109">To polecenie tworzy nowe zapisane wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="4b20e-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="4b20e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b20e-110">PARAMETERS</span></span>

### <span data-ttu-id="4b20e-111">-Category</span><span class="sxs-lookup"><span data-stu-id="4b20e-111">-Category</span></span>
<span data-ttu-id="4b20e-112">Określa nazwę kategorii.</span><span class="sxs-lookup"><span data-stu-id="4b20e-112">Specifies the category name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b20e-113">-DefaultProfile</span></span>
<span data-ttu-id="4b20e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4b20e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4b20e-115">-DisplayName</span></span>
<span data-ttu-id="4b20e-116">Określa zapisaną nazwę wyświetlaną wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="4b20e-116">Specifies the saved search display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4b20e-117">-Force</span></span>
<span data-ttu-id="4b20e-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4b20e-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-119">-Query</span><span class="sxs-lookup"><span data-stu-id="4b20e-119">-Query</span></span>
<span data-ttu-id="4b20e-120">Określa nazwę zapytania.</span><span class="sxs-lookup"><span data-stu-id="4b20e-120">Specifies the query name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b20e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4b20e-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4b20e-122">Specifies the resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="4b20e-123">-SavedSearchId</span></span>
<span data-ttu-id="4b20e-124">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="4b20e-124">Specifies the saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b20e-125">-Tag</span></span>
<span data-ttu-id="4b20e-126">Zapisane Tagi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="4b20e-126">The saved search tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-127">-Version</span><span class="sxs-lookup"><span data-stu-id="4b20e-127">-Version</span></span>
<span data-ttu-id="4b20e-128">Określa wersję.</span><span class="sxs-lookup"><span data-stu-id="4b20e-128">Specifies the version.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="4b20e-129">-WorkspaceName</span></span>
<span data-ttu-id="4b20e-130">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4b20e-130">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4b20e-131">-Confirm</span></span>
<span data-ttu-id="4b20e-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b20e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b20e-133">-WhatIf</span></span>
<span data-ttu-id="4b20e-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b20e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b20e-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4b20e-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b20e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b20e-136">CommonParameters</span></span>
<span data-ttu-id="4b20e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b20e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b20e-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b20e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b20e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b20e-139">INPUTS</span></span>

### <span data-ttu-id="4b20e-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4b20e-140">None</span></span>
<span data-ttu-id="4b20e-141">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4b20e-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b20e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b20e-142">OUTPUTS</span></span>

## <span data-ttu-id="4b20e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b20e-143">NOTES</span></span>

## <span data-ttu-id="4b20e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b20e-144">RELATED LINKS</span></span>

[<span data-ttu-id="4b20e-145">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="4b20e-145">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


