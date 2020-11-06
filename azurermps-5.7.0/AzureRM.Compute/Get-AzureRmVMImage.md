---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526962"
---
# <span data-ttu-id="3717f-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3717f-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="3717f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3717f-102">SYNOPSIS</span></span>
<span data-ttu-id="3717f-103">Pobiera wszystkie wersje VMImage.</span><span class="sxs-lookup"><span data-stu-id="3717f-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3717f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3717f-104">SYNTAX</span></span>

### <span data-ttu-id="3717f-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="3717f-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### <span data-ttu-id="3717f-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="3717f-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## <span data-ttu-id="3717f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3717f-107">DESCRIPTION</span></span>
<span data-ttu-id="3717f-108">Polecenie cmdlet **Get-AzureRmVMImage** pobiera wszystkie wersje VMImage.</span><span class="sxs-lookup"><span data-stu-id="3717f-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="3717f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3717f-109">EXAMPLES</span></span>

### <span data-ttu-id="3717f-110">Przykład 1: pobieranie obiektów VMImage</span><span class="sxs-lookup"><span data-stu-id="3717f-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="3717f-111">To polecenie pobiera wszystkie wersje VMImage, które pasują do określonych wartości.</span><span class="sxs-lookup"><span data-stu-id="3717f-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="3717f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3717f-112">PARAMETERS</span></span>

### <span data-ttu-id="3717f-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="3717f-113">-FilterExpression</span></span>
<span data-ttu-id="3717f-114">Określa wyrażenie filtru.</span><span class="sxs-lookup"><span data-stu-id="3717f-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3717f-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3717f-115">-Location</span></span>
<span data-ttu-id="3717f-116">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="3717f-116">Specifies the location of a VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3717f-117">-Offer</span><span class="sxs-lookup"><span data-stu-id="3717f-117">-Offer</span></span>
<span data-ttu-id="3717f-118">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="3717f-118">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="3717f-119">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="3717f-119">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3717f-120">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3717f-120">-PublisherName</span></span>
<span data-ttu-id="3717f-121">Umożliwia określenie wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="3717f-121">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="3717f-122">Aby uzyskać wydawcę obrazu, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="3717f-122">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3717f-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="3717f-123">-Skus</span></span>
<span data-ttu-id="3717f-124">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="3717f-124">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="3717f-125">Aby uzyskać jednostkę SKU, użyj polecenia cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="3717f-125">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3717f-126">-Version</span><span class="sxs-lookup"><span data-stu-id="3717f-126">-Version</span></span>
<span data-ttu-id="3717f-127">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="3717f-127">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3717f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3717f-128">CommonParameters</span></span>
<span data-ttu-id="3717f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3717f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3717f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3717f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3717f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3717f-131">INPUTS</span></span>

### <span data-ttu-id="3717f-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3717f-132">None</span></span>
<span data-ttu-id="3717f-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3717f-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3717f-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3717f-134">OUTPUTS</span></span>

## <span data-ttu-id="3717f-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3717f-135">NOTES</span></span>

## <span data-ttu-id="3717f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3717f-136">RELATED LINKS</span></span>

[<span data-ttu-id="3717f-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="3717f-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="3717f-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3717f-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="3717f-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="3717f-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="3717f-140">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3717f-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


