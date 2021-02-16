---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: f9bf63a65642e62e7f0416f0f053ef62277fa9bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184067"
---
# <span data-ttu-id="5f046-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="5f046-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="5f046-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f046-102">SYNOPSIS</span></span>
<span data-ttu-id="5f046-103">Umożliwia usunięcie zapisanego wyszukiwania z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5f046-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="5f046-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f046-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f046-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f046-105">DESCRIPTION</span></span>
<span data-ttu-id="5f046-106">Polecenie **cmdlet Remove-AzOperationalInsightsSavedSearch** usuwa zapisane wyszukiwanie z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5f046-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="5f046-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f046-107">EXAMPLES</span></span>

### <span data-ttu-id="5f046-108">Przykład 1. Usuwanie zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="5f046-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="5f046-109">To polecenie usuwa zapisane wyszukiwanie z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5f046-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="5f046-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f046-110">PARAMETERS</span></span>

### <span data-ttu-id="5f046-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f046-111">-DefaultProfile</span></span>
<span data-ttu-id="5f046-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5f046-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f046-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f046-113">-ResourceGroupName</span></span>
<span data-ttu-id="5f046-114">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5f046-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="5f046-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="5f046-115">-SavedSearchId</span></span>
<span data-ttu-id="5f046-116">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="5f046-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="5f046-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5f046-117">-WorkspaceName</span></span>
<span data-ttu-id="5f046-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5f046-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="5f046-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f046-119">-Confirm</span></span>
<span data-ttu-id="5f046-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5f046-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f046-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f046-121">-WhatIf</span></span>
<span data-ttu-id="5f046-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f046-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f046-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5f046-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f046-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f046-124">CommonParameters</span></span>
<span data-ttu-id="5f046-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f046-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f046-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f046-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f046-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f046-127">INPUTS</span></span>

### <span data-ttu-id="5f046-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5f046-128">System.String</span></span>

## <span data-ttu-id="5f046-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f046-129">OUTPUTS</span></span>

### <span data-ttu-id="5f046-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="5f046-130">System.Void</span></span>

## <span data-ttu-id="5f046-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f046-131">NOTES</span></span>

## <span data-ttu-id="5f046-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f046-132">RELATED LINKS</span></span>

[<span data-ttu-id="5f046-133">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="5f046-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


