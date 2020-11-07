---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: 032efea1c892905a41dc141e253cd480c3f3bba7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710199"
---
# <span data-ttu-id="89e48-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="89e48-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="89e48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89e48-102">SYNOPSIS</span></span>
<span data-ttu-id="89e48-103">Modyfikuje właściwości dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89e48-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="89e48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89e48-104">SYNTAX</span></span>

### <span data-ttu-id="89e48-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="89e48-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89e48-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="89e48-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89e48-107">Opis</span><span class="sxs-lookup"><span data-stu-id="89e48-107">DESCRIPTION</span></span>
<span data-ttu-id="89e48-108">Polecenie cmdlet **Set-AzVMDataDisk** modyfikuje właściwości dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89e48-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="89e48-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89e48-109">EXAMPLES</span></span>

### <span data-ttu-id="89e48-110">Przykład 1: modyfikowanie trybu buforowania na dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="89e48-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="89e48-111">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie ContosoVM07 przy użyciu polecenia **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="89e48-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="89e48-112">Polecenie zapisuje je w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="89e48-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="89e48-113">Drugie polecenie modyfikuje tryb buforowania dla dysku danych o nazwie DataDisk01 na maszynie wirtualnej w $VM.</span><span class="sxs-lookup"><span data-stu-id="89e48-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="89e48-114">Polecenie przekazuje wynik do polecenia cmdlet Update-AzVM, które implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="89e48-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="89e48-115">Zmiana w trybie gotówki powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89e48-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="89e48-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89e48-116">PARAMETERS</span></span>

### <span data-ttu-id="89e48-117">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="89e48-117">-Caching</span></span>
<span data-ttu-id="89e48-118">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="89e48-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="89e48-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="89e48-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89e48-120">Odczytu</span><span class="sxs-lookup"><span data-stu-id="89e48-120">ReadOnly</span></span>
- <span data-ttu-id="89e48-121">ReadWrite wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="89e48-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="89e48-122">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89e48-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="89e48-123">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="89e48-123">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e48-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e48-124">-DefaultProfile</span></span>
<span data-ttu-id="89e48-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89e48-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89e48-126">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="89e48-126">-DiskSizeInGB</span></span>
<span data-ttu-id="89e48-127">Określa rozmiar dysku danych (w gigabajtach).</span><span class="sxs-lookup"><span data-stu-id="89e48-127">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e48-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="89e48-128">-Lun</span></span>
<span data-ttu-id="89e48-129">Określa logiczny numer jednostki (LUN) dysku danych, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="89e48-129">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e48-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89e48-130">-Name</span></span>
<span data-ttu-id="89e48-131">Określa nazwę dysku danych zmodyfikowanego przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89e48-131">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e48-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="89e48-132">-StorageAccountType</span></span>
<span data-ttu-id="89e48-133">Typ konta dysk zarządzany maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89e48-133">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="89e48-134">-VM</span><span class="sxs-lookup"><span data-stu-id="89e48-134">-VM</span></span>
<span data-ttu-id="89e48-135">Umożliwia określenie maszyny wirtualnej, dla której to polecenie cmdlet modyfikuje dysk danych.</span><span class="sxs-lookup"><span data-stu-id="89e48-135">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="89e48-136">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="89e48-136">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89e48-137">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="89e48-137">-WriteAccelerator</span></span>
<span data-ttu-id="89e48-138">Określa, czy WriteAccelerator ma być włączony, czy wyłączony na dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="89e48-138">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="89e48-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e48-139">CommonParameters</span></span>
<span data-ttu-id="89e48-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e48-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e48-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e48-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e48-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89e48-142">INPUTS</span></span>

### <span data-ttu-id="89e48-143">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="89e48-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="89e48-144">System. String</span><span class="sxs-lookup"><span data-stu-id="89e48-144">System.String</span></span>

### <span data-ttu-id="89e48-145">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="89e48-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="89e48-146">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. CachingTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="89e48-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="89e48-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89e48-147">OUTPUTS</span></span>

### <span data-ttu-id="89e48-148">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="89e48-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="89e48-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89e48-149">NOTES</span></span>

## <span data-ttu-id="89e48-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89e48-150">RELATED LINKS</span></span>

[<span data-ttu-id="89e48-151">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="89e48-151">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="89e48-152">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="89e48-152">Update-AzVM</span></span>](./Update-AzVM.md)


