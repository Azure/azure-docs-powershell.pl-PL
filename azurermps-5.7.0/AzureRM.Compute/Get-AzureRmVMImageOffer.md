---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: ccdc7ee8a63c0a633caf162f8549fd1ba737ce8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553008"
---
# <span data-ttu-id="12b05-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="12b05-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="12b05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12b05-102">SYNOPSIS</span></span>
<span data-ttu-id="12b05-103">Pobiera typy ofert VMImage.</span><span class="sxs-lookup"><span data-stu-id="12b05-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12b05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12b05-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="12b05-105">Opis</span><span class="sxs-lookup"><span data-stu-id="12b05-105">DESCRIPTION</span></span>
<span data-ttu-id="12b05-106">Polecenie cmdlet **Get-AzureRmVMImageOffer** pobiera typy oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="12b05-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="12b05-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12b05-107">EXAMPLES</span></span>

### <span data-ttu-id="12b05-108">Przykład 1: Uzyskaj typy ofert dla wydawcy</span><span class="sxs-lookup"><span data-stu-id="12b05-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="12b05-109">To polecenie pobiera typy oferty dla określonego wydawcy w regionie centrali Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="12b05-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="12b05-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12b05-110">PARAMETERS</span></span>

### <span data-ttu-id="12b05-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="12b05-111">-Location</span></span>
<span data-ttu-id="12b05-112">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="12b05-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="12b05-113">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="12b05-113">-PublisherName</span></span>
<span data-ttu-id="12b05-114">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="12b05-114">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="12b05-115">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="12b05-115">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="12b05-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b05-116">CommonParameters</span></span>
<span data-ttu-id="12b05-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b05-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b05-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b05-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b05-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12b05-119">INPUTS</span></span>

### <span data-ttu-id="12b05-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="12b05-120">None</span></span>
<span data-ttu-id="12b05-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="12b05-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12b05-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12b05-122">OUTPUTS</span></span>

## <span data-ttu-id="12b05-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12b05-123">NOTES</span></span>

## <span data-ttu-id="12b05-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12b05-124">RELATED LINKS</span></span>

[<span data-ttu-id="12b05-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="12b05-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="12b05-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="12b05-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="12b05-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="12b05-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="12b05-128">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="12b05-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


