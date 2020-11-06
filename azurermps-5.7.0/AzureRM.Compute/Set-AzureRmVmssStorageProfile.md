---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 26f61261bd8fd1c2d5fc2bbdacec71f73db91fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548151"
---
# <span data-ttu-id="87454-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="87454-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="87454-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87454-102">SYNOPSIS</span></span>
<span data-ttu-id="87454-103">Ustawia właściwości profilu magazynu VMSS.</span><span class="sxs-lookup"><span data-stu-id="87454-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87454-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87454-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [-OsDiskName <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87454-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87454-105">DESCRIPTION</span></span>
<span data-ttu-id="87454-106">Polecenie cmdlet **Set-AzureRmVmssStorageProfile** ustawia właściwości profilu magazynu dla zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="87454-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="87454-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87454-107">EXAMPLES</span></span>

### <span data-ttu-id="87454-108">Przykład 1: Ustawianie właściwości profilu magazynu dla VMSS</span><span class="sxs-lookup"><span data-stu-id="87454-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="87454-109">To polecenie ustawia właściwości profilu magazynu dla VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="87454-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="87454-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87454-110">PARAMETERS</span></span>

### <span data-ttu-id="87454-111">-Datadysk</span><span class="sxs-lookup"><span data-stu-id="87454-111">-DataDisk</span></span>
<span data-ttu-id="87454-112">Określa obiekt dysk danych.</span><span class="sxs-lookup"><span data-stu-id="87454-112">Specifies the data disk object.</span></span>

```yaml
Type: VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-113">-Image</span><span class="sxs-lookup"><span data-stu-id="87454-113">-Image</span></span>
<span data-ttu-id="87454-114">Określa identyfikator URI obiektu BLOB dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="87454-114">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="87454-115">VMSS tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="87454-115">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-116">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="87454-116">-ImageReferenceId</span></span>
<span data-ttu-id="87454-117">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="87454-117">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-118">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="87454-118">-ImageReferenceOffer</span></span>
<span data-ttu-id="87454-119">Określa typ obrazu maszyny wirtualnej (VMImage).</span><span class="sxs-lookup"><span data-stu-id="87454-119">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="87454-120">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="87454-120">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-121">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="87454-121">-ImageReferencePublisher</span></span>
<span data-ttu-id="87454-122">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="87454-122">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="87454-123">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="87454-123">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-124">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="87454-124">-ImageReferenceSku</span></span>
<span data-ttu-id="87454-125">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="87454-125">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="87454-126">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="87454-126">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-127">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="87454-127">-ImageReferenceVersion</span></span>
<span data-ttu-id="87454-128">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="87454-128">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="87454-129">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="87454-129">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-130">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="87454-130">-ManagedDisk</span></span>
<span data-ttu-id="87454-131">Określa zarządzany dysk.</span><span class="sxs-lookup"><span data-stu-id="87454-131">Specifies the managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-132">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="87454-132">-OsDiskCaching</span></span>
<span data-ttu-id="87454-133">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="87454-133">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="87454-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="87454-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87454-135">Odczytu</span><span class="sxs-lookup"><span data-stu-id="87454-135">ReadOnly</span></span>
- <span data-ttu-id="87454-136">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="87454-136">ReadWrite</span></span>

<span data-ttu-id="87454-137">Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="87454-137">The default value is ReadWrite.</span></span>
<span data-ttu-id="87454-138">Jeśli zmienisz wartość w polu buforowanie, polecenie cmdlet spowoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="87454-138">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="87454-139">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="87454-139">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-140">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="87454-140">-OsDiskCreateOption</span></span>
<span data-ttu-id="87454-141">Określa, jak to polecenie cmdlet tworzy maszyny wirtualne VMSS.</span><span class="sxs-lookup"><span data-stu-id="87454-141">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="87454-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="87454-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87454-143">Dołącz: Ta wartość jest używana w przypadku korzystania z specjalnego dysku w celu utworzenia maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="87454-143">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="87454-144">FromImage: Ta wartość jest używana podczas tworzenia maszyny wirtualnej VMSS przy użyciu obrazu.</span><span class="sxs-lookup"><span data-stu-id="87454-144">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="87454-145">Jeśli używasz obrazu platformy, możesz również użyć parametru *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="87454-145">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-146">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="87454-146">-OsDiskName</span></span>
<span data-ttu-id="87454-147">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="87454-147">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-148">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="87454-148">-OsDiskOsType</span></span>
<span data-ttu-id="87454-149">Określa typ systemu operacyjnego na dysku.</span><span class="sxs-lookup"><span data-stu-id="87454-149">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="87454-150">Jest to potrzebne tylko w przypadku scenariuszy obrazów użytkownika, a nie dla obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="87454-150">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-151">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="87454-151">-VhdContainer</span></span>
<span data-ttu-id="87454-152">Określa adresy URL kontenera, które są używane do przechowywania dysków z systemem operacyjnym dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="87454-152">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-153">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="87454-153">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="87454-154">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="87454-154">Specifies the VMSS object.</span></span>
<span data-ttu-id="87454-155">Aby uzyskać obiekt, użyj obiektu New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="87454-155">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87454-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87454-156">-Confirm</span></span>
<span data-ttu-id="87454-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87454-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87454-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87454-158">-WhatIf</span></span>
<span data-ttu-id="87454-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87454-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87454-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87454-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87454-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87454-161">CommonParameters</span></span>
<span data-ttu-id="87454-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87454-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87454-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87454-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87454-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87454-164">INPUTS</span></span>

###  
<span data-ttu-id="87454-165">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="87454-165">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="87454-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87454-166">OUTPUTS</span></span>

## <span data-ttu-id="87454-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87454-167">NOTES</span></span>

## <span data-ttu-id="87454-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87454-168">RELATED LINKS</span></span>

[<span data-ttu-id="87454-169">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="87454-169">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="87454-170">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="87454-170">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="87454-171">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="87454-171">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="87454-172">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="87454-172">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


