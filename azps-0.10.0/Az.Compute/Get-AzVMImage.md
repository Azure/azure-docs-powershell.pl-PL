---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 7b7a61c6d3043fcb4687d75ac49400b88361b81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893745"
---
# <span data-ttu-id="51658-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="51658-101">Get-AzVMImage</span></span>

## <span data-ttu-id="51658-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51658-102">SYNOPSIS</span></span>
<span data-ttu-id="51658-103">Pobiera wszystkie wersje VMImage.</span><span class="sxs-lookup"><span data-stu-id="51658-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="51658-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51658-104">SYNTAX</span></span>

### <span data-ttu-id="51658-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="51658-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51658-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="51658-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51658-107">Opis</span><span class="sxs-lookup"><span data-stu-id="51658-107">DESCRIPTION</span></span>
<span data-ttu-id="51658-108">Polecenie cmdlet **Get-AzVMImage** pobiera wszystkie wersje VMImage.</span><span class="sxs-lookup"><span data-stu-id="51658-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="51658-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51658-109">EXAMPLES</span></span>

### <span data-ttu-id="51658-110">Przykład 1: pobieranie obiektów VMImage</span><span class="sxs-lookup"><span data-stu-id="51658-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="51658-111">To polecenie pobiera wszystkie wersje VMImage, które pasują do określonych wartości.</span><span class="sxs-lookup"><span data-stu-id="51658-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="51658-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51658-112">PARAMETERS</span></span>

### <span data-ttu-id="51658-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51658-113">-DefaultProfile</span></span>
<span data-ttu-id="51658-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51658-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51658-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="51658-115">-FilterExpression</span></span>
<span data-ttu-id="51658-116">Określa wyrażenie filtru.</span><span class="sxs-lookup"><span data-stu-id="51658-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="51658-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="51658-117">-Location</span></span>
<span data-ttu-id="51658-118">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="51658-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="51658-119">-Offer</span><span class="sxs-lookup"><span data-stu-id="51658-119">-Offer</span></span>
<span data-ttu-id="51658-120">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="51658-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="51658-121">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="51658-121">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="51658-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="51658-122">-PublisherName</span></span>
<span data-ttu-id="51658-123">Umożliwia określenie wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="51658-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="51658-124">Aby uzyskać wydawcę obrazu, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="51658-124">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="51658-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="51658-125">-Skus</span></span>
<span data-ttu-id="51658-126">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="51658-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="51658-127">Aby uzyskać jednostkę SKU, użyj polecenia cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="51658-127">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="51658-128">-Version</span><span class="sxs-lookup"><span data-stu-id="51658-128">-Version</span></span>
<span data-ttu-id="51658-129">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="51658-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="51658-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51658-130">CommonParameters</span></span>
<span data-ttu-id="51658-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51658-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51658-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51658-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51658-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51658-133">INPUTS</span></span>

### <span data-ttu-id="51658-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="51658-134">None</span></span>
<span data-ttu-id="51658-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="51658-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51658-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51658-136">OUTPUTS</span></span>

### <span data-ttu-id="51658-137">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="51658-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="51658-138">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="51658-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="51658-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51658-139">NOTES</span></span>

## <span data-ttu-id="51658-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51658-140">RELATED LINKS</span></span>

[<span data-ttu-id="51658-141">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="51658-141">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="51658-142">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="51658-142">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="51658-143">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="51658-143">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="51658-144">Zapisz — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="51658-144">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


