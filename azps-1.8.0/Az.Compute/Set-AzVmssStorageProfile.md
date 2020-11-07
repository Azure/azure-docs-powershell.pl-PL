---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 44156d29d352adb83fe10fa898af2f655bfd4456
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710182"
---
# <span data-ttu-id="bd11b-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="bd11b-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="bd11b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd11b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd11b-103">Ustawia właściwości profilu magazynu VMSS.</span><span class="sxs-lookup"><span data-stu-id="bd11b-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="bd11b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd11b-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd11b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd11b-105">DESCRIPTION</span></span>
<span data-ttu-id="bd11b-106">Polecenie cmdlet **Set-AzVmssStorageProfile** ustawia właściwości profilu magazynu dla zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="bd11b-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="bd11b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd11b-107">EXAMPLES</span></span>

### <span data-ttu-id="bd11b-108">Przykład 1: Ustawianie właściwości profilu magazynu dla VMSS</span><span class="sxs-lookup"><span data-stu-id="bd11b-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="bd11b-109">To polecenie ustawia właściwości profilu magazynu dla VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="bd11b-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="bd11b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd11b-110">PARAMETERS</span></span>

### <span data-ttu-id="bd11b-111">-Datadysk</span><span class="sxs-lookup"><span data-stu-id="bd11b-111">-DataDisk</span></span>
<span data-ttu-id="bd11b-112">Określa obiekt dysk danych.</span><span class="sxs-lookup"><span data-stu-id="bd11b-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="bd11b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd11b-113">-DefaultProfile</span></span>
<span data-ttu-id="bd11b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd11b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd11b-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="bd11b-115">-DiffDiskSetting</span></span>
<span data-ttu-id="bd11b-116">Określa ustawienia dysku różnicowego dla dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="bd11b-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="bd11b-117">-Image</span><span class="sxs-lookup"><span data-stu-id="bd11b-117">-Image</span></span>
<span data-ttu-id="bd11b-118">Określa identyfikator URI obiektu BLOB dla obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bd11b-118">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="bd11b-119">VMSS tworzy dysk systemu operacyjnego w tym samym kontenerze obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bd11b-119">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="bd11b-120">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="bd11b-120">-ImageReferenceId</span></span>
<span data-ttu-id="bd11b-121">Określa identyfikator odwołania do obrazu.</span><span class="sxs-lookup"><span data-stu-id="bd11b-121">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="bd11b-122">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="bd11b-122">-ImageReferenceOffer</span></span>
<span data-ttu-id="bd11b-123">Określa typ obrazu maszyny wirtualnej (VMImage).</span><span class="sxs-lookup"><span data-stu-id="bd11b-123">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="bd11b-124">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="bd11b-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="bd11b-125">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="bd11b-125">-ImageReferencePublisher</span></span>
<span data-ttu-id="bd11b-126">Określa nazwę wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="bd11b-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="bd11b-127">Aby uzyskać wydawcę, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="bd11b-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="bd11b-128">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="bd11b-128">-ImageReferenceSku</span></span>
<span data-ttu-id="bd11b-129">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="bd11b-129">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="bd11b-130">Aby uzyskać jednostki SKU, użyj polecenia cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="bd11b-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="bd11b-131">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="bd11b-131">-ImageReferenceVersion</span></span>
<span data-ttu-id="bd11b-132">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="bd11b-132">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="bd11b-133">Aby użyć najnowszej wersji, określ wartość najnowszą zamiast konkretnej wersji.</span><span class="sxs-lookup"><span data-stu-id="bd11b-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="bd11b-134">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="bd11b-134">-ManagedDisk</span></span>
<span data-ttu-id="bd11b-135">Określa zarządzany dysk.</span><span class="sxs-lookup"><span data-stu-id="bd11b-135">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="bd11b-136">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="bd11b-136">-OsDiskCaching</span></span>
<span data-ttu-id="bd11b-137">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="bd11b-137">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="bd11b-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bd11b-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bd11b-139">Odczytu</span><span class="sxs-lookup"><span data-stu-id="bd11b-139">ReadOnly</span></span>
- <span data-ttu-id="bd11b-140">ReadWrite wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="bd11b-140">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="bd11b-141">Jeśli zmienisz wartość w polu buforowanie, polecenie cmdlet spowoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bd11b-141">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="bd11b-142">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="bd11b-142">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="bd11b-143">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="bd11b-143">-OsDiskCreateOption</span></span>
<span data-ttu-id="bd11b-144">Określa, jak to polecenie cmdlet tworzy maszyny wirtualne VMSS.</span><span class="sxs-lookup"><span data-stu-id="bd11b-144">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="bd11b-145">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bd11b-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bd11b-146">Dołącz: Ta wartość jest używana w przypadku korzystania z specjalnego dysku w celu utworzenia maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="bd11b-146">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="bd11b-147">FromImage: Ta wartość jest używana podczas tworzenia maszyny wirtualnej VMSS przy użyciu obrazu.</span><span class="sxs-lookup"><span data-stu-id="bd11b-147">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="bd11b-148">Jeśli używasz obrazu platformy, możesz również użyć parametru *imageReference* .</span><span class="sxs-lookup"><span data-stu-id="bd11b-148">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="bd11b-149">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="bd11b-149">-OsDiskName</span></span>
<span data-ttu-id="bd11b-150">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="bd11b-150">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="bd11b-151">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="bd11b-151">-OsDiskOsType</span></span>
<span data-ttu-id="bd11b-152">Określa typ systemu operacyjnego na dysku.</span><span class="sxs-lookup"><span data-stu-id="bd11b-152">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="bd11b-153">Jest to potrzebne tylko w przypadku scenariuszy obrazów użytkownika, a nie dla obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="bd11b-153">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="bd11b-154">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="bd11b-154">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="bd11b-155">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="bd11b-155">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="bd11b-156">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="bd11b-156">-VhdContainer</span></span>
<span data-ttu-id="bd11b-157">Określa adresy URL kontenera, które są używane do przechowywania dysków z systemem operacyjnym dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="bd11b-157">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="bd11b-158">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bd11b-158">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bd11b-159">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="bd11b-159">Specifies the VMSS object.</span></span>
<span data-ttu-id="bd11b-160">Aby uzyskać obiekt, użyj obiektu New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="bd11b-160">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="bd11b-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd11b-161">-Confirm</span></span>
<span data-ttu-id="bd11b-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd11b-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd11b-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd11b-163">-WhatIf</span></span>
<span data-ttu-id="bd11b-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd11b-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd11b-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd11b-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd11b-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd11b-166">CommonParameters</span></span>
<span data-ttu-id="bd11b-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd11b-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd11b-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd11b-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd11b-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd11b-169">INPUTS</span></span>

### <span data-ttu-id="bd11b-170">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bd11b-170">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="bd11b-171">System. String</span><span class="sxs-lookup"><span data-stu-id="bd11b-171">System.String</span></span>

### <span data-ttu-id="bd11b-172">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. CachingTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="bd11b-172">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="bd11b-173">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="bd11b-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="bd11b-174">System. String []</span><span class="sxs-lookup"><span data-stu-id="bd11b-174">System.String[]</span></span>

### <span data-ttu-id="bd11b-175">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="bd11b-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="bd11b-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd11b-176">OUTPUTS</span></span>

### <span data-ttu-id="bd11b-177">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bd11b-177">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bd11b-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd11b-178">NOTES</span></span>

## <span data-ttu-id="bd11b-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd11b-179">RELATED LINKS</span></span>

[<span data-ttu-id="bd11b-180">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="bd11b-180">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="bd11b-181">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="bd11b-181">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="bd11b-182">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="bd11b-182">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="bd11b-183">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bd11b-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


