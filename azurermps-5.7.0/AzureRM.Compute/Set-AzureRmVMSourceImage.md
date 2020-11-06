---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: d96d583f871e0d037c72018339d44952562bac35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526910"
---
# <span data-ttu-id="69ca5-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="69ca5-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="69ca5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="69ca5-103">Umożliwia określenie obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="69ca5-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ca5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69ca5-104">SYNTAX</span></span>

### <span data-ttu-id="69ca5-105">ImageReferenceSkuParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69ca5-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [<CommonParameters>]
```

### <span data-ttu-id="69ca5-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69ca5-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="69ca5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="69ca5-107">DESCRIPTION</span></span>
<span data-ttu-id="69ca5-108">Polecenie cmdlet **Set-AzureRmVMSourceImage** określa obraz platformy, który ma być używany dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="69ca5-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="69ca5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69ca5-109">EXAMPLES</span></span>

### <span data-ttu-id="69ca5-110">Przykład 1. Ustawianie wartości dla obrazu</span><span class="sxs-lookup"><span data-stu-id="69ca5-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="69ca5-111">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="69ca5-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="69ca5-112">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="69ca5-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="69ca5-113">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="69ca5-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="69ca5-114">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="69ca5-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="69ca5-115">Ostatnie polecenie ustawia wartości dla nazwy, oferty, jednostki SKU i wersji programu Publisher.</span><span class="sxs-lookup"><span data-stu-id="69ca5-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="69ca5-116">Polecenia cmdlet **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** i **Get-AzureRmVMImage** mogą odnajdować te ustawienia.</span><span class="sxs-lookup"><span data-stu-id="69ca5-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="69ca5-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69ca5-117">PARAMETERS</span></span>

### <span data-ttu-id="69ca5-118">-ID</span><span class="sxs-lookup"><span data-stu-id="69ca5-118">-Id</span></span>
<span data-ttu-id="69ca5-119">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="69ca5-119">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceIdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ca5-120">-Offer</span><span class="sxs-lookup"><span data-stu-id="69ca5-120">-Offer</span></span>
<span data-ttu-id="69ca5-121">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="69ca5-121">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="69ca5-122">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="69ca5-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ca5-123">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="69ca5-123">-PublisherName</span></span>
<span data-ttu-id="69ca5-124">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="69ca5-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="69ca5-125">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="69ca5-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ca5-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="69ca5-126">-Skus</span></span>
<span data-ttu-id="69ca5-127">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="69ca5-127">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="69ca5-128">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="69ca5-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ca5-129">-Version</span><span class="sxs-lookup"><span data-stu-id="69ca5-129">-Version</span></span>
<span data-ttu-id="69ca5-130">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="69ca5-130">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="69ca5-131">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="69ca5-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ca5-132">-VM</span><span class="sxs-lookup"><span data-stu-id="69ca5-132">-VM</span></span>
<span data-ttu-id="69ca5-133">Określa obiekt lokalnego maszyny wirtualnej do skonfigurowania.</span><span class="sxs-lookup"><span data-stu-id="69ca5-133">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ca5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ca5-134">CommonParameters</span></span>
<span data-ttu-id="69ca5-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ca5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ca5-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ca5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ca5-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69ca5-137">INPUTS</span></span>

### <span data-ttu-id="69ca5-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="69ca5-138">None</span></span>
<span data-ttu-id="69ca5-139">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="69ca5-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69ca5-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69ca5-140">OUTPUTS</span></span>

## <span data-ttu-id="69ca5-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69ca5-141">NOTES</span></span>

## <span data-ttu-id="69ca5-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69ca5-142">RELATED LINKS</span></span>

[<span data-ttu-id="69ca5-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="69ca5-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="69ca5-144">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="69ca5-144">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="69ca5-145">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="69ca5-145">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="69ca5-146">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="69ca5-146">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="69ca5-147">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="69ca5-147">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="69ca5-148">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="69ca5-148">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


