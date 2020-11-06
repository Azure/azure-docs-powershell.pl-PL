---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 15b1316940c42534844245eaaf1aee3e450adc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526966"
---
# <span data-ttu-id="169ea-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="169ea-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="169ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="169ea-102">SYNOPSIS</span></span>
<span data-ttu-id="169ea-103">Pobiera typ rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="169ea-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="169ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="169ea-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="169ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="169ea-105">DESCRIPTION</span></span>
<span data-ttu-id="169ea-106">Polecenie cmdlet **Get-AzureRmVMExtensionImageType** Pobiera typ rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="169ea-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="169ea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="169ea-107">EXAMPLES</span></span>

### <span data-ttu-id="169ea-108">Przykład 1: uzyskiwanie typu obrazu rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="169ea-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="169ea-109">To polecenie pobiera typ obrazu rozszerzenia dla określonego wydawcy i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="169ea-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="169ea-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="169ea-110">PARAMETERS</span></span>

### <span data-ttu-id="169ea-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="169ea-111">-Location</span></span>
<span data-ttu-id="169ea-112">Określa lokalizację rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="169ea-112">Specifies the location of an extension.</span></span>
<span data-ttu-id="169ea-113">To polecenie cmdlet umożliwia pobieranie typu rozszerzenia w lokalizacji, w której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="169ea-113">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="169ea-114">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="169ea-114">-PublisherName</span></span>
<span data-ttu-id="169ea-115">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="169ea-115">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="169ea-116">Aby uzyskać wydawcę rozszerzenia, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="169ea-116">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="169ea-117">To polecenie cmdlet umożliwia pobieranie typu rozszerzenia od wydawcy, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="169ea-117">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="169ea-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169ea-118">CommonParameters</span></span>
<span data-ttu-id="169ea-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169ea-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169ea-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="169ea-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169ea-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="169ea-121">INPUTS</span></span>

### <span data-ttu-id="169ea-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="169ea-122">None</span></span>
<span data-ttu-id="169ea-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="169ea-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="169ea-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="169ea-124">OUTPUTS</span></span>

## <span data-ttu-id="169ea-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="169ea-125">NOTES</span></span>

## <span data-ttu-id="169ea-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="169ea-126">RELATED LINKS</span></span>

[<span data-ttu-id="169ea-127">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="169ea-127">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="169ea-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="169ea-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


