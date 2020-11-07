---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: eb31437870a77e4af84bdcb94ffa4172d117c78d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719043"
---
# <span data-ttu-id="c56fe-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c56fe-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="c56fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c56fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c56fe-103">Pobiera typy ofert VMImage.</span><span class="sxs-lookup"><span data-stu-id="c56fe-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c56fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c56fe-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c56fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c56fe-105">DESCRIPTION</span></span>
<span data-ttu-id="c56fe-106">Polecenie cmdlet **Get-AzureRmVMImageOffer** pobiera typy oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="c56fe-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="c56fe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c56fe-107">EXAMPLES</span></span>

### <span data-ttu-id="c56fe-108">Przykład 1: Uzyskaj typy ofert dla wydawcy</span><span class="sxs-lookup"><span data-stu-id="c56fe-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="c56fe-109">To polecenie pobiera typy oferty dla określonego wydawcy w regionie centrali Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="c56fe-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="c56fe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c56fe-110">PARAMETERS</span></span>

### <span data-ttu-id="c56fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56fe-111">-DefaultProfile</span></span>
<span data-ttu-id="c56fe-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c56fe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c56fe-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c56fe-113">-Location</span></span>
<span data-ttu-id="c56fe-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="c56fe-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="c56fe-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c56fe-115">-PublisherName</span></span>
<span data-ttu-id="c56fe-116">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="c56fe-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="c56fe-117">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="c56fe-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="c56fe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56fe-118">CommonParameters</span></span>
<span data-ttu-id="c56fe-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c56fe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56fe-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c56fe-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56fe-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c56fe-121">INPUTS</span></span>

## <span data-ttu-id="c56fe-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c56fe-122">OUTPUTS</span></span>

## <span data-ttu-id="c56fe-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c56fe-123">NOTES</span></span>

## <span data-ttu-id="c56fe-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c56fe-124">RELATED LINKS</span></span>

[<span data-ttu-id="c56fe-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c56fe-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="c56fe-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c56fe-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="c56fe-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c56fe-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="c56fe-128">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c56fe-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)

