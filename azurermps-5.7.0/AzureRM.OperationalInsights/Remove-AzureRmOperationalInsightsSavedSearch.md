---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: e66ca332d2fd59faa64e4360d00af714cfa28475
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525073"
---
# <span data-ttu-id="16173-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="16173-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="16173-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16173-102">SYNOPSIS</span></span>
<span data-ttu-id="16173-103">Umożliwia usunięcie zapisanego wyszukiwania z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="16173-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16173-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16173-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16173-105">Opis</span><span class="sxs-lookup"><span data-stu-id="16173-105">DESCRIPTION</span></span>
<span data-ttu-id="16173-106">Polecenie cmdlet **Remove-AzureRmOperationalInsightsSavedSearch** usuwa zapisane wyszukiwanie z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="16173-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="16173-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16173-107">EXAMPLES</span></span>

### <span data-ttu-id="16173-108">Przykład 1: Usuwanie zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="16173-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="16173-109">To polecenie umożliwia usunięcie zapisanego wyszukiwania z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="16173-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="16173-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16173-110">PARAMETERS</span></span>

### <span data-ttu-id="16173-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16173-111">-DefaultProfile</span></span>
<span data-ttu-id="16173-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="16173-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16173-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16173-113">-ResourceGroupName</span></span>
<span data-ttu-id="16173-114">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="16173-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="16173-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="16173-115">-SavedSearchId</span></span>
<span data-ttu-id="16173-116">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="16173-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="16173-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="16173-117">-WorkspaceName</span></span>
<span data-ttu-id="16173-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="16173-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="16173-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16173-119">-Confirm</span></span>
<span data-ttu-id="16173-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16173-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16173-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16173-121">-WhatIf</span></span>
<span data-ttu-id="16173-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16173-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16173-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="16173-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16173-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16173-124">CommonParameters</span></span>
<span data-ttu-id="16173-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16173-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16173-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16173-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16173-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16173-127">INPUTS</span></span>

### <span data-ttu-id="16173-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="16173-128">None</span></span>
<span data-ttu-id="16173-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="16173-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16173-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16173-130">OUTPUTS</span></span>

## <span data-ttu-id="16173-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16173-131">NOTES</span></span>

## <span data-ttu-id="16173-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16173-132">RELATED LINKS</span></span>

[<span data-ttu-id="16173-133">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="16173-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


