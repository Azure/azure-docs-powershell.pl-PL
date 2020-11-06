---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3996096b692a7e242fc6cf42288508bdc4625cd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523898"
---
# <span data-ttu-id="5e0e8-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="5e0e8-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="5e0e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0e8-103">Lista publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-103">List of public IP addresses.</span></span>

## <span data-ttu-id="5e0e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e0e8-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="5e0e8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e0e8-105">DESCRIPTION</span></span>
<span data-ttu-id="5e0e8-106">Lista publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-106">List of public IP addresses.</span></span>

## <span data-ttu-id="5e0e8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e0e8-107">EXAMPLES</span></span>

### <span data-ttu-id="5e0e8-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e0e8-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="5e0e8-109">Pobierz listę publicznych adresów IP, przydzielonych lub nieprzydzielonych.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="5e0e8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e0e8-110">PARAMETERS</span></span>

### <span data-ttu-id="5e0e8-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="5e0e8-111">-Filter</span></span>
<span data-ttu-id="5e0e8-112">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="5e0e8-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="5e0e8-113">-InlineCount</span></span>
<span data-ttu-id="5e0e8-114">Parametr liczby w tekście OData.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="5e0e8-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="5e0e8-115">-OrderBy</span></span>
<span data-ttu-id="5e0e8-116">Parametr orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="5e0e8-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="5e0e8-117">-Skip</span></span>
<span data-ttu-id="5e0e8-118">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5e0e8-119">-Początek</span><span class="sxs-lookup"><span data-stu-id="5e0e8-119">-Top</span></span>
<span data-ttu-id="5e0e8-120">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5e0e8-121">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5e0e8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0e8-122">CommonParameters</span></span>
<span data-ttu-id="5e0e8-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0e8-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e0e8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0e8-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e0e8-125">INPUTS</span></span>

## <span data-ttu-id="5e0e8-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e0e8-126">OUTPUTS</span></span>

### <span data-ttu-id="5e0e8-127">Microsoft. AzureStack. Management. Network. admin. models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5e0e8-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="5e0e8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e0e8-128">NOTES</span></span>

## <span data-ttu-id="5e0e8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e0e8-129">RELATED LINKS</span></span>

