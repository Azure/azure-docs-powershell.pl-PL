---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181691"
---
# <span data-ttu-id="0bd90-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0bd90-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="0bd90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bd90-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd90-103">Pobiera jednostki SKU WIRTUALNEJ obrazów.</span><span class="sxs-lookup"><span data-stu-id="0bd90-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="0bd90-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0bd90-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bd90-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0bd90-105">DESCRIPTION</span></span>
<span data-ttu-id="0bd90-106">Polecenie **cmdlet Get-AzVMImageSku** pobiera jednostki SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="0bd90-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="0bd90-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0bd90-107">EXAMPLES</span></span>

### <span data-ttu-id="0bd90-108">Przykład 1. Uzyskiwanie jednostki SKU VMImage</span><span class="sxs-lookup"><span data-stu-id="0bd90-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="0bd90-109">To polecenie pobiera jednostki SKU dla określonego wydawcy i ofertę.</span><span class="sxs-lookup"><span data-stu-id="0bd90-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="0bd90-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bd90-110">PARAMETERS</span></span>

### <span data-ttu-id="0bd90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd90-111">-DefaultProfile</span></span>
<span data-ttu-id="0bd90-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd90-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bd90-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0bd90-113">-Location</span></span>
<span data-ttu-id="0bd90-114">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0bd90-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="0bd90-115">— Oferta</span><span class="sxs-lookup"><span data-stu-id="0bd90-115">-Offer</span></span>
<span data-ttu-id="0bd90-116">Określa typ oferty maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0bd90-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="0bd90-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="0bd90-117">-PublisherName</span></span>
<span data-ttu-id="0bd90-118">Określa wydawcę danych PROGRAMU WIRTUALNEGO.</span><span class="sxs-lookup"><span data-stu-id="0bd90-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="0bd90-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd90-119">CommonParameters</span></span>
<span data-ttu-id="0bd90-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bd90-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd90-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bd90-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd90-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bd90-122">INPUTS</span></span>

### <span data-ttu-id="0bd90-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0bd90-123">System.String</span></span>

## <span data-ttu-id="0bd90-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bd90-124">OUTPUTS</span></span>

### <span data-ttu-id="0bd90-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="0bd90-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="0bd90-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0bd90-126">NOTES</span></span>

## <span data-ttu-id="0bd90-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bd90-127">RELATED LINKS</span></span>

[<span data-ttu-id="0bd90-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0bd90-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="0bd90-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0bd90-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="0bd90-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0bd90-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="0bd90-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0bd90-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


