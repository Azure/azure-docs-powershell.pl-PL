---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: bd463ffad1c38265dbca894748d0c5b9a479fade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553367"
---
# <span data-ttu-id="95389-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="95389-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="95389-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95389-102">SYNOPSIS</span></span>
<span data-ttu-id="95389-103">Pobiera wydawców VMImage.</span><span class="sxs-lookup"><span data-stu-id="95389-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95389-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95389-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95389-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95389-105">DESCRIPTION</span></span>
<span data-ttu-id="95389-106">Polecenie cmdlet **Get-AzureRmVMImagePublisher** pobiera wydawców VMImage.</span><span class="sxs-lookup"><span data-stu-id="95389-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="95389-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95389-107">EXAMPLES</span></span>

### <span data-ttu-id="95389-108">Przykład 1: uzyskiwanie wydawców VMImage dla regionu</span><span class="sxs-lookup"><span data-stu-id="95389-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="95389-109">To polecenie umożliwia uzyskiwanie wydawców wystąpień VMImage dla centralnego regionu USA w ramach Twojego profilu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95389-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="95389-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95389-110">PARAMETERS</span></span>

### <span data-ttu-id="95389-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95389-111">-DefaultProfile</span></span>
<span data-ttu-id="95389-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="95389-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95389-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="95389-113">-Location</span></span>
<span data-ttu-id="95389-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="95389-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="95389-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95389-115">CommonParameters</span></span>
<span data-ttu-id="95389-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95389-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95389-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95389-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95389-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95389-118">INPUTS</span></span>

## <span data-ttu-id="95389-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95389-119">OUTPUTS</span></span>

## <span data-ttu-id="95389-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95389-120">NOTES</span></span>

## <span data-ttu-id="95389-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95389-121">RELATED LINKS</span></span>

[<span data-ttu-id="95389-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="95389-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="95389-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="95389-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="95389-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="95389-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="95389-125">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="95389-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)

