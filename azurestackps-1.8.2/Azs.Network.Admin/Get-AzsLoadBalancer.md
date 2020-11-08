---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b280b9e99fa91c53371d2eff38d42003873951bb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055917"
---
# <span data-ttu-id="c53e7-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c53e7-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="c53e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c53e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c53e7-103">Zapoznaj się z listą wszystkich modułów równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c53e7-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="c53e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c53e7-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c53e7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c53e7-105">DESCRIPTION</span></span>
<span data-ttu-id="c53e7-106">Zapoznaj się z listą wszystkich modułów równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c53e7-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="c53e7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c53e7-107">EXAMPLES</span></span>

### <span data-ttu-id="c53e7-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="c53e7-108">EXAMPLE 1</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="c53e7-109">Zapoznaj się z listą wszystkich modułów równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c53e7-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="c53e7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c53e7-110">PARAMETERS</span></span>

### <span data-ttu-id="c53e7-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="c53e7-111">-Filter</span></span>
<span data-ttu-id="c53e7-112">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="c53e7-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53e7-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c53e7-113">-OrderBy</span></span>
<span data-ttu-id="c53e7-114">Parametr orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="c53e7-114">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53e7-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="c53e7-115">-Skip</span></span>
<span data-ttu-id="c53e7-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c53e7-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53e7-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="c53e7-117">-Top</span></span>
<span data-ttu-id="c53e7-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c53e7-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c53e7-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="c53e7-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53e7-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="c53e7-120">-InlineCount</span></span>
<span data-ttu-id="c53e7-121">Parametr liczby w tekście OData.</span><span class="sxs-lookup"><span data-stu-id="c53e7-121">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53e7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53e7-122">CommonParameters</span></span>
<span data-ttu-id="c53e7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c53e7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c53e7-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c53e7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53e7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c53e7-125">INPUTS</span></span>

## <span data-ttu-id="c53e7-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c53e7-126">OUTPUTS</span></span>

### <span data-ttu-id="c53e7-127">Microsoft. AzureStack. Management. Network. admin. models. modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c53e7-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="c53e7-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c53e7-128">NOTES</span></span>

## <span data-ttu-id="c53e7-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c53e7-129">RELATED LINKS</span></span>
