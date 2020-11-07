---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: e2eca141678c5455df0e443c155693c3c1445e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717341"
---
# <span data-ttu-id="41c4a-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="41c4a-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="41c4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="41c4a-103">Dodaje dysk danych do VMSS.</span><span class="sxs-lookup"><span data-stu-id="41c4a-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41c4a-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41c4a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="41c4a-106">Polecenie cmdlet **Add-AzureRmVmssDataDisk** dodaje dysk danych do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="41c4a-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="41c4a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41c4a-107">EXAMPLES</span></span>

### <span data-ttu-id="41c4a-108">Przykład 1: Dodawanie dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="41c4a-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="41c4a-109">To polecenie dodaje pusty dysk danych do obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="41c4a-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="41c4a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41c4a-110">PARAMETERS</span></span>

### <span data-ttu-id="41c4a-111">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="41c4a-111">-Caching</span></span>
<span data-ttu-id="41c4a-112">Określa typ buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="41c4a-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="41c4a-113">-Opcja</span><span class="sxs-lookup"><span data-stu-id="41c4a-113">-CreateOption</span></span>
<span data-ttu-id="41c4a-114">Określa opcję tworzenia dysku.</span><span class="sxs-lookup"><span data-stu-id="41c4a-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="41c4a-115">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="41c4a-115">-DiskSizeGB</span></span>
<span data-ttu-id="41c4a-116">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="41c4a-116">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="41c4a-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="41c4a-117">-Lun</span></span>
<span data-ttu-id="41c4a-118">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="41c4a-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="41c4a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41c4a-119">-Name</span></span>
<span data-ttu-id="41c4a-120">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="41c4a-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="41c4a-121">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="41c4a-121">-StorageAccountType</span></span>
<span data-ttu-id="41c4a-122">Określa typ konta magazynu na dysku.</span><span class="sxs-lookup"><span data-stu-id="41c4a-122">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="41c4a-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="41c4a-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="41c4a-124">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="41c4a-124">Specify the VMSS object.</span></span>
<span data-ttu-id="41c4a-125">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="41c4a-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="41c4a-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41c4a-126">-Confirm</span></span>
<span data-ttu-id="41c4a-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41c4a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c4a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c4a-128">-WhatIf</span></span>
<span data-ttu-id="41c4a-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41c4a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c4a-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41c4a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c4a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c4a-131">CommonParameters</span></span>
<span data-ttu-id="41c4a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c4a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c4a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41c4a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c4a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41c4a-134">INPUTS</span></span>

### <span data-ttu-id="41c4a-135">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="41c4a-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="41c4a-136">System. String system. Int32. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. models. DiskCreateOptionTypes; Microsoft. Azure. Management. COMPUTE. platform.................. = Neutral; PublicKeyToken = 31bf3856ad364e35]] system. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. models. StorageAccountTypes, Microsoft. Azure. Management. obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="41c4a-136">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="41c4a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41c4a-137">OUTPUTS</span></span>

### <span data-ttu-id="41c4a-138">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="41c4a-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="41c4a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41c4a-139">NOTES</span></span>

## <span data-ttu-id="41c4a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41c4a-140">RELATED LINKS</span></span>
