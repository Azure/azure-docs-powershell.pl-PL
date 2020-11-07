---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 607da2e6478d72915497f1476e04ae11f9a69b9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872419"
---
# <span data-ttu-id="d0d97-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="d0d97-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="d0d97-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0d97-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d97-103">Umożliwia zaktualizowanie źródła danych.</span><span class="sxs-lookup"><span data-stu-id="d0d97-103">Updates a data source.</span></span>

## <span data-ttu-id="d0d97-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0d97-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0d97-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0d97-105">DESCRIPTION</span></span>
<span data-ttu-id="d0d97-106">Polecenie cmdlet **Set-AzOperationalInsightsDataSource** umożliwia zaktualizowanie źródła danych.</span><span class="sxs-lookup"><span data-stu-id="d0d97-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="d0d97-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0d97-107">EXAMPLES</span></span>

## <span data-ttu-id="d0d97-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0d97-108">PARAMETERS</span></span>

### <span data-ttu-id="d0d97-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="d0d97-109">-DataSource</span></span>
<span data-ttu-id="d0d97-110">Określa źródło danych, które jest aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0d97-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="d0d97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d97-111">-DefaultProfile</span></span>
<span data-ttu-id="d0d97-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d0d97-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0d97-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d97-113">CommonParameters</span></span>
<span data-ttu-id="d0d97-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0d97-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d97-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0d97-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d97-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0d97-116">INPUTS</span></span>

### <span data-ttu-id="d0d97-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d0d97-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d0d97-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0d97-118">OUTPUTS</span></span>

### <span data-ttu-id="d0d97-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d0d97-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d0d97-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0d97-120">NOTES</span></span>
* <span data-ttu-id="d0d97-121">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="d0d97-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d0d97-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0d97-122">RELATED LINKS</span></span>

[<span data-ttu-id="d0d97-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="d0d97-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="d0d97-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="d0d97-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


