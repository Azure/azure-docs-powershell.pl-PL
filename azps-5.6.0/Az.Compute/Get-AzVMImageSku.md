---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 4eea328b83b4d4ad70ba755e4875168b6b35ecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013745"
---
# <span data-ttu-id="966e9-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="966e9-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="966e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="966e9-102">SYNOPSIS</span></span>
<span data-ttu-id="966e9-103">Pobiera jednostki SKU WIRTUALNEJ obrazów.</span><span class="sxs-lookup"><span data-stu-id="966e9-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="966e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="966e9-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="966e9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="966e9-105">DESCRIPTION</span></span>
<span data-ttu-id="966e9-106">Polecenie **cmdlet Get-AzVMImageSku** pobiera jednostki SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="966e9-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="966e9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="966e9-107">EXAMPLES</span></span>

### <span data-ttu-id="966e9-108">Przykład 1. Uzyskiwanie jednostki SKU VMImage</span><span class="sxs-lookup"><span data-stu-id="966e9-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="966e9-109">To polecenie pobiera jednostki SKU dla określonego wydawcy i ofertę.</span><span class="sxs-lookup"><span data-stu-id="966e9-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="966e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="966e9-110">PARAMETERS</span></span>

### <span data-ttu-id="966e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966e9-111">-DefaultProfile</span></span>
<span data-ttu-id="966e9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="966e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="966e9-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="966e9-113">-Location</span></span>
<span data-ttu-id="966e9-114">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="966e9-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="966e9-115">— Oferta</span><span class="sxs-lookup"><span data-stu-id="966e9-115">-Offer</span></span>
<span data-ttu-id="966e9-116">Określa typ oferty maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="966e9-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="966e9-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="966e9-117">-PublisherName</span></span>
<span data-ttu-id="966e9-118">Określa wydawcę obrazów MASZYNY WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="966e9-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="966e9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966e9-119">CommonParameters</span></span>
<span data-ttu-id="966e9-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="966e9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966e9-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="966e9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966e9-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="966e9-122">INPUTS</span></span>

### <span data-ttu-id="966e9-123">System.String</span><span class="sxs-lookup"><span data-stu-id="966e9-123">System.String</span></span>

## <span data-ttu-id="966e9-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="966e9-124">OUTPUTS</span></span>

### <span data-ttu-id="966e9-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="966e9-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="966e9-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="966e9-126">NOTES</span></span>

## <span data-ttu-id="966e9-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="966e9-127">RELATED LINKS</span></span>

[<span data-ttu-id="966e9-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="966e9-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="966e9-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="966e9-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="966e9-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="966e9-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="966e9-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="966e9-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


