---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: ebea93e7d59e0740aa21e909f35779857aacba01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527353"
---
# <span data-ttu-id="db45a-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="db45a-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="db45a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db45a-102">SYNOPSIS</span></span>
<span data-ttu-id="db45a-103">Umożliwia zaktualizowanie zapisanego wyszukiwania, które już istnieje.</span><span class="sxs-lookup"><span data-stu-id="db45a-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db45a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db45a-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db45a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db45a-105">DESCRIPTION</span></span>
<span data-ttu-id="db45a-106">Polecenie cmdlet **Set-AzureRmOperationalInsightsSavedSearch** umożliwia zaktualizowanie zapisanego wyszukiwania, które już istnieje.</span><span class="sxs-lookup"><span data-stu-id="db45a-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="db45a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db45a-107">EXAMPLES</span></span>

### <span data-ttu-id="db45a-108">Przykład 1. ustawia zapisane wyszukiwanie ze zaktualizowanymi właściwościami</span><span class="sxs-lookup"><span data-stu-id="db45a-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="db45a-109">To polecenie umożliwia ustawienie zapisanego wyszukiwania przy użyciu zaktualizowanych właściwości.</span><span class="sxs-lookup"><span data-stu-id="db45a-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="db45a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db45a-110">PARAMETERS</span></span>

### <span data-ttu-id="db45a-111">-Category</span><span class="sxs-lookup"><span data-stu-id="db45a-111">-Category</span></span>
<span data-ttu-id="db45a-112">Określa nazwę kategorii.</span><span class="sxs-lookup"><span data-stu-id="db45a-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="db45a-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db45a-113">-DisplayName</span></span>
<span data-ttu-id="db45a-114">Określa nazwę wyświetlaną.</span><span class="sxs-lookup"><span data-stu-id="db45a-114">Specifies the display name.</span></span>

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

### <span data-ttu-id="db45a-115">-ETag</span><span class="sxs-lookup"><span data-stu-id="db45a-115">-ETag</span></span>
<span data-ttu-id="db45a-116">Określa nazwę elementu ETag.</span><span class="sxs-lookup"><span data-stu-id="db45a-116">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="db45a-117">-Query</span><span class="sxs-lookup"><span data-stu-id="db45a-117">-Query</span></span>
<span data-ttu-id="db45a-118">Określa nazwę zapytania.</span><span class="sxs-lookup"><span data-stu-id="db45a-118">Specifies the query name.</span></span>

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

### <span data-ttu-id="db45a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db45a-119">-ResourceGroupName</span></span>
<span data-ttu-id="db45a-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="db45a-120">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="db45a-121">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="db45a-121">-SavedSearchId</span></span>
<span data-ttu-id="db45a-122">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="db45a-122">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="db45a-123">-Tagi</span><span class="sxs-lookup"><span data-stu-id="db45a-123">-Tags</span></span>
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

### <span data-ttu-id="db45a-124">-Version</span><span class="sxs-lookup"><span data-stu-id="db45a-124">-Version</span></span>
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

### <span data-ttu-id="db45a-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="db45a-125">-WorkspaceName</span></span>
<span data-ttu-id="db45a-126">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="db45a-126">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="db45a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db45a-127">-DefaultProfile</span></span>
<span data-ttu-id="db45a-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db45a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db45a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db45a-129">CommonParameters</span></span>
<span data-ttu-id="db45a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db45a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db45a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db45a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db45a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db45a-132">INPUTS</span></span>

## <span data-ttu-id="db45a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db45a-133">OUTPUTS</span></span>

## <span data-ttu-id="db45a-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db45a-134">NOTES</span></span>

## <span data-ttu-id="db45a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db45a-135">RELATED LINKS</span></span>

[<span data-ttu-id="db45a-136">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="db45a-136">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


