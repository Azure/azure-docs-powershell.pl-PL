---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4156bc414105d6d104e8315d83f92f0fb6e19ab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989745"
---
# <span data-ttu-id="1ed42-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="1ed42-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="1ed42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ed42-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed42-103">Aktualizuje źródło danych.</span><span class="sxs-lookup"><span data-stu-id="1ed42-103">Updates a data source.</span></span>

## <span data-ttu-id="1ed42-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1ed42-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ed42-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1ed42-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed42-106">Polecenie cmdlet **Set-AzOperationalInsightsDataSource** aktualizuje źródło danych.</span><span class="sxs-lookup"><span data-stu-id="1ed42-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="1ed42-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1ed42-107">EXAMPLES</span></span>

## <span data-ttu-id="1ed42-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ed42-108">PARAMETERS</span></span>

### <span data-ttu-id="1ed42-109">- DataSource</span><span class="sxs-lookup"><span data-stu-id="1ed42-109">-DataSource</span></span>
<span data-ttu-id="1ed42-110">Określa źródło danych, które będzie aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed42-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed42-111">-DefaultProfile</span></span>
<span data-ttu-id="1ed42-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1ed42-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ed42-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed42-113">CommonParameters</span></span>
<span data-ttu-id="1ed42-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ed42-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed42-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed42-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed42-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ed42-116">INPUTS</span></span>

### <span data-ttu-id="1ed42-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1ed42-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1ed42-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ed42-118">OUTPUTS</span></span>

### <span data-ttu-id="1ed42-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1ed42-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1ed42-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1ed42-120">NOTES</span></span>
* <span data-ttu-id="1ed42-121">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="1ed42-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="1ed42-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ed42-122">RELATED LINKS</span></span>

[<span data-ttu-id="1ed42-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="1ed42-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="1ed42-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="1ed42-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


