---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889878"
---
# <span data-ttu-id="45260-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="45260-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="45260-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45260-102">SYNOPSIS</span></span>
<span data-ttu-id="45260-103">Lista publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="45260-103">List of public IP addresses.</span></span>

## <span data-ttu-id="45260-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45260-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="45260-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45260-105">DESCRIPTION</span></span>
<span data-ttu-id="45260-106">Lista publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="45260-106">List of public IP addresses.</span></span>

## <span data-ttu-id="45260-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45260-107">EXAMPLES</span></span>

### <span data-ttu-id="45260-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="45260-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="45260-109">Pobierz listę publicznych adresów IP, przydzielonych lub nieprzydzielonych.</span><span class="sxs-lookup"><span data-stu-id="45260-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="45260-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45260-110">PARAMETERS</span></span>

### <span data-ttu-id="45260-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="45260-111">-Filter</span></span>
<span data-ttu-id="45260-112">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="45260-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="45260-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="45260-113">-OrderBy</span></span>
<span data-ttu-id="45260-114">Parametr orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="45260-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="45260-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="45260-115">-Skip</span></span>
<span data-ttu-id="45260-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="45260-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="45260-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="45260-117">-Top</span></span>
<span data-ttu-id="45260-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="45260-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="45260-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="45260-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="45260-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="45260-120">-InlineCount</span></span>
<span data-ttu-id="45260-121">Parametr liczby w tekście OData.</span><span class="sxs-lookup"><span data-stu-id="45260-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="45260-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45260-122">CommonParameters</span></span>
<span data-ttu-id="45260-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45260-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45260-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45260-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45260-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45260-125">INPUTS</span></span>

## <span data-ttu-id="45260-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45260-126">OUTPUTS</span></span>

### <span data-ttu-id="45260-127">Microsoft. AzureStack. Management. Network. admin. models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="45260-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="45260-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45260-128">NOTES</span></span>

## <span data-ttu-id="45260-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45260-129">RELATED LINKS</span></span>
