---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: 94556ce0b78b90ae9c418aee175f090e9209adb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013809"
---
# <span data-ttu-id="bad71-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="bad71-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="bad71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bad71-102">SYNOPSIS</span></span>
<span data-ttu-id="bad71-103">Pobiera typy ofert dla usługi VMImage.</span><span class="sxs-lookup"><span data-stu-id="bad71-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="bad71-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bad71-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bad71-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bad71-105">DESCRIPTION</span></span>
<span data-ttu-id="bad71-106">Polecenie **cmdlet Get-AzVMImageOffer** pobiera typy ofert WIRTUALNEJImage.</span><span class="sxs-lookup"><span data-stu-id="bad71-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="bad71-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bad71-107">EXAMPLES</span></span>

### <span data-ttu-id="bad71-108">Przykład 1. Uzyskiwanie typów ofert dla wydawcy</span><span class="sxs-lookup"><span data-stu-id="bad71-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="bad71-109">To polecenie pobiera typy ofert dla określonego wydawcy w regionie Środkowych Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="bad71-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="bad71-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bad71-110">PARAMETERS</span></span>

### <span data-ttu-id="bad71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bad71-111">-DefaultProfile</span></span>
<span data-ttu-id="bad71-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bad71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bad71-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bad71-113">-Location</span></span>
<span data-ttu-id="bad71-114">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bad71-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="bad71-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="bad71-115">-PublisherName</span></span>
<span data-ttu-id="bad71-116">Określa nazwę wydawcy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bad71-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="bad71-117">Aby uzyskać wydawcę, użyj Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bad71-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="bad71-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad71-118">CommonParameters</span></span>
<span data-ttu-id="bad71-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bad71-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad71-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bad71-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad71-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bad71-121">INPUTS</span></span>

### <span data-ttu-id="bad71-122">System.String</span><span class="sxs-lookup"><span data-stu-id="bad71-122">System.String</span></span>

## <span data-ttu-id="bad71-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bad71-123">OUTPUTS</span></span>

### <span data-ttu-id="bad71-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="bad71-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="bad71-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bad71-125">NOTES</span></span>

## <span data-ttu-id="bad71-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bad71-126">RELATED LINKS</span></span>

[<span data-ttu-id="bad71-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="bad71-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="bad71-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="bad71-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="bad71-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="bad71-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="bad71-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="bad71-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


