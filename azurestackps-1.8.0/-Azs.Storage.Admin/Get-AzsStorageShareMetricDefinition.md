---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 646ee96dec361ac6318b4cfe48b80ec4c3686321
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889353"
---
# <span data-ttu-id="ce71e-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="ce71e-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="ce71e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce71e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce71e-103">Zwraca listę definicji metryk dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce71e-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="ce71e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce71e-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-Name] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ce71e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ce71e-105">DESCRIPTION</span></span>
<span data-ttu-id="ce71e-106">Zwraca listę definicji metryk dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce71e-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="ce71e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce71e-107">EXAMPLES</span></span>

### <span data-ttu-id="ce71e-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ce71e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Name "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="ce71e-109">Pobierz listę definicji metryk dla udziału magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce71e-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="ce71e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce71e-110">PARAMETERS</span></span>

### <span data-ttu-id="ce71e-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="ce71e-111">-FarmName</span></span>
<span data-ttu-id="ce71e-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="ce71e-112">Farm Id.</span></span>

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

### <span data-ttu-id="ce71e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce71e-113">-Name</span></span>
<span data-ttu-id="ce71e-114">Nazwa udziału.</span><span class="sxs-lookup"><span data-stu-id="ce71e-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce71e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce71e-115">-ResourceGroupName</span></span>
<span data-ttu-id="ce71e-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ce71e-116">Resource group name.</span></span>

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

### <span data-ttu-id="ce71e-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="ce71e-117">-Skip</span></span>
<span data-ttu-id="ce71e-118">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="ce71e-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ce71e-119">-Początek</span><span class="sxs-lookup"><span data-stu-id="ce71e-119">-Top</span></span>
<span data-ttu-id="ce71e-120">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="ce71e-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ce71e-121">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="ce71e-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ce71e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce71e-122">CommonParameters</span></span>
<span data-ttu-id="ce71e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce71e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce71e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce71e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce71e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce71e-125">INPUTS</span></span>

## <span data-ttu-id="ce71e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce71e-126">OUTPUTS</span></span>

### <span data-ttu-id="ce71e-127">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="ce71e-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="ce71e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce71e-128">NOTES</span></span>

## <span data-ttu-id="ce71e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce71e-129">RELATED LINKS</span></span>

