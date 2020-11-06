---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: 0ef680f60f48451e5d5dd9bff730cbfe4ebc9aae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547503"
---
# <span data-ttu-id="b2e93-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="b2e93-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="b2e93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2e93-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e93-103">Dodaje dysk danych do VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2e93-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2e93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2e93-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2e93-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b2e93-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e93-106">Polecenie cmdlet **Add-AzureRmVmssDataDisk** dodaje dysk danych do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b2e93-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b2e93-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2e93-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e93-108">Przykład 1: Dodawanie dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="b2e93-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="b2e93-109">To polecenie dodaje pusty dysk danych do obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2e93-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="b2e93-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2e93-110">PARAMETERS</span></span>

### <span data-ttu-id="b2e93-111">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="b2e93-111">-Caching</span></span>
<span data-ttu-id="b2e93-112">Określa typ buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="b2e93-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="b2e93-113">-Opcja</span><span class="sxs-lookup"><span data-stu-id="b2e93-113">-CreateOption</span></span>
<span data-ttu-id="b2e93-114">Określa opcję tworzenia dysku.</span><span class="sxs-lookup"><span data-stu-id="b2e93-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="b2e93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e93-115">-DefaultProfile</span></span>
<span data-ttu-id="b2e93-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e93-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2e93-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b2e93-117">-DiskSizeGB</span></span>
<span data-ttu-id="b2e93-118">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="b2e93-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="b2e93-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="b2e93-119">-Lun</span></span>
<span data-ttu-id="b2e93-120">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="b2e93-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="b2e93-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2e93-121">-Name</span></span>
<span data-ttu-id="b2e93-122">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="b2e93-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="b2e93-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b2e93-123">-StorageAccountType</span></span>
<span data-ttu-id="b2e93-124">Określa typ konta magazynu na dysku.</span><span class="sxs-lookup"><span data-stu-id="b2e93-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="b2e93-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b2e93-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b2e93-126">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="b2e93-126">Specify the VMSS object.</span></span>
<span data-ttu-id="b2e93-127">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="b2e93-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="b2e93-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b2e93-128">-WriteAccelerator</span></span>
<span data-ttu-id="b2e93-129">Określa, czy WriteAccelerator ma być włączony, czy wyłączony na dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="b2e93-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="b2e93-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2e93-130">-Confirm</span></span>
<span data-ttu-id="b2e93-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e93-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e93-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e93-132">-WhatIf</span></span>
<span data-ttu-id="b2e93-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e93-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e93-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b2e93-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e93-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e93-135">CommonParameters</span></span>
<span data-ttu-id="b2e93-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e93-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e93-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e93-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e93-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2e93-138">INPUTS</span></span>

### <span data-ttu-id="b2e93-139">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b2e93-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b2e93-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e93-140">System.String</span></span>

### <span data-ttu-id="b2e93-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b2e93-141">System.Int32</span></span>

### <span data-ttu-id="b2e93-142">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. CachingTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="b2e93-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b2e93-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2e93-143">OUTPUTS</span></span>

### <span data-ttu-id="b2e93-144">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b2e93-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b2e93-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2e93-145">NOTES</span></span>

## <span data-ttu-id="b2e93-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2e93-146">RELATED LINKS</span></span>
