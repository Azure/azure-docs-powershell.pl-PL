---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233975"
---
# <span data-ttu-id="c4c45-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="c4c45-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="c4c45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4c45-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c45-103">Dodaje dysk danych do VMSS.</span><span class="sxs-lookup"><span data-stu-id="c4c45-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="c4c45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4c45-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4c45-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c4c45-105">DESCRIPTION</span></span>
<span data-ttu-id="c4c45-106">Polecenie cmdlet **Add-AzVmssDataDisk** dodaje dysk danych do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c4c45-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="c4c45-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4c45-107">EXAMPLES</span></span>

### <span data-ttu-id="c4c45-108">Przykład 1: Dodawanie dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="c4c45-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="c4c45-109">To polecenie dodaje pusty dysk danych do obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="c4c45-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="c4c45-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4c45-110">PARAMETERS</span></span>

### <span data-ttu-id="c4c45-111">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="c4c45-111">-Caching</span></span>
<span data-ttu-id="c4c45-112">Określa typ buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="c4c45-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c45-113">-Opcja</span><span class="sxs-lookup"><span data-stu-id="c4c45-113">-CreateOption</span></span>
<span data-ttu-id="c4c45-114">Określa opcję tworzenia dysku.</span><span class="sxs-lookup"><span data-stu-id="c4c45-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="c4c45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c45-115">-DefaultProfile</span></span>
<span data-ttu-id="c4c45-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c45-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4c45-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="c4c45-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="c4c45-118">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanego przez klienta.</span><span class="sxs-lookup"><span data-stu-id="c4c45-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="c4c45-119">Ten parametr może być określony tylko dla dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="c4c45-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="c4c45-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="c4c45-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="c4c45-121">Określa Read-Write IOPS dla zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="c4c45-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="c4c45-122">Należy użyć tylko wtedy, gdy StorageAccountType jest UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="c4c45-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="c4c45-123">Jeśli nie określono tej wartości, przypisze się wartość domyślna na podstawie diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="c4c45-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c45-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="c4c45-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="c4c45-125">Określa szerokość pasma (w MB/s) dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="c4c45-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="c4c45-126">Należy użyć tylko wtedy, gdy StorageAccountType jest UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="c4c45-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="c4c45-127">Jeśli nie określono tej wartości, przypisze się wartość domyślna na podstawie diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="c4c45-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c45-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c4c45-128">-DiskSizeGB</span></span>
<span data-ttu-id="c4c45-129">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="c4c45-129">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c45-130">-LUN</span><span class="sxs-lookup"><span data-stu-id="c4c45-130">-Lun</span></span>
<span data-ttu-id="c4c45-131">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="c4c45-131">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c45-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4c45-132">-Name</span></span>
<span data-ttu-id="c4c45-133">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="c4c45-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="c4c45-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c4c45-134">-StorageAccountType</span></span>
<span data-ttu-id="c4c45-135">Określa typ konta magazynu na dysku.</span><span class="sxs-lookup"><span data-stu-id="c4c45-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="c4c45-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c4c45-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c4c45-137">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="c4c45-137">Specify the VMSS object.</span></span>
<span data-ttu-id="c4c45-138">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="c4c45-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="c4c45-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="c4c45-139">-WriteAccelerator</span></span>
<span data-ttu-id="c4c45-140">Określa, czy WriteAccelerator ma być włączony, czy wyłączony na dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="c4c45-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="c4c45-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4c45-141">-Confirm</span></span>
<span data-ttu-id="c4c45-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4c45-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4c45-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4c45-143">-WhatIf</span></span>
<span data-ttu-id="c4c45-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4c45-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4c45-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4c45-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4c45-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c45-146">CommonParameters</span></span>
<span data-ttu-id="c4c45-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c45-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c45-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4c45-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c45-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4c45-149">INPUTS</span></span>

### <span data-ttu-id="c4c45-150">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c4c45-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="c4c45-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c4c45-151">System.String</span></span>

### <span data-ttu-id="c4c45-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c4c45-152">System.Int32</span></span>

### <span data-ttu-id="c4c45-153">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. CachingTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="c4c45-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="c4c45-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4c45-154">OUTPUTS</span></span>

### <span data-ttu-id="c4c45-155">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c4c45-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c4c45-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4c45-156">NOTES</span></span>

## <span data-ttu-id="c4c45-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4c45-157">RELATED LINKS</span></span>
