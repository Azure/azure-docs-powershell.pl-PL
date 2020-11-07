---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5bdce17c963cc2529fab3f328b9ab64cc549e1d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719667"
---
# <span data-ttu-id="7cee7-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7cee7-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="7cee7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7cee7-102">SYNOPSIS</span></span>
<span data-ttu-id="7cee7-103">Pobiera VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="7cee7-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cee7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7cee7-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cee7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7cee7-105">DESCRIPTION</span></span>
<span data-ttu-id="7cee7-106">Polecenie cmdlet **Get-AzureRmVMImageSku** pobiera VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="7cee7-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="7cee7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7cee7-107">EXAMPLES</span></span>

### <span data-ttu-id="7cee7-108">Przykład 1: Pobierz VMImage SKU</span><span class="sxs-lookup"><span data-stu-id="7cee7-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="7cee7-109">To polecenie pobiera jednostki SKU określonego wydawcy i oferty.</span><span class="sxs-lookup"><span data-stu-id="7cee7-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="7cee7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7cee7-110">PARAMETERS</span></span>

### <span data-ttu-id="7cee7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cee7-111">-DefaultProfile</span></span>
<span data-ttu-id="7cee7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cee7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cee7-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7cee7-113">-Location</span></span>
<span data-ttu-id="7cee7-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="7cee7-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="7cee7-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="7cee7-115">-Offer</span></span>
<span data-ttu-id="7cee7-116">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="7cee7-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="7cee7-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7cee7-117">-PublisherName</span></span>
<span data-ttu-id="7cee7-118">Umożliwia określenie wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="7cee7-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="7cee7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cee7-119">CommonParameters</span></span>
<span data-ttu-id="7cee7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cee7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cee7-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cee7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cee7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cee7-122">INPUTS</span></span>

## <span data-ttu-id="7cee7-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7cee7-123">OUTPUTS</span></span>

## <span data-ttu-id="7cee7-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7cee7-124">NOTES</span></span>

## <span data-ttu-id="7cee7-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cee7-125">RELATED LINKS</span></span>

[<span data-ttu-id="7cee7-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7cee7-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="7cee7-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7cee7-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="7cee7-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7cee7-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="7cee7-129">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7cee7-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


