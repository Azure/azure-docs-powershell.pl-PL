---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 80c80cb38013701d3e58d6d6bf77f774e2d61548
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055582"
---
# <span data-ttu-id="98a97-101">Get-AzsStorageShareMetric</span><span class="sxs-lookup"><span data-stu-id="98a97-101">Get-AzsStorageShareMetric</span></span>

## <span data-ttu-id="98a97-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98a97-102">SYNOPSIS</span></span>
<span data-ttu-id="98a97-103">Zwraca listę metryk dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="98a97-103">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="98a97-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98a97-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetric [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="98a97-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98a97-105">DESCRIPTION</span></span>
<span data-ttu-id="98a97-106">Zwraca listę metryk dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="98a97-106">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="98a97-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98a97-107">EXAMPLES</span></span>

### <span data-ttu-id="98a97-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="98a97-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="98a97-109">Pobieranie listy metryk dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="98a97-109">Get the list of metrics for a storage share.</span></span>

## <span data-ttu-id="98a97-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98a97-110">PARAMETERS</span></span>

### <span data-ttu-id="98a97-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="98a97-111">-FarmName</span></span>
<span data-ttu-id="98a97-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="98a97-112">Farm Id.</span></span>

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

### <span data-ttu-id="98a97-113">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="98a97-113">-ShareName</span></span>
<span data-ttu-id="98a97-114">Nazwa udziału.</span><span class="sxs-lookup"><span data-stu-id="98a97-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a97-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a97-115">-ResourceGroupName</span></span>
<span data-ttu-id="98a97-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="98a97-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a97-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="98a97-117">-Skip</span></span>
<span data-ttu-id="98a97-118">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="98a97-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="98a97-119">-Początek</span><span class="sxs-lookup"><span data-stu-id="98a97-119">-Top</span></span>
<span data-ttu-id="98a97-120">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="98a97-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="98a97-121">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="98a97-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a97-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a97-122">CommonParameters</span></span>
<span data-ttu-id="98a97-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98a97-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a97-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a97-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a97-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98a97-125">INPUTS</span></span>

## <span data-ttu-id="98a97-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98a97-126">OUTPUTS</span></span>

### <span data-ttu-id="98a97-127">Microsoft. AzureStack. Management. Storage. admin. models. Metric</span><span class="sxs-lookup"><span data-stu-id="98a97-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="98a97-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98a97-128">NOTES</span></span>

## <span data-ttu-id="98a97-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98a97-129">RELATED LINKS</span></span>
