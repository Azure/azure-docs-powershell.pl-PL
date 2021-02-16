---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199290"
---
# <span data-ttu-id="110e1-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="110e1-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="110e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="110e1-102">SYNOPSIS</span></span>
<span data-ttu-id="110e1-103">Pobiera wydawców usługi VMImage.</span><span class="sxs-lookup"><span data-stu-id="110e1-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="110e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="110e1-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="110e1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="110e1-105">DESCRIPTION</span></span>
<span data-ttu-id="110e1-106">Polecenie **cmdlet Get-AzVMImagePublisher** pobiera wydawców maszyny WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="110e1-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="110e1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="110e1-107">EXAMPLES</span></span>

### <span data-ttu-id="110e1-108">Przykład 1. Uzyskiwanie wydawców programu VMImage dla regionu</span><span class="sxs-lookup"><span data-stu-id="110e1-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="110e1-109">To polecenie pobiera wydawców wystąpień maszyny WIRTUALNEJ dla regionu Środkowych Stanów Zjednoczonych w ramach profilu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="110e1-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="110e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="110e1-110">PARAMETERS</span></span>

### <span data-ttu-id="110e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="110e1-111">-DefaultProfile</span></span>
<span data-ttu-id="110e1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="110e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="110e1-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="110e1-113">-Location</span></span>
<span data-ttu-id="110e1-114">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="110e1-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="110e1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="110e1-115">CommonParameters</span></span>
<span data-ttu-id="110e1-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="110e1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="110e1-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="110e1-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="110e1-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="110e1-118">INPUTS</span></span>

### <span data-ttu-id="110e1-119">System.String</span><span class="sxs-lookup"><span data-stu-id="110e1-119">System.String</span></span>

## <span data-ttu-id="110e1-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="110e1-120">OUTPUTS</span></span>

### <span data-ttu-id="110e1-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="110e1-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="110e1-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="110e1-122">NOTES</span></span>

## <span data-ttu-id="110e1-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="110e1-123">RELATED LINKS</span></span>

[<span data-ttu-id="110e1-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="110e1-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="110e1-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="110e1-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="110e1-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="110e1-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="110e1-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="110e1-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


