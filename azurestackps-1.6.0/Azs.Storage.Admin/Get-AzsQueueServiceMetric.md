---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac33f0feae7d54798753637f8f7898ab796f0939
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523201"
---
# <span data-ttu-id="49c65-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="49c65-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="49c65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49c65-102">SYNOPSIS</span></span>
<span data-ttu-id="49c65-103">Zwraca listę metryk dla usługi kolejkowania.</span><span class="sxs-lookup"><span data-stu-id="49c65-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="49c65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49c65-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="49c65-105">Opis</span><span class="sxs-lookup"><span data-stu-id="49c65-105">DESCRIPTION</span></span>
<span data-ttu-id="49c65-106">Zwraca listę metryk dla usługi kolejkowania.</span><span class="sxs-lookup"><span data-stu-id="49c65-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="49c65-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49c65-107">EXAMPLES</span></span>

### <span data-ttu-id="49c65-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="49c65-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="49c65-109">Pobieranie listy metryk dla usługi kolejkowania.</span><span class="sxs-lookup"><span data-stu-id="49c65-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="49c65-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49c65-110">PARAMETERS</span></span>

### <span data-ttu-id="49c65-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="49c65-111">-FarmName</span></span>
<span data-ttu-id="49c65-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="49c65-112">Farm Id.</span></span>

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

### <span data-ttu-id="49c65-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c65-113">-ResourceGroupName</span></span>
<span data-ttu-id="49c65-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="49c65-114">Resource group name.</span></span>

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

### <span data-ttu-id="49c65-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="49c65-115">-Skip</span></span>
<span data-ttu-id="49c65-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="49c65-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="49c65-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="49c65-117">-Top</span></span>
<span data-ttu-id="49c65-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="49c65-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="49c65-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="49c65-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="49c65-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c65-120">CommonParameters</span></span>
<span data-ttu-id="49c65-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c65-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c65-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49c65-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c65-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49c65-123">INPUTS</span></span>

## <span data-ttu-id="49c65-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49c65-124">OUTPUTS</span></span>

### <span data-ttu-id="49c65-125">Microsoft. AzureStack. Management. Storage. admin. models. Metric</span><span class="sxs-lookup"><span data-stu-id="49c65-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="49c65-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49c65-126">NOTES</span></span>

## <span data-ttu-id="49c65-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49c65-127">RELATED LINKS</span></span>
