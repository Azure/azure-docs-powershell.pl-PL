---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3af374d6609a7063581e06aa8aa496e56a1fd45c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717059"
---
# <span data-ttu-id="81905-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="81905-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="81905-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81905-102">SYNOPSIS</span></span>
<span data-ttu-id="81905-103">Umożliwia zaktualizowanie zapisanego wyszukiwania, które już istnieje.</span><span class="sxs-lookup"><span data-stu-id="81905-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81905-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81905-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81905-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81905-105">DESCRIPTION</span></span>
<span data-ttu-id="81905-106">Polecenie cmdlet **Set-AzureRmOperationalInsightsSavedSearch** umożliwia zaktualizowanie zapisanego wyszukiwania, które już istnieje.</span><span class="sxs-lookup"><span data-stu-id="81905-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="81905-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81905-107">EXAMPLES</span></span>

### <span data-ttu-id="81905-108">Przykład 1. ustawia zapisane wyszukiwanie ze zaktualizowanymi właściwościami</span><span class="sxs-lookup"><span data-stu-id="81905-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="81905-109">To polecenie umożliwia ustawienie zapisanego wyszukiwania przy użyciu zaktualizowanych właściwości.</span><span class="sxs-lookup"><span data-stu-id="81905-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="81905-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81905-110">PARAMETERS</span></span>

### <span data-ttu-id="81905-111">-Category</span><span class="sxs-lookup"><span data-stu-id="81905-111">-Category</span></span>
<span data-ttu-id="81905-112">Określa nazwę kategorii.</span><span class="sxs-lookup"><span data-stu-id="81905-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="81905-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81905-113">-DefaultProfile</span></span>
<span data-ttu-id="81905-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="81905-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81905-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="81905-115">-DisplayName</span></span>
<span data-ttu-id="81905-116">Określa nazwę wyświetlaną.</span><span class="sxs-lookup"><span data-stu-id="81905-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="81905-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="81905-117">-ETag</span></span>
<span data-ttu-id="81905-118">Określa nazwę elementu ETag.</span><span class="sxs-lookup"><span data-stu-id="81905-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="81905-119">-Query</span><span class="sxs-lookup"><span data-stu-id="81905-119">-Query</span></span>
<span data-ttu-id="81905-120">Określa nazwę zapytania.</span><span class="sxs-lookup"><span data-stu-id="81905-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="81905-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81905-121">-ResourceGroupName</span></span>
<span data-ttu-id="81905-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81905-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="81905-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="81905-123">-SavedSearchId</span></span>
<span data-ttu-id="81905-124">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="81905-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="81905-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="81905-125">-Tag</span></span>
<span data-ttu-id="81905-126">Zapisane Tagi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="81905-126">The saved search tags.</span></span>

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

### <span data-ttu-id="81905-127">-Version</span><span class="sxs-lookup"><span data-stu-id="81905-127">-Version</span></span>
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

### <span data-ttu-id="81905-128">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="81905-128">-WorkspaceName</span></span>
<span data-ttu-id="81905-129">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="81905-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="81905-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81905-130">CommonParameters</span></span>
<span data-ttu-id="81905-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81905-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81905-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81905-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81905-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81905-133">INPUTS</span></span>

### <span data-ttu-id="81905-134">System. String</span><span class="sxs-lookup"><span data-stu-id="81905-134">System.String</span></span>

### <span data-ttu-id="81905-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="81905-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="81905-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="81905-136">System.Int64</span></span>

## <span data-ttu-id="81905-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81905-137">OUTPUTS</span></span>

### <span data-ttu-id="81905-138">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="81905-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="81905-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81905-139">NOTES</span></span>

## <span data-ttu-id="81905-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81905-140">RELATED LINKS</span></span>

[<span data-ttu-id="81905-141">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="81905-141">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


