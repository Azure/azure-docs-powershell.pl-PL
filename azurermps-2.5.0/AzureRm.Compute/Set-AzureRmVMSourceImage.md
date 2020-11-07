---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsourceimage
schema: 2.0.0
ms.openlocfilehash: 5e07ba8ffceb42a94c41c0b21c62329f9dbe96a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898522"
---
# <span data-ttu-id="47331-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="47331-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="47331-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47331-102">SYNOPSIS</span></span>
<span data-ttu-id="47331-103">Umożliwia określenie obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="47331-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47331-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47331-104">SYNTAX</span></span>

### <span data-ttu-id="47331-105">ImageReferenceSkuParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="47331-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47331-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47331-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47331-107">Opis</span><span class="sxs-lookup"><span data-stu-id="47331-107">DESCRIPTION</span></span>
<span data-ttu-id="47331-108">Polecenie cmdlet **Set-AzureRmVMSourceImage** określa obraz platformy, który ma być używany dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="47331-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="47331-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47331-109">EXAMPLES</span></span>

### <span data-ttu-id="47331-110">Przykład 1. Ustawianie wartości dla obrazu</span><span class="sxs-lookup"><span data-stu-id="47331-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="47331-111">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="47331-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="47331-112">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="47331-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="47331-113">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="47331-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="47331-114">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="47331-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="47331-115">Ostatnie polecenie ustawia wartości dla nazwy, oferty, jednostki SKU i wersji programu Publisher.</span><span class="sxs-lookup"><span data-stu-id="47331-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="47331-116">Polecenia cmdlet **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** i **Get-AzureRmVMImage** mogą odnajdować te ustawienia.</span><span class="sxs-lookup"><span data-stu-id="47331-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="47331-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47331-117">PARAMETERS</span></span>

### <span data-ttu-id="47331-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47331-118">-DefaultProfile</span></span>
<span data-ttu-id="47331-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47331-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47331-120">-ID</span><span class="sxs-lookup"><span data-stu-id="47331-120">-Id</span></span>
<span data-ttu-id="47331-121">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="47331-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="47331-122">-Offer</span><span class="sxs-lookup"><span data-stu-id="47331-122">-Offer</span></span>
<span data-ttu-id="47331-123">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="47331-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="47331-124">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="47331-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="47331-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="47331-125">-PublisherName</span></span>
<span data-ttu-id="47331-126">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="47331-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="47331-127">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="47331-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="47331-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="47331-128">-Skus</span></span>
<span data-ttu-id="47331-129">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="47331-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="47331-130">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="47331-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="47331-131">-Version</span><span class="sxs-lookup"><span data-stu-id="47331-131">-Version</span></span>
<span data-ttu-id="47331-132">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="47331-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="47331-133">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="47331-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="47331-134">-VM</span><span class="sxs-lookup"><span data-stu-id="47331-134">-VM</span></span>
<span data-ttu-id="47331-135">Określa obiekt lokalnego maszyny wirtualnej do skonfigurowania.</span><span class="sxs-lookup"><span data-stu-id="47331-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="47331-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47331-136">CommonParameters</span></span>
<span data-ttu-id="47331-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47331-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47331-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47331-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47331-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47331-139">INPUTS</span></span>

### <span data-ttu-id="47331-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="47331-140">PSVirtualMachine</span></span>
<span data-ttu-id="47331-141">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="47331-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="47331-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47331-142">OUTPUTS</span></span>

### <span data-ttu-id="47331-143">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="47331-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="47331-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47331-144">NOTES</span></span>

## <span data-ttu-id="47331-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47331-145">RELATED LINKS</span></span>

[<span data-ttu-id="47331-146">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47331-146">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="47331-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="47331-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="47331-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="47331-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="47331-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="47331-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="47331-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="47331-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="47331-151">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="47331-151">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


