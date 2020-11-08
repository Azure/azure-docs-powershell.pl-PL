---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220161"
---
# <span data-ttu-id="d85fb-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d85fb-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="d85fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d85fb-102">SYNOPSIS</span></span>
<span data-ttu-id="d85fb-103">Pobiera VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="d85fb-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="d85fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d85fb-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d85fb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d85fb-105">DESCRIPTION</span></span>
<span data-ttu-id="d85fb-106">Polecenie cmdlet **Get-AzVMImageSku** pobiera VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="d85fb-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="d85fb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d85fb-107">EXAMPLES</span></span>

### <span data-ttu-id="d85fb-108">Przykład 1: Pobierz VMImage SKU</span><span class="sxs-lookup"><span data-stu-id="d85fb-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="d85fb-109">To polecenie pobiera jednostki SKU określonego wydawcy i oferty.</span><span class="sxs-lookup"><span data-stu-id="d85fb-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="d85fb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d85fb-110">PARAMETERS</span></span>

### <span data-ttu-id="d85fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85fb-111">-DefaultProfile</span></span>
<span data-ttu-id="d85fb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d85fb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d85fb-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d85fb-113">-Location</span></span>
<span data-ttu-id="d85fb-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="d85fb-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="d85fb-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="d85fb-115">-Offer</span></span>
<span data-ttu-id="d85fb-116">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="d85fb-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="d85fb-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="d85fb-117">-PublisherName</span></span>
<span data-ttu-id="d85fb-118">Umożliwia określenie wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="d85fb-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="d85fb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85fb-119">CommonParameters</span></span>
<span data-ttu-id="d85fb-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d85fb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85fb-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d85fb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85fb-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d85fb-122">INPUTS</span></span>

### <span data-ttu-id="d85fb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d85fb-123">System.String</span></span>

## <span data-ttu-id="d85fb-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d85fb-124">OUTPUTS</span></span>

### <span data-ttu-id="d85fb-125">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="d85fb-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="d85fb-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d85fb-126">NOTES</span></span>

## <span data-ttu-id="d85fb-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d85fb-127">RELATED LINKS</span></span>

[<span data-ttu-id="d85fb-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d85fb-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="d85fb-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d85fb-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="d85fb-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d85fb-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="d85fb-131">Zapisz — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d85fb-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


