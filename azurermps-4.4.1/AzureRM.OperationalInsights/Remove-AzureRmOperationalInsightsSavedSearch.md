---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 103012f25baa67cbd8faeab4a9cc0c22297e7922
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543108"
---
# <span data-ttu-id="6aaf1-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="6aaf1-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="6aaf1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aaf1-102">SYNOPSIS</span></span>
<span data-ttu-id="6aaf1-103">Umożliwia usunięcie zapisanego wyszukiwania z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aaf1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aaf1-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aaf1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6aaf1-105">DESCRIPTION</span></span>
<span data-ttu-id="6aaf1-106">Polecenie cmdlet **Remove-AzureRmOperationalInsightsSavedSearch** usuwa zapisane wyszukiwanie z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="6aaf1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aaf1-107">EXAMPLES</span></span>

### <span data-ttu-id="6aaf1-108">Przykład 1: Usuwanie zapisanego wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="6aaf1-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="6aaf1-109">To polecenie umożliwia usunięcie zapisanego wyszukiwania z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="6aaf1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aaf1-110">PARAMETERS</span></span>

### <span data-ttu-id="6aaf1-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aaf1-111">-ResourceGroupName</span></span>
<span data-ttu-id="6aaf1-112">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-112">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="6aaf1-113">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="6aaf1-113">-SavedSearchId</span></span>
<span data-ttu-id="6aaf1-114">Określa zapisany identyfikator wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-114">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="6aaf1-115">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="6aaf1-115">-WorkspaceName</span></span>
<span data-ttu-id="6aaf1-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="6aaf1-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6aaf1-117">-Confirm</span></span>
<span data-ttu-id="6aaf1-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aaf1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aaf1-119">-WhatIf</span></span>
<span data-ttu-id="6aaf1-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aaf1-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aaf1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aaf1-122">-DefaultProfile</span></span>
<span data-ttu-id="6aaf1-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aaf1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aaf1-124">CommonParameters</span></span>
<span data-ttu-id="6aaf1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aaf1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aaf1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aaf1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aaf1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aaf1-127">INPUTS</span></span>

## <span data-ttu-id="6aaf1-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aaf1-128">OUTPUTS</span></span>

## <span data-ttu-id="6aaf1-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aaf1-129">NOTES</span></span>

## <span data-ttu-id="6aaf1-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aaf1-130">RELATED LINKS</span></span>

[<span data-ttu-id="6aaf1-131">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="6aaf1-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


