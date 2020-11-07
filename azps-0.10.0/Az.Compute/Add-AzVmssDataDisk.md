---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: c1a1b95dcaa06d922b0357d0e9e6a1b75fa7d793
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893870"
---
# <span data-ttu-id="e7a05-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="e7a05-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="e7a05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7a05-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a05-103">Dodaje dysk danych do VMSS.</span><span class="sxs-lookup"><span data-stu-id="e7a05-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="e7a05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7a05-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <DiskCreateOptionTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a05-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e7a05-105">DESCRIPTION</span></span>
<span data-ttu-id="e7a05-106">Polecenie cmdlet **Add-AzVmssDataDisk** dodaje dysk danych do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e7a05-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="e7a05-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7a05-107">EXAMPLES</span></span>

### <span data-ttu-id="e7a05-108">Przykład 1: Dodawanie dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="e7a05-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="e7a05-109">To polecenie dodaje pusty dysk danych do obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="e7a05-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="e7a05-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7a05-110">PARAMETERS</span></span>

### <span data-ttu-id="e7a05-111">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="e7a05-111">-Caching</span></span>
<span data-ttu-id="e7a05-112">Określa typ buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e7a05-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a05-113">-Opcja</span><span class="sxs-lookup"><span data-stu-id="e7a05-113">-CreateOption</span></span>
<span data-ttu-id="e7a05-114">Określa opcję tworzenia dysku.</span><span class="sxs-lookup"><span data-stu-id="e7a05-114">Specifies the create option of the disk.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a05-115">-DefaultProfile</span></span>
<span data-ttu-id="e7a05-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7a05-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7a05-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e7a05-117">-DiskSizeGB</span></span>
<span data-ttu-id="e7a05-118">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="e7a05-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a05-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="e7a05-119">-Lun</span></span>
<span data-ttu-id="e7a05-120">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="e7a05-120">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a05-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7a05-121">-Name</span></span>
<span data-ttu-id="e7a05-122">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="e7a05-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="e7a05-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e7a05-123">-StorageAccountType</span></span>
<span data-ttu-id="e7a05-124">Określa typ konta magazynu na dysku.</span><span class="sxs-lookup"><span data-stu-id="e7a05-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="e7a05-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7a05-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e7a05-126">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="e7a05-126">Specify the VMSS object.</span></span>
<span data-ttu-id="e7a05-127">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="e7a05-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a05-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e7a05-128">-WriteAccelerator</span></span>
<span data-ttu-id="e7a05-129">Określa, czy WriteAccelerator ma być włączony, czy wyłączony na dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="e7a05-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a05-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7a05-130">-Confirm</span></span>
<span data-ttu-id="e7a05-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a05-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a05-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a05-132">-WhatIf</span></span>
<span data-ttu-id="e7a05-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a05-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a05-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7a05-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a05-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a05-135">CommonParameters</span></span>
<span data-ttu-id="e7a05-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a05-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a05-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7a05-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a05-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7a05-138">INPUTS</span></span>

### <span data-ttu-id="e7a05-139">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7a05-139">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="e7a05-140">System. String system. Int32. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. models. DiskCreateOptionTypes; Microsoft. Azure. Management. COMPUTE. platform.................. = Neutral; PublicKeyToken = 31bf3856ad364e35]] system. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. models. StorageAccountTypes, Microsoft. Azure. Management. obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="e7a05-140">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="e7a05-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7a05-141">OUTPUTS</span></span>

### <span data-ttu-id="e7a05-142">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7a05-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="e7a05-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7a05-143">NOTES</span></span>

## <span data-ttu-id="e7a05-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7a05-144">RELATED LINKS</span></span>

