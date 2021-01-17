---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353254"
---
# <span data-ttu-id="3d29f-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="3d29f-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="3d29f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d29f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d29f-103">Dodaje dysk danych do VMSS.</span><span class="sxs-lookup"><span data-stu-id="3d29f-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="3d29f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d29f-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d29f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d29f-105">DESCRIPTION</span></span>
<span data-ttu-id="3d29f-106">Polecenie cmdlet **Add-AzVmssDataDisk** dodaje dysk danych do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3d29f-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="3d29f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d29f-107">EXAMPLES</span></span>

### <span data-ttu-id="3d29f-108">Przykład 1: Dodawanie dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="3d29f-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="3d29f-109">To polecenie dodaje pusty dysk danych do obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="3d29f-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="3d29f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d29f-110">PARAMETERS</span></span>

### <span data-ttu-id="3d29f-111">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="3d29f-111">-Caching</span></span>
<span data-ttu-id="3d29f-112">Określa typ buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="3d29f-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="3d29f-113">-Opcja</span><span class="sxs-lookup"><span data-stu-id="3d29f-113">-CreateOption</span></span>
<span data-ttu-id="3d29f-114">Określa opcję tworzenia dysku.</span><span class="sxs-lookup"><span data-stu-id="3d29f-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="3d29f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d29f-115">-DefaultProfile</span></span>
<span data-ttu-id="3d29f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d29f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d29f-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="3d29f-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="3d29f-118">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanego przez klienta.</span><span class="sxs-lookup"><span data-stu-id="3d29f-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="3d29f-119">Ten parametr może być określony tylko dla dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="3d29f-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="3d29f-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="3d29f-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="3d29f-121">Określa Read-Write IOPS dla zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="3d29f-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="3d29f-122">Należy użyć tylko wtedy, gdy StorageAccountType jest UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="3d29f-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="3d29f-123">Jeśli nie określono tej wartości, przypisze się wartość domyślna na podstawie diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="3d29f-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="3d29f-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="3d29f-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="3d29f-125">Określa szerokość pasma (w MB/s) dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="3d29f-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="3d29f-126">Należy użyć tylko wtedy, gdy StorageAccountType jest UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="3d29f-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="3d29f-127">Jeśli nie określono tej wartości, przypisze się wartość domyślna na podstawie diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="3d29f-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="3d29f-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3d29f-128">-DiskSizeGB</span></span>
<span data-ttu-id="3d29f-129">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="3d29f-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="3d29f-130">-LUN</span><span class="sxs-lookup"><span data-stu-id="3d29f-130">-Lun</span></span>
<span data-ttu-id="3d29f-131">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="3d29f-131">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="3d29f-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d29f-132">-Name</span></span>
<span data-ttu-id="3d29f-133">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="3d29f-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="3d29f-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3d29f-134">-StorageAccountType</span></span>
<span data-ttu-id="3d29f-135">Określa typ konta magazynu na dysku.</span><span class="sxs-lookup"><span data-stu-id="3d29f-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="3d29f-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3d29f-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3d29f-137">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="3d29f-137">Specify the VMSS object.</span></span>
<span data-ttu-id="3d29f-138">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="3d29f-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="3d29f-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="3d29f-139">-WriteAccelerator</span></span>
<span data-ttu-id="3d29f-140">Określa, czy WriteAccelerator ma być włączony, czy wyłączony na dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="3d29f-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="3d29f-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d29f-141">-Confirm</span></span>
<span data-ttu-id="3d29f-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d29f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d29f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d29f-143">-WhatIf</span></span>
<span data-ttu-id="3d29f-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d29f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d29f-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d29f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d29f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d29f-146">CommonParameters</span></span>
<span data-ttu-id="3d29f-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d29f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d29f-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d29f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d29f-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d29f-149">INPUTS</span></span>

### <span data-ttu-id="3d29f-150">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3d29f-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3d29f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3d29f-151">System.String</span></span>

### <span data-ttu-id="3d29f-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3d29f-152">System.Int32</span></span>

### <span data-ttu-id="3d29f-153">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. CachingTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="3d29f-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="3d29f-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d29f-154">OUTPUTS</span></span>

### <span data-ttu-id="3d29f-155">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3d29f-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3d29f-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d29f-156">NOTES</span></span>

## <span data-ttu-id="3d29f-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d29f-157">RELATED LINKS</span></span>
