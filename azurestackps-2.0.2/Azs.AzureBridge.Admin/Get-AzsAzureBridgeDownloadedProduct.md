---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b7cc2211df4fd8b9d65c3e93483a485a10ae32
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/26/2020
ms.locfileid: "94061801"
---
# <span data-ttu-id="736b3-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="736b3-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="736b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="736b3-102">SYNOPSIS</span></span>
<span data-ttu-id="736b3-103">Zwraca listę produktów pobranych z usługi Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="736b3-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="736b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="736b3-104">SYNTAX</span></span>

### <span data-ttu-id="736b3-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="736b3-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="736b3-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="736b3-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="736b3-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="736b3-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="736b3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="736b3-108">DESCRIPTION</span></span>
<span data-ttu-id="736b3-109">Zwraca listę produktów pobranych z usługi Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="736b3-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="736b3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="736b3-110">EXAMPLES</span></span>

### <span data-ttu-id="736b3-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="736b3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="736b3-112">Uzyskiwanie listy pobranych produktów z usługi Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="736b3-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="736b3-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="736b3-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="736b3-114">Uzyskiwanie pobranego produktu Azure Bridge według nazwy</span><span class="sxs-lookup"><span data-stu-id="736b3-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="736b3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="736b3-115">PARAMETERS</span></span>

### <span data-ttu-id="736b3-116">-Activationname</span><span class="sxs-lookup"><span data-stu-id="736b3-116">-ActivationName</span></span>
<span data-ttu-id="736b3-117">Nazwa aktywacji.</span><span class="sxs-lookup"><span data-stu-id="736b3-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="736b3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="736b3-118">-Name</span></span>
<span data-ttu-id="736b3-119">Nazwa produktu.</span><span class="sxs-lookup"><span data-stu-id="736b3-119">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="736b3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="736b3-120">-ResourceGroupName</span></span>
<span data-ttu-id="736b3-121">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="736b3-121">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="736b3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="736b3-122">-ResourceId</span></span>
<span data-ttu-id="736b3-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="736b3-123">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="736b3-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="736b3-124">-Skip</span></span>
<span data-ttu-id="736b3-125">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="736b3-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="736b3-126">-Początek</span><span class="sxs-lookup"><span data-stu-id="736b3-126">-Top</span></span>
<span data-ttu-id="736b3-127">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="736b3-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="736b3-128">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="736b3-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="736b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="736b3-129">CommonParameters</span></span>
<span data-ttu-id="736b3-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="736b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="736b3-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="736b3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="736b3-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="736b3-132">INPUTS</span></span>

## <span data-ttu-id="736b3-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="736b3-133">OUTPUTS</span></span>

### <span data-ttu-id="736b3-134">Microsoft. AzureStack. Management. AzureBridge. admin. models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="736b3-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="736b3-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="736b3-135">NOTES</span></span>

## <span data-ttu-id="736b3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="736b3-136">RELATED LINKS</span></span>

