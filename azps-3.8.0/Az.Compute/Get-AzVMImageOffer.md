---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051850"
---
# <span data-ttu-id="7ac1d-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7ac1d-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="7ac1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ac1d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac1d-103">Pobiera typy ofert VMImage.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="7ac1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ac1d-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ac1d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ac1d-105">DESCRIPTION</span></span>
<span data-ttu-id="7ac1d-106">Polecenie cmdlet **Get-AzVMImageOffer** pobiera typy oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="7ac1d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ac1d-107">EXAMPLES</span></span>

### <span data-ttu-id="7ac1d-108">Przykład 1: Uzyskaj typy ofert dla wydawcy</span><span class="sxs-lookup"><span data-stu-id="7ac1d-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="7ac1d-109">To polecenie pobiera typy oferty dla określonego wydawcy w regionie centrali Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="7ac1d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ac1d-110">PARAMETERS</span></span>

### <span data-ttu-id="7ac1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac1d-111">-DefaultProfile</span></span>
<span data-ttu-id="7ac1d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac1d-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7ac1d-113">-Location</span></span>
<span data-ttu-id="7ac1d-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="7ac1d-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7ac1d-115">-PublisherName</span></span>
<span data-ttu-id="7ac1d-116">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="7ac1d-117">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="7ac1d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac1d-118">CommonParameters</span></span>
<span data-ttu-id="7ac1d-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac1d-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ac1d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac1d-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ac1d-121">INPUTS</span></span>

### <span data-ttu-id="7ac1d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="7ac1d-122">System.String</span></span>

## <span data-ttu-id="7ac1d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ac1d-123">OUTPUTS</span></span>

### <span data-ttu-id="7ac1d-124">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="7ac1d-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="7ac1d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ac1d-125">NOTES</span></span>

## <span data-ttu-id="7ac1d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ac1d-126">RELATED LINKS</span></span>

[<span data-ttu-id="7ac1d-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7ac1d-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="7ac1d-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7ac1d-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="7ac1d-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7ac1d-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="7ac1d-130">Zapisz — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7ac1d-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


