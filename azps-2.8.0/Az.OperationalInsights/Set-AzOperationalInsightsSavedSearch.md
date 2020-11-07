---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 535fbe737184b996ee0caa030c83137ea8cd1019
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93897090"
---
# <span data-ttu-id="213a8-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="213a8-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="213a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="213a8-102">SYNOPSIS</span></span>
<span data-ttu-id="213a8-103">Umożliwia zaktualizowanie zapisanego wyszukiwania, które już istnieje.</span><span class="sxs-lookup"><span data-stu-id="213a8-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="213a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="213a8-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="213a8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="213a8-105">DESCRIPTION</span></span>
<span data-ttu-id="213a8-106">Polecenie cmdlet **Set-AzOperationalInsightsSavedSearch** umożliwia zaktualizowanie zapisanego wyszukiwania, które już istnieje.</span><span class="sxs-lookup"><span data-stu-id="213a8-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="213a8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="213a8-107">EXAMPLES</span></span>

### <span data-ttu-id="213a8-108">Przykład 1. ustawia zapisane wyszukiwanie ze zaktualizowanymi właściwościami</span><span class="sxs-lookup"><span data-stu-id="213a8-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="213a8-109">To polecenie umożliwia ustawienie zapisanego wyszukiwania przy użyciu zaktualizowanych właściwości.</span><span class="sxs-lookup"><span data-stu-id="213a8-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="213a8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="213a8-110">PARAMETERS</span></span>

### <span data-ttu-id="213a8-111">-Category</span><span class="sxs-lookup"><span data-stu-id="213a8-111">-Category</span></span>
<span data-ttu-id="213a8-112">Określa nazwę kategorii.</span><span class="sxs-lookup"><span data-stu-id="213a8-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="213a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213a8-113">-DefaultProfile</span></span>
<span data-ttu-id="213a8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="213a8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="213a8-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="213a8-115">-DisplayName</span></span>
<span data-ttu-id="213a8-116">Określa nazwę wyświetlaną.</span><span class="sxs-lookup"><span data-stu-id="213a8-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="213a8-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="213a8-117">-ETag</span></span>
<span data-ttu-id="213a8-118">Określa nazwę elementu ETag.</span><span class="sxs-lookup"><span data-stu-id="213a8-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="213a8-119">-Query</span><span class="sxs-lookup"><span data-stu-id="213a8-119">-Query</span></span>
<span data-ttu-id="213a8-120">Określa nazwę zapytania.</span><span class="sxs-lookup"><span data-stu-id="213a8-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="213a8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="213a8-121">-ResourceGroupName</span></span>
<span data-ttu-id="213a8-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="213a8-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="213a8-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="213a8-123">-SavedSearchId</span></span>
<span data-ttu-id="213a8-124">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="213a8-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="213a8-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="213a8-125">-Tag</span></span>
<span data-ttu-id="213a8-126">Zapisane Tagi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="213a8-126">The saved search tags.</span></span>

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

### <span data-ttu-id="213a8-127">-Version</span><span class="sxs-lookup"><span data-stu-id="213a8-127">-Version</span></span>
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

### <span data-ttu-id="213a8-128">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="213a8-128">-WorkspaceName</span></span>
<span data-ttu-id="213a8-129">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="213a8-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="213a8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213a8-130">CommonParameters</span></span>
<span data-ttu-id="213a8-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="213a8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213a8-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="213a8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213a8-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="213a8-133">INPUTS</span></span>

### <span data-ttu-id="213a8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="213a8-134">System.String</span></span>

### <span data-ttu-id="213a8-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="213a8-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="213a8-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="213a8-136">System.Int64</span></span>

## <span data-ttu-id="213a8-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="213a8-137">OUTPUTS</span></span>

### <span data-ttu-id="213a8-138">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="213a8-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="213a8-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="213a8-139">NOTES</span></span>

## <span data-ttu-id="213a8-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="213a8-140">RELATED LINKS</span></span>

[<span data-ttu-id="213a8-141">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="213a8-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


