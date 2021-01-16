---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349201"
---
# <span data-ttu-id="c6e7c-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c6e7c-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="c6e7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e7c-103">Pobiera wydawców VMImage.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="c6e7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6e7c-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6e7c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c6e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="c6e7c-106">Polecenie cmdlet **Get-AzVMImagePublisher** pobiera wydawców VMImage.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="c6e7c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6e7c-107">EXAMPLES</span></span>

### <span data-ttu-id="c6e7c-108">Przykład 1: uzyskiwanie wydawców VMImage dla regionu</span><span class="sxs-lookup"><span data-stu-id="c6e7c-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="c6e7c-109">To polecenie umożliwia uzyskiwanie wydawców wystąpień VMImage dla centralnego regionu USA w ramach Twojego profilu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="c6e7c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6e7c-110">PARAMETERS</span></span>

### <span data-ttu-id="c6e7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e7c-111">-DefaultProfile</span></span>
<span data-ttu-id="c6e7c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e7c-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c6e7c-113">-Location</span></span>
<span data-ttu-id="c6e7c-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="c6e7c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e7c-115">CommonParameters</span></span>
<span data-ttu-id="c6e7c-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e7c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e7c-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6e7c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e7c-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6e7c-118">INPUTS</span></span>

### <span data-ttu-id="c6e7c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c6e7c-119">System.String</span></span>

## <span data-ttu-id="c6e7c-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6e7c-120">OUTPUTS</span></span>

### <span data-ttu-id="c6e7c-121">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c6e7c-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="c6e7c-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6e7c-122">NOTES</span></span>

## <span data-ttu-id="c6e7c-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6e7c-123">RELATED LINKS</span></span>

[<span data-ttu-id="c6e7c-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c6e7c-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="c6e7c-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c6e7c-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="c6e7c-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c6e7c-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="c6e7c-127">Zapisz — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c6e7c-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


