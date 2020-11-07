---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimageoffer
schema: 2.0.0
ms.openlocfilehash: 00169d833244ece2f697d2429f5e5db5ee0bf901
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898529"
---
# <span data-ttu-id="4e453-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4e453-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="4e453-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e453-102">SYNOPSIS</span></span>
<span data-ttu-id="4e453-103">Pobiera typy ofert VMImage.</span><span class="sxs-lookup"><span data-stu-id="4e453-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e453-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e453-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e453-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4e453-105">DESCRIPTION</span></span>
<span data-ttu-id="4e453-106">Polecenie cmdlet **Get-AzureRmVMImageOffer** pobiera typy oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="4e453-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="4e453-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e453-107">EXAMPLES</span></span>

### <span data-ttu-id="4e453-108">Przykład 1: Uzyskaj typy ofert dla wydawcy</span><span class="sxs-lookup"><span data-stu-id="4e453-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="4e453-109">To polecenie pobiera typy oferty dla określonego wydawcy w regionie centrali Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="4e453-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="4e453-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e453-110">PARAMETERS</span></span>

### <span data-ttu-id="4e453-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e453-111">-DefaultProfile</span></span>
<span data-ttu-id="4e453-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e453-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e453-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4e453-113">-Location</span></span>
<span data-ttu-id="4e453-114">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="4e453-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="4e453-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4e453-115">-PublisherName</span></span>
<span data-ttu-id="4e453-116">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="4e453-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="4e453-117">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="4e453-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4e453-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e453-118">CommonParameters</span></span>
<span data-ttu-id="4e453-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e453-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e453-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e453-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e453-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e453-121">INPUTS</span></span>

### <span data-ttu-id="4e453-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4e453-122">None</span></span>
<span data-ttu-id="4e453-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4e453-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e453-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e453-124">OUTPUTS</span></span>

### <span data-ttu-id="4e453-125">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="4e453-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="4e453-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e453-126">NOTES</span></span>

## <span data-ttu-id="4e453-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e453-127">RELATED LINKS</span></span>

[<span data-ttu-id="4e453-128">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4e453-128">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4e453-129">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4e453-129">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4e453-130">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4e453-130">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="4e453-131">Zapisz — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4e453-131">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


