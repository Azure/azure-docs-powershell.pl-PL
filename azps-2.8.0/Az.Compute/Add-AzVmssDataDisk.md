---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 032c38c3fcc3b09286b795fd3e0efba85e076807
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706479"
---
# <span data-ttu-id="ad329-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="ad329-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="ad329-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad329-102">SYNOPSIS</span></span>
<span data-ttu-id="ad329-103">Dodaje dysk danych do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ad329-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="ad329-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad329-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad329-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad329-105">DESCRIPTION</span></span>
<span data-ttu-id="ad329-106">Polecenie cmdlet **Add-AzVmssDataDisk** dodaje dysk danych do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ad329-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="ad329-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad329-107">EXAMPLES</span></span>

### <span data-ttu-id="ad329-108">Przykład 1: Dodawanie dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="ad329-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="ad329-109">To polecenie dodaje pusty dysk danych do obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="ad329-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="ad329-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad329-110">PARAMETERS</span></span>

### <span data-ttu-id="ad329-111">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="ad329-111">-Caching</span></span>
<span data-ttu-id="ad329-112">Określa typ buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="ad329-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="ad329-113">-Opcja</span><span class="sxs-lookup"><span data-stu-id="ad329-113">-CreateOption</span></span>
<span data-ttu-id="ad329-114">Określa opcję tworzenia dysku.</span><span class="sxs-lookup"><span data-stu-id="ad329-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="ad329-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad329-115">-DefaultProfile</span></span>
<span data-ttu-id="ad329-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad329-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad329-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ad329-117">-DiskSizeGB</span></span>
<span data-ttu-id="ad329-118">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="ad329-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ad329-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="ad329-119">-Lun</span></span>
<span data-ttu-id="ad329-120">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="ad329-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="ad329-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad329-121">-Name</span></span>
<span data-ttu-id="ad329-122">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="ad329-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="ad329-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ad329-123">-StorageAccountType</span></span>
<span data-ttu-id="ad329-124">Określa typ konta magazynu na dysku.</span><span class="sxs-lookup"><span data-stu-id="ad329-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="ad329-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ad329-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ad329-126">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="ad329-126">Specify the VMSS object.</span></span>
<span data-ttu-id="ad329-127">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="ad329-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="ad329-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="ad329-128">-WriteAccelerator</span></span>
<span data-ttu-id="ad329-129">Określa, czy WriteAccelerator ma być włączony, czy wyłączony na dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="ad329-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="ad329-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad329-130">-Confirm</span></span>
<span data-ttu-id="ad329-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad329-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad329-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad329-132">-WhatIf</span></span>
<span data-ttu-id="ad329-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad329-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad329-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad329-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad329-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad329-135">CommonParameters</span></span>
<span data-ttu-id="ad329-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad329-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad329-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad329-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad329-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad329-138">INPUTS</span></span>

### <span data-ttu-id="ad329-139">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ad329-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ad329-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ad329-140">System.String</span></span>

### <span data-ttu-id="ad329-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ad329-141">System.Int32</span></span>

### <span data-ttu-id="ad329-142">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. CachingTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="ad329-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ad329-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad329-143">OUTPUTS</span></span>

### <span data-ttu-id="ad329-144">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ad329-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ad329-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad329-145">NOTES</span></span>

## <span data-ttu-id="ad329-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad329-146">RELATED LINKS</span></span>
