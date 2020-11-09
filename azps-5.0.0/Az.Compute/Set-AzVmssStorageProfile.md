---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304212"
---
# <span data-ttu-id="45096-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="45096-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="45096-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45096-102">SYNOPSIS</span></span>
<span data-ttu-id="45096-103">Ustawia właściwości profilu magazynu VMSS.</span><span class="sxs-lookup"><span data-stu-id="45096-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="45096-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45096-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45096-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45096-105">DESCRIPTION</span></span>
<span data-ttu-id="45096-106">Polecenie cmdlet **Set-AzVmssStorageProfile** ustawia właściwości profilu magazynu dla zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="45096-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="45096-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45096-107">EXAMPLES</span></span>

### <span data-ttu-id="45096-108">Przykład 1: Ustawianie właściwości profilu magazynu dla VMSS</span><span class="sxs-lookup"><span data-stu-id="45096-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="45096-109">To polecenie ustawia właściwości profilu magazynu dla VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="45096-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="45096-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45096-110">PARAMETERS</span></span>

### <span data-ttu-id="45096-111">-Datadysk</span><span class="sxs-lookup"><span data-stu-id="45096-111">-DataDisk</span></span>
<span data-ttu-id="45096-112">Określa obiekt dysk danych.</span><span class="sxs-lookup"><span data-stu-id="45096-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="45096-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45096-113">-DefaultProfile</span></span>
<span data-ttu-id="45096-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45096-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45096-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="45096-115">-DiffDiskSetting</span></span>
<span data-ttu-id="45096-116">Określa ustawienia dysku różnicowego dla dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="45096-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="45096-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="45096-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="45096-118">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanego przez klienta.</span><span class="sxs-lookup"><span data-stu-id="45096-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="45096-119">Ten parametr może być określony tylko dla dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="45096-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="45096-120">-Image</span><span class="sxs-lookup"><span data-stu-id="45096-120">-Image</span></span>
<span data-ttu-id="45096-121">Określa identyfikator URI obiektu BLOB dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="45096-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="45096-122">VMSS tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="45096-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="45096-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="45096-123">-ImageReferenceId</span></span>
<span data-ttu-id="45096-124">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="45096-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="45096-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="45096-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="45096-126">Określa typ obrazu maszyny wirtualnej (VMImage).</span><span class="sxs-lookup"><span data-stu-id="45096-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="45096-127">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="45096-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="45096-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="45096-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="45096-129">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="45096-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="45096-130">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="45096-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="45096-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="45096-131">-ImageReferenceSku</span></span>
<span data-ttu-id="45096-132">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="45096-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="45096-133">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="45096-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="45096-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="45096-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="45096-135">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="45096-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="45096-136">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="45096-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="45096-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="45096-137">-ManagedDisk</span></span>
<span data-ttu-id="45096-138">Określa zarządzany dysk.</span><span class="sxs-lookup"><span data-stu-id="45096-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="45096-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="45096-139">-OsDiskCaching</span></span>
<span data-ttu-id="45096-140">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="45096-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="45096-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="45096-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45096-142">Odczytu</span><span class="sxs-lookup"><span data-stu-id="45096-142">ReadOnly</span></span>
- <span data-ttu-id="45096-143">ReadWrite wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="45096-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="45096-144">Jeśli zmienisz wartość w polu buforowanie, polecenie cmdlet spowoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45096-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="45096-145">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="45096-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="45096-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="45096-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="45096-147">Określa, jak to polecenie cmdlet tworzy maszyny wirtualne VMSS.</span><span class="sxs-lookup"><span data-stu-id="45096-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="45096-148">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="45096-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45096-149">Dołącz: Ta wartość jest używana w przypadku korzystania z specjalnego dysku w celu utworzenia maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="45096-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="45096-150">FromImage: Ta wartość jest używana podczas tworzenia maszyny wirtualnej VMSS przy użyciu obrazu.</span><span class="sxs-lookup"><span data-stu-id="45096-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="45096-151">Jeśli używasz obrazu platformy, możesz również użyć parametru *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="45096-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45096-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="45096-152">-OsDiskName</span></span>
<span data-ttu-id="45096-153">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="45096-153">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="45096-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="45096-154">-OsDiskOsType</span></span>
<span data-ttu-id="45096-155">Określa typ systemu operacyjnego na dysku.</span><span class="sxs-lookup"><span data-stu-id="45096-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="45096-156">Jest to potrzebne tylko w przypadku scenariuszy obrazów użytkownika, a nie dla obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="45096-156">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="45096-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="45096-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="45096-158">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="45096-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45096-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="45096-159">-VhdContainer</span></span>
<span data-ttu-id="45096-160">Określa adresy URL kontenera, które są używane do przechowywania dysków z systemem operacyjnym dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="45096-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="45096-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="45096-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="45096-162">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="45096-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="45096-163">Aby uzyskać obiekt, użyj obiektu New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="45096-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="45096-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45096-164">-Confirm</span></span>
<span data-ttu-id="45096-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45096-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45096-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45096-166">-WhatIf</span></span>
<span data-ttu-id="45096-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45096-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45096-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45096-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45096-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45096-169">CommonParameters</span></span>
<span data-ttu-id="45096-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45096-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45096-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45096-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45096-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45096-172">INPUTS</span></span>

### <span data-ttu-id="45096-173">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="45096-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="45096-174">System. String</span><span class="sxs-lookup"><span data-stu-id="45096-174">System.String</span></span>

### <span data-ttu-id="45096-175">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. CachingTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="45096-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="45096-176">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="45096-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="45096-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="45096-177">System.String[]</span></span>

### <span data-ttu-id="45096-178">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="45096-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="45096-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45096-179">OUTPUTS</span></span>

### <span data-ttu-id="45096-180">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="45096-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="45096-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45096-181">NOTES</span></span>

## <span data-ttu-id="45096-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45096-182">RELATED LINKS</span></span>

[<span data-ttu-id="45096-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="45096-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="45096-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="45096-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="45096-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="45096-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="45096-186">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="45096-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


