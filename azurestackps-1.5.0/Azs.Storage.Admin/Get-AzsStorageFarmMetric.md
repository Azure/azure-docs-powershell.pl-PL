---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95ea9afa5d3dce953f4e51e84d011886e4ba5688
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523305"
---
# <span data-ttu-id="8a0c3-101">Get-AzsStorageFarmMetric</span><span class="sxs-lookup"><span data-stu-id="8a0c3-101">Get-AzsStorageFarmMetric</span></span>

## <span data-ttu-id="8a0c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0c3-103">Zwraca listę metryk farmy magazynu.</span><span class="sxs-lookup"><span data-stu-id="8a0c3-103">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="8a0c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a0c3-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a0c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8a0c3-105">DESCRIPTION</span></span>
<span data-ttu-id="8a0c3-106">Zwraca listę metryk farmy magazynu.</span><span class="sxs-lookup"><span data-stu-id="8a0c3-106">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="8a0c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a0c3-107">EXAMPLES</span></span>

### <span data-ttu-id="8a0c3-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8a0c3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarmMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="8a0c3-109">Uzyskaj listę metryk farmy magazynu.</span><span class="sxs-lookup"><span data-stu-id="8a0c3-109">Get the list of storage farm metrics.</span></span>

## <span data-ttu-id="8a0c3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a0c3-110">PARAMETERS</span></span>

### <span data-ttu-id="8a0c3-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="8a0c3-111">-FarmName</span></span>
<span data-ttu-id="8a0c3-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="8a0c3-112">Farm Id.</span></span>

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

### <span data-ttu-id="8a0c3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a0c3-113">-ResourceGroupName</span></span>
<span data-ttu-id="8a0c3-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a0c3-114">Resource group name.</span></span>

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

### <span data-ttu-id="8a0c3-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="8a0c3-115">-Skip</span></span>
<span data-ttu-id="8a0c3-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="8a0c3-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8a0c3-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="8a0c3-117">-Top</span></span>
<span data-ttu-id="8a0c3-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="8a0c3-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8a0c3-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="8a0c3-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8a0c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0c3-120">CommonParameters</span></span>
<span data-ttu-id="8a0c3-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a0c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0c3-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a0c3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0c3-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a0c3-123">INPUTS</span></span>

## <span data-ttu-id="8a0c3-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a0c3-124">OUTPUTS</span></span>

### <span data-ttu-id="8a0c3-125">Microsoft. AzureStack. Management. Storage. admin. models. Metric</span><span class="sxs-lookup"><span data-stu-id="8a0c3-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="8a0c3-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a0c3-126">NOTES</span></span>

## <span data-ttu-id="8a0c3-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a0c3-127">RELATED LINKS</span></span>
