---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 60d525cc50b62350853755ae46698cbecb358654
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525546"
---
# <span data-ttu-id="64205-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="64205-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="64205-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64205-102">SYNOPSIS</span></span>
<span data-ttu-id="64205-103">Ustawia właściwości profilu magazynu VMSS.</span><span class="sxs-lookup"><span data-stu-id="64205-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64205-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64205-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64205-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64205-105">DESCRIPTION</span></span>
<span data-ttu-id="64205-106">Polecenie cmdlet **Set-AzureRmVmssStorageProfile** ustawia właściwości profilu magazynu dla zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="64205-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="64205-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64205-107">EXAMPLES</span></span>

### <span data-ttu-id="64205-108">Przykład 1: Ustawianie właściwości profilu magazynu dla VMSS</span><span class="sxs-lookup"><span data-stu-id="64205-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="64205-109">To polecenie ustawia właściwości profilu magazynu dla VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="64205-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="64205-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64205-110">PARAMETERS</span></span>

### <span data-ttu-id="64205-111">-Datadysk</span><span class="sxs-lookup"><span data-stu-id="64205-111">-DataDisk</span></span>
<span data-ttu-id="64205-112">Określa obiekt dysk danych.</span><span class="sxs-lookup"><span data-stu-id="64205-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64205-113">-DefaultProfile</span></span>
<span data-ttu-id="64205-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64205-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64205-115">-Image</span><span class="sxs-lookup"><span data-stu-id="64205-115">-Image</span></span>
<span data-ttu-id="64205-116">Określa identyfikator URI obiektu BLOB dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="64205-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="64205-117">VMSS tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="64205-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="64205-118">-ImageReferenceId</span></span>
<span data-ttu-id="64205-119">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="64205-119">Specifies the image reference ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="64205-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="64205-121">Określa typ obrazu maszyny wirtualnej (VMImage).</span><span class="sxs-lookup"><span data-stu-id="64205-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="64205-122">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="64205-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="64205-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="64205-124">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="64205-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="64205-125">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="64205-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="64205-126">-ImageReferenceSku</span></span>
<span data-ttu-id="64205-127">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="64205-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="64205-128">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="64205-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="64205-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="64205-130">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="64205-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="64205-131">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="64205-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="64205-132">-ManagedDisk</span></span>
<span data-ttu-id="64205-133">Określa zarządzany dysk.</span><span class="sxs-lookup"><span data-stu-id="64205-133">Specifies the managed disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="64205-134">-OsDiskCaching</span></span>
<span data-ttu-id="64205-135">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="64205-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="64205-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="64205-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64205-137">Odczytu</span><span class="sxs-lookup"><span data-stu-id="64205-137">ReadOnly</span></span>
- <span data-ttu-id="64205-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="64205-138">ReadWrite</span></span>

<span data-ttu-id="64205-139">Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="64205-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="64205-140">Jeśli zmienisz wartość w polu buforowanie, polecenie cmdlet spowoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64205-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="64205-141">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="64205-141">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="64205-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="64205-143">Określa, jak to polecenie cmdlet tworzy maszyny wirtualne VMSS.</span><span class="sxs-lookup"><span data-stu-id="64205-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="64205-144">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="64205-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64205-145">Dołącz: Ta wartość jest używana w przypadku korzystania z specjalnego dysku w celu utworzenia maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="64205-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="64205-146">FromImage: Ta wartość jest używana podczas tworzenia maszyny wirtualnej VMSS przy użyciu obrazu.</span><span class="sxs-lookup"><span data-stu-id="64205-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="64205-147">Jeśli używasz obrazu platformy, możesz również użyć parametru *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="64205-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="64205-148">-OsDiskName</span></span>
<span data-ttu-id="64205-149">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="64205-149">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="64205-150">-OsDiskOsType</span></span>
<span data-ttu-id="64205-151">Określa typ systemu operacyjnego na dysku.</span><span class="sxs-lookup"><span data-stu-id="64205-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="64205-152">Jest to potrzebne tylko w przypadku scenariuszy obrazów użytkownika, a nie dla obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="64205-152">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-153">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="64205-153">-VhdContainer</span></span>
<span data-ttu-id="64205-154">Określa adresy URL kontenera, które są używane do przechowywania dysków z systemem operacyjnym dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="64205-154">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-155">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64205-155">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="64205-156">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="64205-156">Specifies the VMSS object.</span></span>
<span data-ttu-id="64205-157">Aby uzyskać obiekt, użyj obiektu New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="64205-157">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64205-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64205-158">-Confirm</span></span>
<span data-ttu-id="64205-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64205-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64205-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64205-160">-WhatIf</span></span>
<span data-ttu-id="64205-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64205-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64205-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64205-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64205-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64205-163">CommonParameters</span></span>
<span data-ttu-id="64205-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64205-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64205-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64205-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64205-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64205-166">INPUTS</span></span>

###  
<span data-ttu-id="64205-167">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="64205-167">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="64205-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64205-168">OUTPUTS</span></span>

## <span data-ttu-id="64205-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64205-169">NOTES</span></span>

## <span data-ttu-id="64205-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64205-170">RELATED LINKS</span></span>

[<span data-ttu-id="64205-171">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="64205-171">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="64205-172">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="64205-172">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="64205-173">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="64205-173">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="64205-174">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="64205-174">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


