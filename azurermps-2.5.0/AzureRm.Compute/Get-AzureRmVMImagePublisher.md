---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898997"
---
# <span data-ttu-id="dbfc2-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="dbfc2-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="dbfc2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dbfc2-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfc2-103">Pobiera wydawców VMImage.</span><span class="sxs-lookup"><span data-stu-id="dbfc2-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbfc2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dbfc2-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbfc2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dbfc2-105">DESCRIPTION</span></span>
<span data-ttu-id="dbfc2-106">Polecenie cmdlet **Get-AzureRmVMImagePublisher** pobiera wydawców VMImage.</span><span class="sxs-lookup"><span data-stu-id="dbfc2-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="dbfc2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dbfc2-107">EXAMPLES</span></span>

### <span data-ttu-id="dbfc2-108">Przykład 1: uzyskiwanie wydawców VMImage dla regionu</span><span class="sxs-lookup"><span data-stu-id="dbfc2-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="dbfc2-109">To polecenie umożliwia uzyskiwanie wydawców wystąpień VMImage dla centralnego regionu USA w ramach Twojego profilu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dbfc2-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="dbfc2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbfc2-110">PARAMETERS</span></span>

### <span data-ttu-id="dbfc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfc2-111">-DefaultProfile</span></span>
<span data-ttu-id="dbfc2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbfc2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbfc2-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dbfc2-113">-Location</span></span>
<span data-ttu-id="dbfc2-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="dbfc2-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="dbfc2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfc2-115">CommonParameters</span></span>
<span data-ttu-id="dbfc2-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbfc2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfc2-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbfc2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfc2-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbfc2-118">INPUTS</span></span>

### <span data-ttu-id="dbfc2-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dbfc2-119">None</span></span>
<span data-ttu-id="dbfc2-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="dbfc2-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dbfc2-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dbfc2-121">OUTPUTS</span></span>

### <span data-ttu-id="dbfc2-122">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="dbfc2-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="dbfc2-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dbfc2-123">NOTES</span></span>

## <span data-ttu-id="dbfc2-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbfc2-124">RELATED LINKS</span></span>

[<span data-ttu-id="dbfc2-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="dbfc2-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="dbfc2-126">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="dbfc2-126">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="dbfc2-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="dbfc2-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="dbfc2-128">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="dbfc2-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


