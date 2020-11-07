---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43691cfa3299fc0534ce2d44fd2a2f6ed1043d04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523897"
---
# <span data-ttu-id="c2293-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c2293-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="c2293-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2293-102">SYNOPSIS</span></span>
<span data-ttu-id="c2293-103">Zapoznaj się z listą wszystkich sieci wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="c2293-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="c2293-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2293-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c2293-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2293-105">DESCRIPTION</span></span>
<span data-ttu-id="c2293-106">Zapoznaj się z listą wszystkich sieci wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="c2293-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="c2293-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2293-107">EXAMPLES</span></span>

### <span data-ttu-id="c2293-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c2293-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="c2293-109">Zwraca listę sieci wirtualnych z sygnaturą stosową platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2293-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="c2293-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2293-110">PARAMETERS</span></span>

### <span data-ttu-id="c2293-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="c2293-111">-Filter</span></span>
<span data-ttu-id="c2293-112">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="c2293-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="c2293-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="c2293-113">-InlineCount</span></span>
<span data-ttu-id="c2293-114">Parametr liczby w tekście OData.</span><span class="sxs-lookup"><span data-stu-id="c2293-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="c2293-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c2293-115">-OrderBy</span></span>
<span data-ttu-id="c2293-116">Parametr orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="c2293-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="c2293-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="c2293-117">-Skip</span></span>
<span data-ttu-id="c2293-118">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c2293-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c2293-119">-Początek</span><span class="sxs-lookup"><span data-stu-id="c2293-119">-Top</span></span>
<span data-ttu-id="c2293-120">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c2293-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c2293-121">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="c2293-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c2293-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2293-122">CommonParameters</span></span>
<span data-ttu-id="c2293-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2293-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2293-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2293-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2293-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2293-125">INPUTS</span></span>

## <span data-ttu-id="c2293-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2293-126">OUTPUTS</span></span>

### <span data-ttu-id="c2293-127">Microsoft. AzureStack. Management. Network. admin. models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c2293-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="c2293-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2293-128">NOTES</span></span>

## <span data-ttu-id="c2293-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2293-129">RELATED LINKS</span></span>
