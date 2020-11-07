---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 6355ce5cea881f66473ca8d541585187a79fe23e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706393"
---
# <span data-ttu-id="f4b78-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f4b78-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="f4b78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4b78-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b78-103">Pobiera VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="f4b78-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="f4b78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4b78-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4b78-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f4b78-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b78-106">Polecenie cmdlet **Get-AzVMImageSku** pobiera VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="f4b78-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="f4b78-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4b78-107">EXAMPLES</span></span>

### <span data-ttu-id="f4b78-108">Przykład 1: Pobierz VMImage SKU</span><span class="sxs-lookup"><span data-stu-id="f4b78-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="f4b78-109">To polecenie pobiera jednostki SKU określonego wydawcy i oferty.</span><span class="sxs-lookup"><span data-stu-id="f4b78-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="f4b78-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4b78-110">PARAMETERS</span></span>

### <span data-ttu-id="f4b78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b78-111">-DefaultProfile</span></span>
<span data-ttu-id="f4b78-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b78-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4b78-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f4b78-113">-Location</span></span>
<span data-ttu-id="f4b78-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="f4b78-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="f4b78-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="f4b78-115">-Offer</span></span>
<span data-ttu-id="f4b78-116">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="f4b78-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="f4b78-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f4b78-117">-PublisherName</span></span>
<span data-ttu-id="f4b78-118">Umożliwia określenie wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="f4b78-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="f4b78-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b78-119">CommonParameters</span></span>
<span data-ttu-id="f4b78-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b78-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b78-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4b78-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b78-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4b78-122">INPUTS</span></span>

### <span data-ttu-id="f4b78-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f4b78-123">System.String</span></span>

## <span data-ttu-id="f4b78-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4b78-124">OUTPUTS</span></span>

### <span data-ttu-id="f4b78-125">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="f4b78-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="f4b78-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4b78-126">NOTES</span></span>

## <span data-ttu-id="f4b78-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4b78-127">RELATED LINKS</span></span>

[<span data-ttu-id="f4b78-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f4b78-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="f4b78-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f4b78-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="f4b78-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f4b78-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f4b78-131">Zapisz — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f4b78-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


