---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 931c85b649393d33f03e778d0e34cf6644e4c2d7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061759"
---
# <span data-ttu-id="85148-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="85148-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="85148-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85148-102">SYNOPSIS</span></span>
<span data-ttu-id="85148-103">Umożliwia usunięcie zapisanego wyszukiwania z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="85148-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="85148-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85148-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85148-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85148-105">DESCRIPTION</span></span>
<span data-ttu-id="85148-106">Polecenie cmdlet **Remove-AzOperationalInsightsSavedSearch** usuwa zapisane wyszukiwanie z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="85148-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="85148-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85148-107">EXAMPLES</span></span>

### <span data-ttu-id="85148-108">Przykład 1: Usuwanie zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="85148-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="85148-109">To polecenie umożliwia usunięcie zapisanego wyszukiwania z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="85148-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="85148-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85148-110">PARAMETERS</span></span>

### <span data-ttu-id="85148-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85148-111">-DefaultProfile</span></span>
<span data-ttu-id="85148-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="85148-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85148-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85148-113">-ResourceGroupName</span></span>
<span data-ttu-id="85148-114">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="85148-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="85148-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="85148-115">-SavedSearchId</span></span>
<span data-ttu-id="85148-116">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="85148-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="85148-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="85148-117">-WorkspaceName</span></span>
<span data-ttu-id="85148-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="85148-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="85148-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85148-119">-Confirm</span></span>
<span data-ttu-id="85148-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85148-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85148-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85148-121">-WhatIf</span></span>
<span data-ttu-id="85148-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85148-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85148-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85148-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85148-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85148-124">CommonParameters</span></span>
<span data-ttu-id="85148-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85148-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85148-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85148-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85148-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85148-127">INPUTS</span></span>

### <span data-ttu-id="85148-128">System. String</span><span class="sxs-lookup"><span data-stu-id="85148-128">System.String</span></span>

## <span data-ttu-id="85148-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85148-129">OUTPUTS</span></span>

### <span data-ttu-id="85148-130">System. void</span><span class="sxs-lookup"><span data-stu-id="85148-130">System.Void</span></span>

## <span data-ttu-id="85148-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85148-131">NOTES</span></span>

## <span data-ttu-id="85148-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85148-132">RELATED LINKS</span></span>

[<span data-ttu-id="85148-133">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="85148-133">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


