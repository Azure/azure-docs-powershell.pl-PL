---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: c69474929fa91b2e4ae1c7f4e50d5961a9322f66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898533"
---
# <span data-ttu-id="32875-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="32875-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="32875-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32875-102">SYNOPSIS</span></span>
<span data-ttu-id="32875-103">Pobiera wszystkie wersje VMImage.</span><span class="sxs-lookup"><span data-stu-id="32875-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32875-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32875-104">SYNTAX</span></span>

### <span data-ttu-id="32875-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="32875-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32875-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="32875-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32875-107">Opis</span><span class="sxs-lookup"><span data-stu-id="32875-107">DESCRIPTION</span></span>
<span data-ttu-id="32875-108">Polecenie cmdlet **Get-AzureRmVMImage** pobiera wszystkie wersje VMImage.</span><span class="sxs-lookup"><span data-stu-id="32875-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="32875-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32875-109">EXAMPLES</span></span>

### <span data-ttu-id="32875-110">Przykład 1: pobieranie obiektów VMImage</span><span class="sxs-lookup"><span data-stu-id="32875-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="32875-111">To polecenie pobiera wszystkie wersje VMImage, które pasują do określonych wartości.</span><span class="sxs-lookup"><span data-stu-id="32875-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="32875-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32875-112">PARAMETERS</span></span>

### <span data-ttu-id="32875-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32875-113">-DefaultProfile</span></span>
<span data-ttu-id="32875-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32875-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32875-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="32875-115">-FilterExpression</span></span>
<span data-ttu-id="32875-116">Określa wyrażenie filtru.</span><span class="sxs-lookup"><span data-stu-id="32875-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="32875-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="32875-117">-Location</span></span>
<span data-ttu-id="32875-118">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="32875-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="32875-119">-Offer</span><span class="sxs-lookup"><span data-stu-id="32875-119">-Offer</span></span>
<span data-ttu-id="32875-120">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="32875-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="32875-121">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="32875-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="32875-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="32875-122">-PublisherName</span></span>
<span data-ttu-id="32875-123">Umożliwia określenie wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="32875-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="32875-124">Aby uzyskać wydawcę obrazu, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="32875-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="32875-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="32875-125">-Skus</span></span>
<span data-ttu-id="32875-126">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="32875-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="32875-127">Aby uzyskać jednostkę SKU, użyj polecenia cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="32875-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="32875-128">-Version</span><span class="sxs-lookup"><span data-stu-id="32875-128">-Version</span></span>
<span data-ttu-id="32875-129">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="32875-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="32875-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32875-130">CommonParameters</span></span>
<span data-ttu-id="32875-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32875-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32875-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32875-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32875-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32875-133">INPUTS</span></span>

### <span data-ttu-id="32875-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="32875-134">None</span></span>
<span data-ttu-id="32875-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="32875-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="32875-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32875-136">OUTPUTS</span></span>

### <span data-ttu-id="32875-137">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="32875-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="32875-138">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="32875-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="32875-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32875-139">NOTES</span></span>

## <span data-ttu-id="32875-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32875-140">RELATED LINKS</span></span>

[<span data-ttu-id="32875-141">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="32875-141">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="32875-142">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="32875-142">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="32875-143">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="32875-143">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="32875-144">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="32875-144">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


