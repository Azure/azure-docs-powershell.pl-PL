---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc0e931c97a60d35db48dbceb1446ff944ee689
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889765"
---
# <span data-ttu-id="b8cf0-101">Get-AzsStorageFarmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b8cf0-101">Get-AzsStorageFarmMetricDefinition</span></span>

## <span data-ttu-id="b8cf0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="b8cf0-103">Zwraca listę definicji metryk dla farmy magazynu.</span><span class="sxs-lookup"><span data-stu-id="b8cf0-103">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="b8cf0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8cf0-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b8cf0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8cf0-105">DESCRIPTION</span></span>
<span data-ttu-id="b8cf0-106">Zwraca listę definicji metryk dla farmy magazynu.</span><span class="sxs-lookup"><span data-stu-id="b8cf0-106">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="b8cf0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8cf0-107">EXAMPLES</span></span>

### <span data-ttu-id="b8cf0-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="b8cf0-108">EXAMPLE 1</span></span>
```
Get-AzsStorageFarmMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="b8cf0-109">Pobierz listę definicji metryk dla farmy magazynów.</span><span class="sxs-lookup"><span data-stu-id="b8cf0-109">Get the list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="b8cf0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8cf0-110">PARAMETERS</span></span>

### <span data-ttu-id="b8cf0-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="b8cf0-111">-FarmName</span></span>
<span data-ttu-id="b8cf0-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="b8cf0-112">Farm Id.</span></span>

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

### <span data-ttu-id="b8cf0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8cf0-113">-ResourceGroupName</span></span>
<span data-ttu-id="b8cf0-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8cf0-114">Resource group name.</span></span>

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

### <span data-ttu-id="b8cf0-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="b8cf0-115">-Skip</span></span>
<span data-ttu-id="b8cf0-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="b8cf0-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b8cf0-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="b8cf0-117">-Top</span></span>
<span data-ttu-id="b8cf0-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="b8cf0-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b8cf0-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="b8cf0-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b8cf0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8cf0-120">CommonParameters</span></span>
<span data-ttu-id="b8cf0-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8cf0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8cf0-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8cf0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8cf0-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8cf0-123">INPUTS</span></span>

## <span data-ttu-id="b8cf0-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8cf0-124">OUTPUTS</span></span>

### <span data-ttu-id="b8cf0-125">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b8cf0-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="b8cf0-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8cf0-126">NOTES</span></span>

## <span data-ttu-id="b8cf0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8cf0-127">RELATED LINKS</span></span>
