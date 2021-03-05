---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 983eba222959fb11a50ce94704ebdf39a9bc9fbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013802"
---
# <span data-ttu-id="25ce1-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="25ce1-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="25ce1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="25ce1-103">Pobiera wydawców usługi VMImage.</span><span class="sxs-lookup"><span data-stu-id="25ce1-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="25ce1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25ce1-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25ce1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="25ce1-105">DESCRIPTION</span></span>
<span data-ttu-id="25ce1-106">Polecenie **cmdlet Get-AzVMImagePublisher** pobiera wydawców maszyny WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="25ce1-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="25ce1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25ce1-107">EXAMPLES</span></span>

### <span data-ttu-id="25ce1-108">Przykład 1. Uzyskiwanie wydawców programu VMImage dla regionu</span><span class="sxs-lookup"><span data-stu-id="25ce1-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="25ce1-109">To polecenie pobiera wydawców wystąpień maszyny WIRTUALNEJ dla regionu środkowych Stanów Zjednoczonych w ramach profilu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="25ce1-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="25ce1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25ce1-110">PARAMETERS</span></span>

### <span data-ttu-id="25ce1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ce1-111">-DefaultProfile</span></span>
<span data-ttu-id="25ce1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25ce1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25ce1-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="25ce1-113">-Location</span></span>
<span data-ttu-id="25ce1-114">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="25ce1-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="25ce1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ce1-115">CommonParameters</span></span>
<span data-ttu-id="25ce1-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25ce1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ce1-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25ce1-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ce1-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25ce1-118">INPUTS</span></span>

### <span data-ttu-id="25ce1-119">System.String</span><span class="sxs-lookup"><span data-stu-id="25ce1-119">System.String</span></span>

## <span data-ttu-id="25ce1-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25ce1-120">OUTPUTS</span></span>

### <span data-ttu-id="25ce1-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="25ce1-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="25ce1-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25ce1-122">NOTES</span></span>

## <span data-ttu-id="25ce1-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25ce1-123">RELATED LINKS</span></span>

[<span data-ttu-id="25ce1-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="25ce1-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="25ce1-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="25ce1-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="25ce1-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="25ce1-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="25ce1-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="25ce1-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


