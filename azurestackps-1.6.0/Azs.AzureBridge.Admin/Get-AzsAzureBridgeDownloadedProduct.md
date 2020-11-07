---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a9faaa3495e61186cab9d97d04e4d4b8186f152
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/22/2020
ms.locfileid: "93554437"
---
# <span data-ttu-id="c2a99-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="c2a99-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="c2a99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2a99-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a99-103">Zwraca listę produktów pobranych z usługi Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="c2a99-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="c2a99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2a99-104">SYNTAX</span></span>

### <span data-ttu-id="c2a99-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c2a99-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c2a99-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c2a99-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="c2a99-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c2a99-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c2a99-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c2a99-108">DESCRIPTION</span></span>
<span data-ttu-id="c2a99-109">Zwraca listę produktów pobranych z usługi Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="c2a99-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="c2a99-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2a99-110">EXAMPLES</span></span>

### <span data-ttu-id="c2a99-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c2a99-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="c2a99-112">Uzyskiwanie listy pobranych produktów z usługi Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="c2a99-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="c2a99-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c2a99-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="c2a99-114">Uzyskiwanie pobranego produktu Azure Bridge według nazwy</span><span class="sxs-lookup"><span data-stu-id="c2a99-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="c2a99-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2a99-115">PARAMETERS</span></span>

### <span data-ttu-id="c2a99-116">-Activationname</span><span class="sxs-lookup"><span data-stu-id="c2a99-116">-ActivationName</span></span>
<span data-ttu-id="c2a99-117">Nazwa aktywacji.</span><span class="sxs-lookup"><span data-stu-id="c2a99-117">Name of the activation.</span></span>

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

### <span data-ttu-id="c2a99-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2a99-118">-Name</span></span>
<span data-ttu-id="c2a99-119">Nazwa produktu.</span><span class="sxs-lookup"><span data-stu-id="c2a99-119">Name of the product.</span></span>

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

### <span data-ttu-id="c2a99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2a99-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2a99-121">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="c2a99-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c2a99-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2a99-122">-ResourceId</span></span>
<span data-ttu-id="c2a99-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c2a99-123">The resource id.</span></span>

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

### <span data-ttu-id="c2a99-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="c2a99-124">-Skip</span></span>
<span data-ttu-id="c2a99-125">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c2a99-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c2a99-126">-Początek</span><span class="sxs-lookup"><span data-stu-id="c2a99-126">-Top</span></span>
<span data-ttu-id="c2a99-127">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="c2a99-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c2a99-128">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="c2a99-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c2a99-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a99-129">CommonParameters</span></span>
<span data-ttu-id="c2a99-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a99-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a99-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2a99-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a99-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2a99-132">INPUTS</span></span>

## <span data-ttu-id="c2a99-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2a99-133">OUTPUTS</span></span>

### <span data-ttu-id="c2a99-134">Microsoft. AzureStack. Management. AzureBridge. admin. models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="c2a99-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="c2a99-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2a99-135">NOTES</span></span>

## <span data-ttu-id="c2a99-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2a99-136">RELATED LINKS</span></span>

