---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
ms.openlocfilehash: 8d2253e20e87a0e6a5d97f2dd0e405412f5a9282
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898995"
---
# <span data-ttu-id="96b1b-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="96b1b-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="96b1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="96b1b-103">Pobiera VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="96b1b-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96b1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96b1b-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96b1b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="96b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="96b1b-106">Polecenie cmdlet **Get-AzureRmVMImageSku** pobiera VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="96b1b-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="96b1b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96b1b-107">EXAMPLES</span></span>

### <span data-ttu-id="96b1b-108">Przykład 1: Pobierz VMImage SKU</span><span class="sxs-lookup"><span data-stu-id="96b1b-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="96b1b-109">To polecenie pobiera jednostki SKU określonego wydawcy i oferty.</span><span class="sxs-lookup"><span data-stu-id="96b1b-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="96b1b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96b1b-110">PARAMETERS</span></span>

### <span data-ttu-id="96b1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b1b-111">-DefaultProfile</span></span>
<span data-ttu-id="96b1b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96b1b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96b1b-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="96b1b-113">-Location</span></span>
<span data-ttu-id="96b1b-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="96b1b-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="96b1b-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="96b1b-115">-Offer</span></span>
<span data-ttu-id="96b1b-116">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="96b1b-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="96b1b-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="96b1b-117">-PublisherName</span></span>
<span data-ttu-id="96b1b-118">Umożliwia określenie wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="96b1b-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="96b1b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b1b-119">CommonParameters</span></span>
<span data-ttu-id="96b1b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96b1b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b1b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96b1b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b1b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96b1b-122">INPUTS</span></span>

### <span data-ttu-id="96b1b-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="96b1b-123">None</span></span>
<span data-ttu-id="96b1b-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="96b1b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96b1b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96b1b-125">OUTPUTS</span></span>

### <span data-ttu-id="96b1b-126">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="96b1b-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="96b1b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96b1b-127">NOTES</span></span>

## <span data-ttu-id="96b1b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96b1b-128">RELATED LINKS</span></span>

[<span data-ttu-id="96b1b-129">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="96b1b-129">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="96b1b-130">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="96b1b-130">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="96b1b-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="96b1b-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="96b1b-132">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="96b1b-132">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


