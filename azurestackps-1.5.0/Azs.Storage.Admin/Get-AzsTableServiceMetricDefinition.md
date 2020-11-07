---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fac65e094352d399f5392b26a8ed314616125ba0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710779"
---
# <span data-ttu-id="a46aa-101">Get-AzsTableServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="a46aa-101">Get-AzsTableServiceMetricDefinition</span></span>

## <span data-ttu-id="a46aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a46aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a46aa-103">Zwraca listę definicji metryk dla usługi Table.</span><span class="sxs-lookup"><span data-stu-id="a46aa-103">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="a46aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a46aa-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a46aa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a46aa-105">DESCRIPTION</span></span>
<span data-ttu-id="a46aa-106">Zwraca listę definicji metryk dla usługi Table.</span><span class="sxs-lookup"><span data-stu-id="a46aa-106">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="a46aa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a46aa-107">EXAMPLES</span></span>

### <span data-ttu-id="a46aa-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a46aa-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="a46aa-109">Pobieranie listy definicji metryk dla usługi Table.</span><span class="sxs-lookup"><span data-stu-id="a46aa-109">Get the list of metric definitions for table service.</span></span>

## <span data-ttu-id="a46aa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a46aa-110">PARAMETERS</span></span>

### <span data-ttu-id="a46aa-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="a46aa-111">-FarmName</span></span>
<span data-ttu-id="a46aa-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="a46aa-112">Farm Id.</span></span>

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

### <span data-ttu-id="a46aa-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a46aa-113">-ResourceGroupName</span></span>
<span data-ttu-id="a46aa-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a46aa-114">Resource group name.</span></span>

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

### <span data-ttu-id="a46aa-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="a46aa-115">-Skip</span></span>
<span data-ttu-id="a46aa-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="a46aa-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a46aa-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="a46aa-117">-Top</span></span>
<span data-ttu-id="a46aa-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="a46aa-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a46aa-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="a46aa-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a46aa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46aa-120">CommonParameters</span></span>
<span data-ttu-id="a46aa-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a46aa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46aa-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a46aa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46aa-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a46aa-123">INPUTS</span></span>

## <span data-ttu-id="a46aa-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a46aa-124">OUTPUTS</span></span>

### <span data-ttu-id="a46aa-125">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="a46aa-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="a46aa-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a46aa-126">NOTES</span></span>

## <span data-ttu-id="a46aa-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a46aa-127">RELATED LINKS</span></span>

