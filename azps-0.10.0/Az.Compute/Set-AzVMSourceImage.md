---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: 88a6431d0a59c4dcd875abb0569a0280325cda18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893350"
---
# <span data-ttu-id="0b4b4-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="0b4b4-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="0b4b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4b4-103">Umożliwia określenie obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="0b4b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b4b4-104">SYNTAX</span></span>

### <span data-ttu-id="0b4b4-105">ImageReferenceSkuParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0b4b4-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b4b4-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b4b4-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b4b4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0b4b4-107">DESCRIPTION</span></span>
<span data-ttu-id="0b4b4-108">Polecenie cmdlet **Set-AzVMSourceImage** określa obraz platformy, który ma być używany dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="0b4b4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b4b4-109">EXAMPLES</span></span>

### <span data-ttu-id="0b4b4-110">Przykład 1. Ustawianie wartości dla obrazu</span><span class="sxs-lookup"><span data-stu-id="0b4b4-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="0b4b4-111">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="0b4b4-112">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0b4b4-113">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="0b4b4-114">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="0b4b4-115">Ostatnie polecenie ustawia wartości dla nazwy, oferty, jednostki SKU i wersji programu Publisher.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="0b4b4-116">Polecenia cmdlet **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** i **Get-AzVMImage** mogą odnajdować te ustawienia.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="0b4b4-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b4b4-117">PARAMETERS</span></span>

### <span data-ttu-id="0b4b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4b4-118">-DefaultProfile</span></span>
<span data-ttu-id="0b4b4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b4b4-120">-ID</span><span class="sxs-lookup"><span data-stu-id="0b4b4-120">-Id</span></span>
<span data-ttu-id="0b4b4-121">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="0b4b4-122">-Offer</span><span class="sxs-lookup"><span data-stu-id="0b4b4-122">-Offer</span></span>
<span data-ttu-id="0b4b4-123">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="0b4b4-124">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="0b4b4-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="0b4b4-125">-PublisherName</span></span>
<span data-ttu-id="0b4b4-126">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="0b4b4-127">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="0b4b4-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="0b4b4-128">-Skus</span></span>
<span data-ttu-id="0b4b4-129">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="0b4b4-130">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="0b4b4-131">-Version</span><span class="sxs-lookup"><span data-stu-id="0b4b4-131">-Version</span></span>
<span data-ttu-id="0b4b4-132">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="0b4b4-133">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="0b4b4-134">-VM</span><span class="sxs-lookup"><span data-stu-id="0b4b4-134">-VM</span></span>
<span data-ttu-id="0b4b4-135">Określa obiekt lokalnego maszyny wirtualnej do skonfigurowania.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="0b4b4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4b4-136">CommonParameters</span></span>
<span data-ttu-id="0b4b4-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b4b4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4b4-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b4b4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4b4-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b4b4-139">INPUTS</span></span>

### <span data-ttu-id="0b4b4-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0b4b4-140">PSVirtualMachine</span></span>
<span data-ttu-id="0b4b4-141">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="0b4b4-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="0b4b4-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b4b4-142">OUTPUTS</span></span>

### <span data-ttu-id="0b4b4-143">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0b4b4-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0b4b4-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b4b4-144">NOTES</span></span>

## <span data-ttu-id="0b4b4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b4b4-145">RELATED LINKS</span></span>

[<span data-ttu-id="0b4b4-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0b4b4-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="0b4b4-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0b4b4-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="0b4b4-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0b4b4-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="0b4b4-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0b4b4-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="0b4b4-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0b4b4-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="0b4b4-151">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="0b4b4-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


