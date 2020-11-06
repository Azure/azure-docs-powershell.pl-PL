---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37569cc786109a3a86b0406eb0aa24e7d106ed53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523241"
---
# <span data-ttu-id="f5710-101">Get-AzsBlobServiceMetric</span><span class="sxs-lookup"><span data-stu-id="f5710-101">Get-AzsBlobServiceMetric</span></span>

## <span data-ttu-id="f5710-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5710-102">SYNOPSIS</span></span>
<span data-ttu-id="f5710-103">Zwraca listę metryk dla usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5710-103">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="f5710-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5710-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5710-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5710-105">DESCRIPTION</span></span>
<span data-ttu-id="f5710-106">Zwraca listę metryk dla usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5710-106">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="f5710-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5710-107">EXAMPLES</span></span>

### <span data-ttu-id="f5710-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f5710-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="f5710-109">Uzyskiwanie listy metryk dla usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5710-109">Get a list of metrics for blob service.</span></span>

## <span data-ttu-id="f5710-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5710-110">PARAMETERS</span></span>

### <span data-ttu-id="f5710-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="f5710-111">-FarmName</span></span>
<span data-ttu-id="f5710-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="f5710-112">Farm Id.</span></span>

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

### <span data-ttu-id="f5710-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5710-113">-ResourceGroupName</span></span>
<span data-ttu-id="f5710-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f5710-114">Resource group name.</span></span>

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

### <span data-ttu-id="f5710-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="f5710-115">-Skip</span></span>
<span data-ttu-id="f5710-116">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="f5710-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f5710-117">-Początek</span><span class="sxs-lookup"><span data-stu-id="f5710-117">-Top</span></span>
<span data-ttu-id="f5710-118">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="f5710-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f5710-119">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="f5710-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f5710-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5710-120">CommonParameters</span></span>
<span data-ttu-id="f5710-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5710-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5710-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5710-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5710-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5710-123">INPUTS</span></span>

## <span data-ttu-id="f5710-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5710-124">OUTPUTS</span></span>

### <span data-ttu-id="f5710-125">Microsoft. AzureStack. Management. Storage. admin. models. Metric</span><span class="sxs-lookup"><span data-stu-id="f5710-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="f5710-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5710-126">NOTES</span></span>

## <span data-ttu-id="f5710-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5710-127">RELATED LINKS</span></span>

