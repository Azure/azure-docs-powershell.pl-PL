---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2776c768f49dabdea8483ff601f129e80bfc2dc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061521"
---
# <span data-ttu-id="2ae6f-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="2ae6f-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="2ae6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ae6f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae6f-103">Zwraca listę metryk dla usługi kolejkowania.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="2ae6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ae6f-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ae6f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ae6f-105">DESCRIPTION</span></span>
<span data-ttu-id="2ae6f-106">Zwraca listę metryk dla usługi kolejkowania.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="2ae6f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ae6f-107">EXAMPLES</span></span>

### <span data-ttu-id="2ae6f-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="2ae6f-108">EXAMPLE 1</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="2ae6f-109">Pobieranie listy metryk dla usługi kolejkowania.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="2ae6f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ae6f-110">PARAMETERS</span></span>

### <span data-ttu-id="2ae6f-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="2ae6f-111">-FarmName</span></span>
<span data-ttu-id="2ae6f-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-112">Farm Id.</span></span>

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

### <span data-ttu-id="2ae6f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ae6f-113">-ResourceGroupName</span></span>
<span data-ttu-id="2ae6f-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-114">Resource group name.</span></span>

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

### <span data-ttu-id="2ae6f-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="2ae6f-115">-Skip</span></span>
<span data-ttu-id="2ae6f-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2ae6f-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="2ae6f-117">-Top</span></span>
<span data-ttu-id="2ae6f-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2ae6f-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2ae6f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae6f-120">CommonParameters</span></span>
<span data-ttu-id="2ae6f-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae6f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ae6f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae6f-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ae6f-123">INPUTS</span></span>

## <span data-ttu-id="2ae6f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ae6f-124">OUTPUTS</span></span>

### <span data-ttu-id="2ae6f-125">Microsoft. AzureStack. Management. Storage. admin. models. Metric</span><span class="sxs-lookup"><span data-stu-id="2ae6f-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="2ae6f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ae6f-126">NOTES</span></span>

## <span data-ttu-id="2ae6f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ae6f-127">RELATED LINKS</span></span>
