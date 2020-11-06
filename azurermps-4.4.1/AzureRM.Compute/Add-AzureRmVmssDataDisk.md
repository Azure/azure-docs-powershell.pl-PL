---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: 5e04013ee8f9452ee28cf7975066f512e2eae1c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525705"
---
# <span data-ttu-id="40bda-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="40bda-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="40bda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40bda-102">SYNOPSIS</span></span>
<span data-ttu-id="40bda-103">Dodaje dysk danych do VMSS.</span><span class="sxs-lookup"><span data-stu-id="40bda-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40bda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40bda-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40bda-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40bda-105">DESCRIPTION</span></span>
<span data-ttu-id="40bda-106">Polecenie cmdlet **Add-AzureRmVmssDataDisk** dodaje dysk danych do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="40bda-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="40bda-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40bda-107">EXAMPLES</span></span>

### <span data-ttu-id="40bda-108">Przykład 1: Dodawanie dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="40bda-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="40bda-109">To polecenie dodaje pusty dysk danych do obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="40bda-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="40bda-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40bda-110">PARAMETERS</span></span>

### <span data-ttu-id="40bda-111">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="40bda-111">-Caching</span></span>
<span data-ttu-id="40bda-112">Określa typ buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="40bda-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="40bda-113">-Opcja</span><span class="sxs-lookup"><span data-stu-id="40bda-113">-CreateOption</span></span>
<span data-ttu-id="40bda-114">Określa opcję tworzenia dysku.</span><span class="sxs-lookup"><span data-stu-id="40bda-114">Specifies the create option of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40bda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40bda-115">-DefaultProfile</span></span>
<span data-ttu-id="40bda-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40bda-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40bda-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="40bda-117">-DiskSizeGB</span></span>
<span data-ttu-id="40bda-118">Określa rozmiar dysku w GB.</span><span class="sxs-lookup"><span data-stu-id="40bda-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40bda-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="40bda-119">-Lun</span></span>
<span data-ttu-id="40bda-120">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="40bda-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="40bda-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40bda-121">-Name</span></span>
<span data-ttu-id="40bda-122">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="40bda-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="40bda-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="40bda-123">-StorageAccountType</span></span>
<span data-ttu-id="40bda-124">Określa typ konta magazynu na dysku.</span><span class="sxs-lookup"><span data-stu-id="40bda-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="40bda-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="40bda-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="40bda-126">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="40bda-126">Specify the VMSS object.</span></span>
<span data-ttu-id="40bda-127">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="40bda-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="40bda-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40bda-128">-Confirm</span></span>
<span data-ttu-id="40bda-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40bda-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40bda-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40bda-130">-WhatIf</span></span>
<span data-ttu-id="40bda-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40bda-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40bda-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="40bda-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40bda-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40bda-133">CommonParameters</span></span>
<span data-ttu-id="40bda-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40bda-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40bda-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40bda-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40bda-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40bda-136">INPUTS</span></span>

### <span data-ttu-id="40bda-137">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="40bda-137">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="40bda-138">System. String system. Int32. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. models. DiskCreateOptionTypes; Microsoft. Azure. Management. COMPUTE. platform.................. = Neutral; PublicKeyToken = 31bf3856ad364e35]] system. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. models. StorageAccountTypes, Microsoft. Azure. Management. obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="40bda-138">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="40bda-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40bda-139">OUTPUTS</span></span>

### <span data-ttu-id="40bda-140">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="40bda-140">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="40bda-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40bda-141">NOTES</span></span>

## <span data-ttu-id="40bda-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40bda-142">RELATED LINKS</span></span>

