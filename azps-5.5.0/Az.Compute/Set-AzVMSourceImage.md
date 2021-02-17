---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a1ed1fa266638891507b6853199bff23d23aa1b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238629"
---
# <span data-ttu-id="6a7dc-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="6a7dc-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="6a7dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a7dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7dc-103">Określa obraz dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="6a7dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a7dc-104">SYNTAX</span></span>

### <span data-ttu-id="6a7dc-105">ImageReferenceSkuParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6a7dc-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a7dc-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a7dc-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a7dc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a7dc-107">DESCRIPTION</span></span>
<span data-ttu-id="6a7dc-108">Polecenie **cmdlet Set-AzVMSourceImage** określa obraz platformy do użycia dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="6a7dc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a7dc-109">EXAMPLES</span></span>

### <span data-ttu-id="6a7dc-110">Przykład 1. Ustawianie wartości obrazu</span><span class="sxs-lookup"><span data-stu-id="6a7dc-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="6a7dc-111">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie Grupa Zasobów11, a następnie przechowuje ten obiekt w zmiennej $AvailabilitySet zasobów.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="6a7dc-112">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6a7dc-113">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6a7dc-114">Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="6a7dc-115">Ostatnie polecenie ustawia wartości dla nazwy wydawcy, oferty, wersji i wersji.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="6a7dc-116">Polecenia cmdlet **Get-AzVMImagePublisher,** **Get-AzVMImageOffer,** **Get-AzVMImageSku** i **Get-AzVMImage** mogą wykryć te ustawienia.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-116">The **Get-AzVMImagePublisher**, **Get-AzVMImageOffer**, **Get-AzVMImageSku**, and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="6a7dc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a7dc-117">PARAMETERS</span></span>

### <span data-ttu-id="6a7dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7dc-118">-DefaultProfile</span></span>
<span data-ttu-id="6a7dc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a7dc-120">— Id</span><span class="sxs-lookup"><span data-stu-id="6a7dc-120">-Id</span></span>
<span data-ttu-id="6a7dc-121">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-121">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a7dc-122">— Oferta</span><span class="sxs-lookup"><span data-stu-id="6a7dc-122">-Offer</span></span>
<span data-ttu-id="6a7dc-123">Określa typ oferty MASZYNY WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="6a7dc-124">Aby uzyskać ofertę obrazu, użyj Get-AzVMImageOffer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a7dc-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6a7dc-125">-PublisherName</span></span>
<span data-ttu-id="6a7dc-126">Określa nazwę wydawcy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="6a7dc-127">Aby uzyskać wydawcę, użyj Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a7dc-128">— jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="6a7dc-128">-Skus</span></span>
<span data-ttu-id="6a7dc-129">Określa sKU MASZYNY.WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="6a7dc-130">Aby uzyskać jednostki SKU, użyj Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a7dc-131">— Wersja</span><span class="sxs-lookup"><span data-stu-id="6a7dc-131">-Version</span></span>
<span data-ttu-id="6a7dc-132">Określa wersję maszyny WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="6a7dc-133">Aby używać najnowszej wersji, określ wartość najnowszej zamiast określonej wersji.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a7dc-134">- MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="6a7dc-134">-VM</span></span>
<span data-ttu-id="6a7dc-135">Określa lokalny obiekt maszyny wirtualnej do skonfigurowania.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a7dc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7dc-136">CommonParameters</span></span>
<span data-ttu-id="6a7dc-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7dc-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a7dc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7dc-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a7dc-139">INPUTS</span></span>

### <span data-ttu-id="6a7dc-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6a7dc-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6a7dc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6a7dc-141">System.String</span></span>

## <span data-ttu-id="6a7dc-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a7dc-142">OUTPUTS</span></span>

### <span data-ttu-id="6a7dc-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6a7dc-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6a7dc-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a7dc-144">NOTES</span></span>

## <span data-ttu-id="6a7dc-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a7dc-145">RELATED LINKS</span></span>

[<span data-ttu-id="6a7dc-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6a7dc-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="6a7dc-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="6a7dc-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="6a7dc-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="6a7dc-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="6a7dc-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6a7dc-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="6a7dc-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="6a7dc-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="6a7dc-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="6a7dc-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


