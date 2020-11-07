---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c875b28f6518a836296fe1f5f19910d549b880c7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/22/2020
ms.locfileid: "93899451"
---
# <span data-ttu-id="3d57a-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="3d57a-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="3d57a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d57a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d57a-103">Zwraca listę produktów dostępnych do pobrania z witryny Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="3d57a-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="3d57a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d57a-104">SYNTAX</span></span>

### <span data-ttu-id="3d57a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3d57a-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d57a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3d57a-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="3d57a-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="3d57a-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3d57a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3d57a-108">DESCRIPTION</span></span>
<span data-ttu-id="3d57a-109">Zwraca listę produktów dostępnych do pobrania z witryny Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="3d57a-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="3d57a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d57a-110">EXAMPLES</span></span>

### <span data-ttu-id="3d57a-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="3d57a-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="3d57a-112">Uzyskaj listę produktów dostępnych do pobrania z witryny Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="3d57a-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="3d57a-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="3d57a-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="3d57a-114">Uzyskaj informacje o produkcie dostępne do pobrania z witryny Azure Marketplace według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3d57a-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="3d57a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d57a-115">PARAMETERS</span></span>

### <span data-ttu-id="3d57a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d57a-116">-Name</span></span>
<span data-ttu-id="3d57a-117">Nazwa produktu.</span><span class="sxs-lookup"><span data-stu-id="3d57a-117">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d57a-118">-Activationname</span><span class="sxs-lookup"><span data-stu-id="3d57a-118">-ActivationName</span></span>
<span data-ttu-id="3d57a-119">Nazwa aktywacji.</span><span class="sxs-lookup"><span data-stu-id="3d57a-119">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d57a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d57a-120">-ResourceGroupName</span></span>
<span data-ttu-id="3d57a-121">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="3d57a-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d57a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d57a-122">-ResourceId</span></span>
<span data-ttu-id="3d57a-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3d57a-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d57a-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="3d57a-124">-Skip</span></span>
<span data-ttu-id="3d57a-125">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="3d57a-125">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d57a-126">-Początek</span><span class="sxs-lookup"><span data-stu-id="3d57a-126">-Top</span></span>
<span data-ttu-id="3d57a-127">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="3d57a-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3d57a-128">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="3d57a-128">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d57a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d57a-129">CommonParameters</span></span>
<span data-ttu-id="3d57a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d57a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d57a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d57a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d57a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d57a-132">INPUTS</span></span>

## <span data-ttu-id="3d57a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d57a-133">OUTPUTS</span></span>

### <span data-ttu-id="3d57a-134">Microsoft. AzureStack. Management. AzureBridge. admin. models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="3d57a-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="3d57a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d57a-135">NOTES</span></span>

## <span data-ttu-id="3d57a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d57a-136">RELATED LINKS</span></span>
