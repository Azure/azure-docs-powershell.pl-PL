---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055956"
---
# <span data-ttu-id="7fa13-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="7fa13-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="7fa13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7fa13-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa13-103">Lista publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="7fa13-103">List of public IP addresses.</span></span>

## <span data-ttu-id="7fa13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7fa13-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="7fa13-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7fa13-105">DESCRIPTION</span></span>
<span data-ttu-id="7fa13-106">Lista publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="7fa13-106">List of public IP addresses.</span></span>

## <span data-ttu-id="7fa13-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7fa13-107">EXAMPLES</span></span>

### <span data-ttu-id="7fa13-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="7fa13-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="7fa13-109">Pobierz listę publicznych adresów IP, przydzielonych lub nieprzydzielonych.</span><span class="sxs-lookup"><span data-stu-id="7fa13-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="7fa13-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7fa13-110">PARAMETERS</span></span>

### <span data-ttu-id="7fa13-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="7fa13-111">-Filter</span></span>
<span data-ttu-id="7fa13-112">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="7fa13-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="7fa13-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="7fa13-113">-OrderBy</span></span>
<span data-ttu-id="7fa13-114">Parametr orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="7fa13-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="7fa13-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="7fa13-115">-Skip</span></span>
<span data-ttu-id="7fa13-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="7fa13-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7fa13-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="7fa13-117">-Top</span></span>
<span data-ttu-id="7fa13-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="7fa13-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7fa13-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="7fa13-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7fa13-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="7fa13-120">-InlineCount</span></span>
<span data-ttu-id="7fa13-121">Parametr liczby w tekście OData.</span><span class="sxs-lookup"><span data-stu-id="7fa13-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="7fa13-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa13-122">CommonParameters</span></span>
<span data-ttu-id="7fa13-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fa13-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa13-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fa13-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa13-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fa13-125">INPUTS</span></span>

## <span data-ttu-id="7fa13-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7fa13-126">OUTPUTS</span></span>

### <span data-ttu-id="7fa13-127">Microsoft. AzureStack. Management. Network. admin. models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7fa13-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="7fa13-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7fa13-128">NOTES</span></span>

## <span data-ttu-id="7fa13-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fa13-129">RELATED LINKS</span></span>
