---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 80c80cb38013701d3e58d6d6bf77f774e2d61548
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93890025"
---
# <span data-ttu-id="32d48-101">Get-AzsStorageShareMetric</span><span class="sxs-lookup"><span data-stu-id="32d48-101">Get-AzsStorageShareMetric</span></span>

## <span data-ttu-id="32d48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32d48-102">SYNOPSIS</span></span>
<span data-ttu-id="32d48-103">Zwraca listę metryk dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="32d48-103">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="32d48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32d48-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetric [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="32d48-105">Opis</span><span class="sxs-lookup"><span data-stu-id="32d48-105">DESCRIPTION</span></span>
<span data-ttu-id="32d48-106">Zwraca listę metryk dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="32d48-106">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="32d48-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32d48-107">EXAMPLES</span></span>

### <span data-ttu-id="32d48-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="32d48-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="32d48-109">Pobieranie listy metryk dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="32d48-109">Get the list of metrics for a storage share.</span></span>

## <span data-ttu-id="32d48-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32d48-110">PARAMETERS</span></span>

### <span data-ttu-id="32d48-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="32d48-111">-FarmName</span></span>
<span data-ttu-id="32d48-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="32d48-112">Farm Id.</span></span>

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

### <span data-ttu-id="32d48-113">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="32d48-113">-ShareName</span></span>
<span data-ttu-id="32d48-114">Nazwa udziału.</span><span class="sxs-lookup"><span data-stu-id="32d48-114">Share name.</span></span>

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

### <span data-ttu-id="32d48-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d48-115">-ResourceGroupName</span></span>
<span data-ttu-id="32d48-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="32d48-116">Resource group name.</span></span>

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

### <span data-ttu-id="32d48-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="32d48-117">-Skip</span></span>
<span data-ttu-id="32d48-118">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="32d48-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="32d48-119">-Początek</span><span class="sxs-lookup"><span data-stu-id="32d48-119">-Top</span></span>
<span data-ttu-id="32d48-120">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="32d48-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="32d48-121">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="32d48-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="32d48-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d48-122">CommonParameters</span></span>
<span data-ttu-id="32d48-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32d48-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d48-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32d48-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d48-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32d48-125">INPUTS</span></span>

## <span data-ttu-id="32d48-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32d48-126">OUTPUTS</span></span>

### <span data-ttu-id="32d48-127">Microsoft. AzureStack. Management. Storage. admin. models. Metric</span><span class="sxs-lookup"><span data-stu-id="32d48-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="32d48-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32d48-128">NOTES</span></span>

## <span data-ttu-id="32d48-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32d48-129">RELATED LINKS</span></span>
