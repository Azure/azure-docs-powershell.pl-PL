---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: 109f55c1afc1c00d26c47d0131d098158010bd70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93554422"
---
# <span data-ttu-id="f3562-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f3562-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="f3562-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3562-102">SYNOPSIS</span></span>
<span data-ttu-id="f3562-103">Pobiera wydawców VMImage.</span><span class="sxs-lookup"><span data-stu-id="f3562-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3562-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3562-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3562-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f3562-105">DESCRIPTION</span></span>
<span data-ttu-id="f3562-106">Polecenie cmdlet **Get-AzureRmVMImagePublisher** pobiera wydawców VMImage.</span><span class="sxs-lookup"><span data-stu-id="f3562-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="f3562-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3562-107">EXAMPLES</span></span>

### <span data-ttu-id="f3562-108">Przykład 1: uzyskiwanie wydawców VMImage dla regionu</span><span class="sxs-lookup"><span data-stu-id="f3562-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="f3562-109">To polecenie umożliwia uzyskiwanie wydawców wystąpień VMImage dla centralnego regionu USA w ramach Twojego profilu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f3562-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="f3562-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3562-110">PARAMETERS</span></span>

### <span data-ttu-id="f3562-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3562-111">-DefaultProfile</span></span>
<span data-ttu-id="f3562-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3562-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3562-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f3562-113">-Location</span></span>
<span data-ttu-id="f3562-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="f3562-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="f3562-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3562-115">CommonParameters</span></span>
<span data-ttu-id="f3562-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3562-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3562-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3562-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3562-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3562-118">INPUTS</span></span>

### <span data-ttu-id="f3562-119">System. String</span><span class="sxs-lookup"><span data-stu-id="f3562-119">System.String</span></span>

## <span data-ttu-id="f3562-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3562-120">OUTPUTS</span></span>

### <span data-ttu-id="f3562-121">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f3562-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="f3562-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3562-122">NOTES</span></span>

## <span data-ttu-id="f3562-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3562-123">RELATED LINKS</span></span>

[<span data-ttu-id="f3562-124">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f3562-124">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="f3562-125">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f3562-125">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f3562-126">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f3562-126">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="f3562-127">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f3562-127">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


