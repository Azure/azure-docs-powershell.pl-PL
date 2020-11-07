---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 7c4b59f97a6cd74da791f090b1c90be72f43a2c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718950"
---
# <span data-ttu-id="6d83e-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="6d83e-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="6d83e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d83e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d83e-103">Pobiera VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="6d83e-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d83e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d83e-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String> [<CommonParameters>]
```

## <span data-ttu-id="6d83e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d83e-105">DESCRIPTION</span></span>
<span data-ttu-id="6d83e-106">Polecenie cmdlet **Get-AzureRmVMImageSku** pobiera VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="6d83e-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="6d83e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d83e-107">EXAMPLES</span></span>

### <span data-ttu-id="6d83e-108">Przykład 1: Pobierz VMImage SKU</span><span class="sxs-lookup"><span data-stu-id="6d83e-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="6d83e-109">To polecenie pobiera jednostki SKU określonego wydawcy i oferty.</span><span class="sxs-lookup"><span data-stu-id="6d83e-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="6d83e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d83e-110">PARAMETERS</span></span>

### <span data-ttu-id="6d83e-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6d83e-111">-Location</span></span>
<span data-ttu-id="6d83e-112">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="6d83e-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="6d83e-113">-Offer</span><span class="sxs-lookup"><span data-stu-id="6d83e-113">-Offer</span></span>
<span data-ttu-id="6d83e-114">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="6d83e-114">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="6d83e-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6d83e-115">-PublisherName</span></span>
<span data-ttu-id="6d83e-116">Umożliwia określenie wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="6d83e-116">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="6d83e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d83e-117">CommonParameters</span></span>
<span data-ttu-id="6d83e-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d83e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d83e-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d83e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d83e-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d83e-120">INPUTS</span></span>

### <span data-ttu-id="6d83e-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6d83e-121">None</span></span>
<span data-ttu-id="6d83e-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6d83e-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d83e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d83e-123">OUTPUTS</span></span>

## <span data-ttu-id="6d83e-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d83e-124">NOTES</span></span>

## <span data-ttu-id="6d83e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d83e-125">RELATED LINKS</span></span>

[<span data-ttu-id="6d83e-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6d83e-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="6d83e-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="6d83e-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="6d83e-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6d83e-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="6d83e-129">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6d83e-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


