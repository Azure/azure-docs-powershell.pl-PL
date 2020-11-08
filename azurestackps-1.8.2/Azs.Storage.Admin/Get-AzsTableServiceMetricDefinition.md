---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5d91226a4762c5f1429d8d05b48defd83b4e2df
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055800"
---
# <span data-ttu-id="ece1b-101">Get-AzsTableServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="ece1b-101">Get-AzsTableServiceMetricDefinition</span></span>

## <span data-ttu-id="ece1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ece1b-102">SYNOPSIS</span></span>
<span data-ttu-id="ece1b-103">Zwraca listę definicji metryk dla usługi Table.</span><span class="sxs-lookup"><span data-stu-id="ece1b-103">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="ece1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ece1b-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ece1b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ece1b-105">DESCRIPTION</span></span>
<span data-ttu-id="ece1b-106">Zwraca listę definicji metryk dla usługi Table.</span><span class="sxs-lookup"><span data-stu-id="ece1b-106">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="ece1b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ece1b-107">EXAMPLES</span></span>

### <span data-ttu-id="ece1b-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="ece1b-108">EXAMPLE 1</span></span>
```
Get-AzsTableServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="ece1b-109">Pobieranie listy definicji metryk dla usługi Table.</span><span class="sxs-lookup"><span data-stu-id="ece1b-109">Get the list of metric definitions for table service.</span></span>

## <span data-ttu-id="ece1b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ece1b-110">PARAMETERS</span></span>

### <span data-ttu-id="ece1b-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="ece1b-111">-FarmName</span></span>
<span data-ttu-id="ece1b-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="ece1b-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece1b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece1b-113">-ResourceGroupName</span></span>
<span data-ttu-id="ece1b-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ece1b-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece1b-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="ece1b-115">-Skip</span></span>
<span data-ttu-id="ece1b-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="ece1b-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece1b-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="ece1b-117">-Top</span></span>
<span data-ttu-id="ece1b-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="ece1b-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ece1b-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="ece1b-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece1b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece1b-120">CommonParameters</span></span>
<span data-ttu-id="ece1b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece1b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece1b-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece1b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece1b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ece1b-123">INPUTS</span></span>

## <span data-ttu-id="ece1b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ece1b-124">OUTPUTS</span></span>

### <span data-ttu-id="ece1b-125">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="ece1b-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="ece1b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ece1b-126">NOTES</span></span>

## <span data-ttu-id="ece1b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ece1b-127">RELATED LINKS</span></span>
