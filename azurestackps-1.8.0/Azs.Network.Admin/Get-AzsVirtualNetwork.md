---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af35419f3e0b28be9782e7bbe5d4eaaf1cdf0807
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889298"
---
# <span data-ttu-id="43ccf-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="43ccf-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="43ccf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="43ccf-103">Zapoznaj się z listą wszystkich sieci wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="43ccf-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="43ccf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43ccf-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="43ccf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43ccf-105">DESCRIPTION</span></span>
<span data-ttu-id="43ccf-106">Zapoznaj się z listą wszystkich sieci wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="43ccf-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="43ccf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43ccf-107">EXAMPLES</span></span>

### <span data-ttu-id="43ccf-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="43ccf-108">EXAMPLE 1</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="43ccf-109">Zwraca listę sieci wirtualnych z sygnaturą stosową platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43ccf-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="43ccf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43ccf-110">PARAMETERS</span></span>

### <span data-ttu-id="43ccf-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="43ccf-111">-Filter</span></span>
<span data-ttu-id="43ccf-112">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="43ccf-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="43ccf-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="43ccf-113">-OrderBy</span></span>
<span data-ttu-id="43ccf-114">Parametr orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="43ccf-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="43ccf-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="43ccf-115">-Skip</span></span>
<span data-ttu-id="43ccf-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="43ccf-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="43ccf-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="43ccf-117">-Top</span></span>
<span data-ttu-id="43ccf-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="43ccf-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="43ccf-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="43ccf-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="43ccf-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="43ccf-120">-InlineCount</span></span>
<span data-ttu-id="43ccf-121">Parametr liczby w tekście OData.</span><span class="sxs-lookup"><span data-stu-id="43ccf-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="43ccf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ccf-122">CommonParameters</span></span>
<span data-ttu-id="43ccf-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ccf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ccf-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ccf-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ccf-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43ccf-125">INPUTS</span></span>

## <span data-ttu-id="43ccf-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43ccf-126">OUTPUTS</span></span>

### <span data-ttu-id="43ccf-127">Microsoft. AzureStack. Management. Network. admin. models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="43ccf-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="43ccf-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43ccf-128">NOTES</span></span>

## <span data-ttu-id="43ccf-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43ccf-129">RELATED LINKS</span></span>
