---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: f299d0f299eaef61ba3655e8ec221cc55f5ab578
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718949"
---
# <span data-ttu-id="86f7d-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="86f7d-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="86f7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="86f7d-103">Pobiera wydawców VMImage.</span><span class="sxs-lookup"><span data-stu-id="86f7d-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86f7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86f7d-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [<CommonParameters>]
```

## <span data-ttu-id="86f7d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="86f7d-106">Polecenie cmdlet **Get-AzureRmVMImagePublisher** pobiera wydawców VMImage.</span><span class="sxs-lookup"><span data-stu-id="86f7d-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="86f7d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86f7d-107">EXAMPLES</span></span>

### <span data-ttu-id="86f7d-108">Przykład 1: uzyskiwanie wydawców VMImage dla regionu</span><span class="sxs-lookup"><span data-stu-id="86f7d-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="86f7d-109">To polecenie umożliwia uzyskiwanie wydawców wystąpień VMImage dla centralnego regionu USA w ramach Twojego profilu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="86f7d-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="86f7d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86f7d-110">PARAMETERS</span></span>

### <span data-ttu-id="86f7d-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="86f7d-111">-Location</span></span>
<span data-ttu-id="86f7d-112">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="86f7d-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="86f7d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f7d-113">CommonParameters</span></span>
<span data-ttu-id="86f7d-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86f7d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f7d-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f7d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f7d-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86f7d-116">INPUTS</span></span>

### <span data-ttu-id="86f7d-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="86f7d-117">None</span></span>
<span data-ttu-id="86f7d-118">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="86f7d-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86f7d-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86f7d-119">OUTPUTS</span></span>

## <span data-ttu-id="86f7d-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86f7d-120">NOTES</span></span>

## <span data-ttu-id="86f7d-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86f7d-121">RELATED LINKS</span></span>

[<span data-ttu-id="86f7d-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="86f7d-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="86f7d-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="86f7d-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="86f7d-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="86f7d-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="86f7d-125">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="86f7d-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


