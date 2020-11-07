---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 4ed0abb355bf7a755e5acaa36f8bb11e88d80c5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717096"
---
# <span data-ttu-id="44ee6-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="44ee6-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="44ee6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="44ee6-103">Modyfikuje właściwości dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="44ee6-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44ee6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44ee6-104">SYNTAX</span></span>

### <span data-ttu-id="44ee6-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="44ee6-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44ee6-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="44ee6-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44ee6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="44ee6-107">DESCRIPTION</span></span>
<span data-ttu-id="44ee6-108">Polecenie cmdlet **Set-AzureRmVMDataDisk** modyfikuje właściwości dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="44ee6-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="44ee6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44ee6-109">EXAMPLES</span></span>

### <span data-ttu-id="44ee6-110">Przykład 1: modyfikowanie trybu buforowania na dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="44ee6-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="44ee6-111">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie ContosoVM07 przy użyciu polecenia **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="44ee6-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="44ee6-112">Polecenie zapisuje je w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="44ee6-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="44ee6-113">Drugie polecenie modyfikuje tryb buforowania dla dysku danych o nazwie DataDisk01 na maszynie wirtualnej w $VM.</span><span class="sxs-lookup"><span data-stu-id="44ee6-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="44ee6-114">Polecenie przekazuje wynik do polecenia cmdlet Update-AzureRmVM, które implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="44ee6-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="44ee6-115">Zmiana w trybie gotówki powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="44ee6-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="44ee6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44ee6-116">PARAMETERS</span></span>

### <span data-ttu-id="44ee6-117">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="44ee6-117">-Caching</span></span>
<span data-ttu-id="44ee6-118">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="44ee6-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="44ee6-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="44ee6-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="44ee6-120">Odczytu</span><span class="sxs-lookup"><span data-stu-id="44ee6-120">ReadOnly</span></span>
- <span data-ttu-id="44ee6-121">ReadWrite wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="44ee6-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="44ee6-122">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="44ee6-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="44ee6-123">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="44ee6-123">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="44ee6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ee6-124">-DefaultProfile</span></span>
<span data-ttu-id="44ee6-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44ee6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44ee6-126">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="44ee6-126">-DiskSizeInGB</span></span>
<span data-ttu-id="44ee6-127">Określa rozmiar dysku danych (w gigabajtach).</span><span class="sxs-lookup"><span data-stu-id="44ee6-127">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="44ee6-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="44ee6-128">-Lun</span></span>
<span data-ttu-id="44ee6-129">Określa logiczny numer jednostki (LUN) dysku danych, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="44ee6-129">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="44ee6-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44ee6-130">-Name</span></span>
<span data-ttu-id="44ee6-131">Określa nazwę dysku danych zmodyfikowanego przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44ee6-131">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="44ee6-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="44ee6-132">-StorageAccountType</span></span>
<span data-ttu-id="44ee6-133">Typ konta dysk zarządzany maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="44ee6-133">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="44ee6-134">-VM</span><span class="sxs-lookup"><span data-stu-id="44ee6-134">-VM</span></span>
<span data-ttu-id="44ee6-135">Umożliwia określenie maszyny wirtualnej, dla której to polecenie cmdlet modyfikuje dysk danych.</span><span class="sxs-lookup"><span data-stu-id="44ee6-135">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="44ee6-136">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="44ee6-136">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="44ee6-137">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="44ee6-137">-WriteAccelerator</span></span>
<span data-ttu-id="44ee6-138">Określa, czy WriteAccelerator ma być włączony, czy wyłączony na dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="44ee6-138">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="44ee6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ee6-139">CommonParameters</span></span>
<span data-ttu-id="44ee6-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44ee6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ee6-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ee6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ee6-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44ee6-142">INPUTS</span></span>

### <span data-ttu-id="44ee6-143">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="44ee6-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="44ee6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="44ee6-144">System.String</span></span>

### <span data-ttu-id="44ee6-145">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="44ee6-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="44ee6-146">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. CachingTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="44ee6-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="44ee6-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44ee6-147">OUTPUTS</span></span>

### <span data-ttu-id="44ee6-148">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="44ee6-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="44ee6-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44ee6-149">NOTES</span></span>

## <span data-ttu-id="44ee6-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44ee6-150">RELATED LINKS</span></span>

[<span data-ttu-id="44ee6-151">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="44ee6-151">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="44ee6-152">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="44ee6-152">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


