---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5d91226a4762c5f1429d8d05b48defd83b4e2df
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889993"
---
# <span data-ttu-id="f7aff-101">Get-AzsTableServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="f7aff-101">Get-AzsTableServiceMetricDefinition</span></span>

## <span data-ttu-id="f7aff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7aff-102">SYNOPSIS</span></span>
<span data-ttu-id="f7aff-103">Zwraca listę definicji metryk dla usługi Table.</span><span class="sxs-lookup"><span data-stu-id="f7aff-103">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="f7aff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7aff-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f7aff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7aff-105">DESCRIPTION</span></span>
<span data-ttu-id="f7aff-106">Zwraca listę definicji metryk dla usługi Table.</span><span class="sxs-lookup"><span data-stu-id="f7aff-106">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="f7aff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7aff-107">EXAMPLES</span></span>

### <span data-ttu-id="f7aff-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="f7aff-108">EXAMPLE 1</span></span>
```
Get-AzsTableServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="f7aff-109">Pobieranie listy definicji metryk dla usługi Table.</span><span class="sxs-lookup"><span data-stu-id="f7aff-109">Get the list of metric definitions for table service.</span></span>

## <span data-ttu-id="f7aff-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7aff-110">PARAMETERS</span></span>

### <span data-ttu-id="f7aff-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="f7aff-111">-FarmName</span></span>
<span data-ttu-id="f7aff-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="f7aff-112">Farm Id.</span></span>

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

### <span data-ttu-id="f7aff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7aff-113">-ResourceGroupName</span></span>
<span data-ttu-id="f7aff-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7aff-114">Resource group name.</span></span>

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

### <span data-ttu-id="f7aff-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="f7aff-115">-Skip</span></span>
<span data-ttu-id="f7aff-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="f7aff-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f7aff-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="f7aff-117">-Top</span></span>
<span data-ttu-id="f7aff-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="f7aff-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f7aff-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="f7aff-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f7aff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7aff-120">CommonParameters</span></span>
<span data-ttu-id="f7aff-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7aff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7aff-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7aff-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7aff-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7aff-123">INPUTS</span></span>

## <span data-ttu-id="f7aff-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7aff-124">OUTPUTS</span></span>

### <span data-ttu-id="f7aff-125">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="f7aff-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="f7aff-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7aff-126">NOTES</span></span>

## <span data-ttu-id="f7aff-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7aff-127">RELATED LINKS</span></span>
