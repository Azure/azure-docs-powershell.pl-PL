---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244210"
---
# <span data-ttu-id="96b83-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="96b83-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="96b83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96b83-102">SYNOPSIS</span></span>
<span data-ttu-id="96b83-103">Dodaje dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="96b83-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="96b83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="96b83-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96b83-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="96b83-105">DESCRIPTION</span></span>
<span data-ttu-id="96b83-106">Polecenie **cmdlet Add-AzVmssDataDataDlet** dodaje dysk danych do wystąpienia zestawu skal maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="96b83-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="96b83-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="96b83-107">EXAMPLES</span></span>

### <span data-ttu-id="96b83-108">Przykład 1. Dodawanie dysku danych</span><span class="sxs-lookup"><span data-stu-id="96b83-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="96b83-109">To polecenie powoduje dodanie pustego dysku danych do obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="96b83-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="96b83-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96b83-110">PARAMETERS</span></span>

### <span data-ttu-id="96b83-111">— buforowanie</span><span class="sxs-lookup"><span data-stu-id="96b83-111">-Caching</span></span>
<span data-ttu-id="96b83-112">Określa typ pamięci buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="96b83-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="96b83-113">— CreateOption</span><span class="sxs-lookup"><span data-stu-id="96b83-113">-CreateOption</span></span>
<span data-ttu-id="96b83-114">Określa opcję tworzenia dysku.</span><span class="sxs-lookup"><span data-stu-id="96b83-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="96b83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b83-115">-DefaultProfile</span></span>
<span data-ttu-id="96b83-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="96b83-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96b83-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="96b83-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="96b83-118">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanych przez klienta.</span><span class="sxs-lookup"><span data-stu-id="96b83-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="96b83-119">Tę wartość można określić tylko dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="96b83-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="96b83-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="96b83-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="96b83-121">Określa Read-Write IOPS dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="96b83-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="96b83-122">Powinien być używany tylko wtedy, gdy typ StorageAccountType UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="96b83-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="96b83-123">Jeśli nie zostanie określona, zostanie przypisana wartość domyślna na podstawie rozmiaru dysku DiskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="96b83-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="96b83-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="96b83-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="96b83-125">Określa przepustowość w MB na sekundę dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="96b83-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="96b83-126">Powinien być używany tylko wtedy, gdy typ StorageAccountType UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="96b83-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="96b83-127">Jeśli nie zostanie określona, zostanie przypisana wartość domyślna na podstawie rozmiaru dysku DiskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="96b83-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="96b83-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="96b83-128">-DiskSizeGB</span></span>
<span data-ttu-id="96b83-129">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="96b83-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="96b83-130">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="96b83-130">-Lun</span></span>
<span data-ttu-id="96b83-131">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="96b83-131">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="96b83-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="96b83-132">-Name</span></span>
<span data-ttu-id="96b83-133">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="96b83-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="96b83-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="96b83-134">-StorageAccountType</span></span>
<span data-ttu-id="96b83-135">Określa typ konta magazynu dysku.</span><span class="sxs-lookup"><span data-stu-id="96b83-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="96b83-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="96b83-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="96b83-137">Określanie obiektu MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="96b83-137">Specify the VMSS object.</span></span>
<span data-ttu-id="96b83-138">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="96b83-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="96b83-139">- WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="96b83-139">-WriteAccelerator</span></span>
<span data-ttu-id="96b83-140">Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na dysku danych.</span><span class="sxs-lookup"><span data-stu-id="96b83-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="96b83-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96b83-141">-Confirm</span></span>
<span data-ttu-id="96b83-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="96b83-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96b83-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96b83-143">-WhatIf</span></span>
<span data-ttu-id="96b83-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96b83-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96b83-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="96b83-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96b83-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b83-146">CommonParameters</span></span>
<span data-ttu-id="96b83-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96b83-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b83-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96b83-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b83-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96b83-149">INPUTS</span></span>

### <span data-ttu-id="96b83-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="96b83-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="96b83-151">System.String</span><span class="sxs-lookup"><span data-stu-id="96b83-151">System.String</span></span>

### <span data-ttu-id="96b83-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="96b83-152">System.Int32</span></span>

### <span data-ttu-id="96b83-153">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="96b83-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="96b83-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96b83-154">OUTPUTS</span></span>

### <span data-ttu-id="96b83-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="96b83-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="96b83-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="96b83-156">NOTES</span></span>

## <span data-ttu-id="96b83-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96b83-157">RELATED LINKS</span></span>
