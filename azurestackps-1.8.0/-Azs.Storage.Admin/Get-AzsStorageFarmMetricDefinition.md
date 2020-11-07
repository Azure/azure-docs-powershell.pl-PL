---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 186b6ca94d6e53f4a40babad2a923406ecbc1248
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889369"
---
# <span data-ttu-id="dda50-101">Get-AzsStorageFarmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="dda50-101">Get-AzsStorageFarmMetricDefinition</span></span>

## <span data-ttu-id="dda50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dda50-102">SYNOPSIS</span></span>
<span data-ttu-id="dda50-103">Zwraca listę definicji metryk dla farmy magazynu.</span><span class="sxs-lookup"><span data-stu-id="dda50-103">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="dda50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dda50-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="dda50-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dda50-105">DESCRIPTION</span></span>
<span data-ttu-id="dda50-106">Zwraca listę definicji metryk dla farmy magazynu.</span><span class="sxs-lookup"><span data-stu-id="dda50-106">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="dda50-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dda50-107">EXAMPLES</span></span>

### <span data-ttu-id="dda50-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dda50-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarmMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="dda50-109">Pobierz listę definicji metryk dla farmy magazynów.</span><span class="sxs-lookup"><span data-stu-id="dda50-109">Get the list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="dda50-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dda50-110">PARAMETERS</span></span>

### <span data-ttu-id="dda50-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="dda50-111">-FarmName</span></span>
<span data-ttu-id="dda50-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="dda50-112">Farm Id.</span></span>

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

### <span data-ttu-id="dda50-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda50-113">-ResourceGroupName</span></span>
<span data-ttu-id="dda50-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dda50-114">Resource group name.</span></span>

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

### <span data-ttu-id="dda50-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="dda50-115">-Skip</span></span>
<span data-ttu-id="dda50-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="dda50-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="dda50-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="dda50-117">-Top</span></span>
<span data-ttu-id="dda50-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="dda50-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="dda50-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="dda50-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="dda50-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda50-120">CommonParameters</span></span>
<span data-ttu-id="dda50-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda50-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda50-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda50-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda50-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dda50-123">INPUTS</span></span>

## <span data-ttu-id="dda50-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dda50-124">OUTPUTS</span></span>

### <span data-ttu-id="dda50-125">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="dda50-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="dda50-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dda50-126">NOTES</span></span>

## <span data-ttu-id="dda50-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dda50-127">RELATED LINKS</span></span>

