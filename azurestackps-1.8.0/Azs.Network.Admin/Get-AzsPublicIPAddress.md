---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889301"
---
# <span data-ttu-id="b6be9-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b6be9-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="b6be9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6be9-102">SYNOPSIS</span></span>
<span data-ttu-id="b6be9-103">Lista publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b6be9-103">List of public IP addresses.</span></span>

## <span data-ttu-id="b6be9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6be9-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b6be9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6be9-105">DESCRIPTION</span></span>
<span data-ttu-id="b6be9-106">Lista publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b6be9-106">List of public IP addresses.</span></span>

## <span data-ttu-id="b6be9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6be9-107">EXAMPLES</span></span>

### <span data-ttu-id="b6be9-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="b6be9-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="b6be9-109">Pobierz listę publicznych adresów IP, przydzielonych lub nieprzydzielonych.</span><span class="sxs-lookup"><span data-stu-id="b6be9-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="b6be9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6be9-110">PARAMETERS</span></span>

### <span data-ttu-id="b6be9-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="b6be9-111">-Filter</span></span>
<span data-ttu-id="b6be9-112">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="b6be9-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="b6be9-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b6be9-113">-OrderBy</span></span>
<span data-ttu-id="b6be9-114">Parametr orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="b6be9-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="b6be9-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="b6be9-115">-Skip</span></span>
<span data-ttu-id="b6be9-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="b6be9-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b6be9-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="b6be9-117">-Top</span></span>
<span data-ttu-id="b6be9-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="b6be9-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b6be9-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="b6be9-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b6be9-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="b6be9-120">-InlineCount</span></span>
<span data-ttu-id="b6be9-121">Parametr liczby w tekście OData.</span><span class="sxs-lookup"><span data-stu-id="b6be9-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="b6be9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6be9-122">CommonParameters</span></span>
<span data-ttu-id="b6be9-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6be9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6be9-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6be9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6be9-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6be9-125">INPUTS</span></span>

## <span data-ttu-id="b6be9-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6be9-126">OUTPUTS</span></span>

### <span data-ttu-id="b6be9-127">Microsoft. AzureStack. Management. Network. admin. models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b6be9-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="b6be9-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6be9-128">NOTES</span></span>

## <span data-ttu-id="b6be9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6be9-129">RELATED LINKS</span></span>
