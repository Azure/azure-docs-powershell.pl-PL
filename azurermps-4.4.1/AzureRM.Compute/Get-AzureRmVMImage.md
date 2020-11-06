---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 5588d320d63a298fab632ea55d7c3b6c2220db85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525694"
---
# <span data-ttu-id="1fab5-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1fab5-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="1fab5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fab5-102">SYNOPSIS</span></span>
<span data-ttu-id="1fab5-103">Pobiera wszystkie wersje VMImage.</span><span class="sxs-lookup"><span data-stu-id="1fab5-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fab5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fab5-104">SYNTAX</span></span>

### <span data-ttu-id="1fab5-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="1fab5-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fab5-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="1fab5-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fab5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1fab5-107">DESCRIPTION</span></span>
<span data-ttu-id="1fab5-108">Polecenie cmdlet **Get-AzureRmVMImage** pobiera wszystkie wersje VMImage.</span><span class="sxs-lookup"><span data-stu-id="1fab5-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="1fab5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fab5-109">EXAMPLES</span></span>

### <span data-ttu-id="1fab5-110">Przykład 1: pobieranie obiektów VMImage</span><span class="sxs-lookup"><span data-stu-id="1fab5-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="1fab5-111">To polecenie pobiera wszystkie wersje VMImage, które pasują do określonych wartości.</span><span class="sxs-lookup"><span data-stu-id="1fab5-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="1fab5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fab5-112">PARAMETERS</span></span>

### <span data-ttu-id="1fab5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fab5-113">-DefaultProfile</span></span>
<span data-ttu-id="1fab5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fab5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="1fab5-115">-FilterExpression</span></span>
<span data-ttu-id="1fab5-116">Określa wyrażenie filtru.</span><span class="sxs-lookup"><span data-stu-id="1fab5-116">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1fab5-117">-Location</span></span>
<span data-ttu-id="1fab5-118">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="1fab5-118">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-119">-Offer</span><span class="sxs-lookup"><span data-stu-id="1fab5-119">-Offer</span></span>
<span data-ttu-id="1fab5-120">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="1fab5-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="1fab5-121">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="1fab5-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="1fab5-122">-PublisherName</span></span>
<span data-ttu-id="1fab5-123">Umożliwia określenie wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="1fab5-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="1fab5-124">Aby uzyskać wydawcę obrazu, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="1fab5-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="1fab5-125">-Skus</span></span>
<span data-ttu-id="1fab5-126">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="1fab5-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="1fab5-127">Aby uzyskać jednostkę SKU, użyj polecenia cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="1fab5-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-128">-Version</span><span class="sxs-lookup"><span data-stu-id="1fab5-128">-Version</span></span>
<span data-ttu-id="1fab5-129">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="1fab5-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fab5-130">CommonParameters</span></span>
<span data-ttu-id="1fab5-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fab5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fab5-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fab5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fab5-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fab5-133">INPUTS</span></span>

## <span data-ttu-id="1fab5-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fab5-134">OUTPUTS</span></span>

## <span data-ttu-id="1fab5-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fab5-135">NOTES</span></span>

## <span data-ttu-id="1fab5-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fab5-136">RELATED LINKS</span></span>

[<span data-ttu-id="1fab5-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="1fab5-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="1fab5-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1fab5-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="1fab5-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="1fab5-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="1fab5-140">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1fab5-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


