---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: 53ad88f6e3df11eb3a8f2f9c4b21af40b9ea614b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899367"
---
# <span data-ttu-id="fa787-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fa787-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="fa787-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa787-102">SYNOPSIS</span></span>
<span data-ttu-id="fa787-103">Modyfikuje właściwości dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fa787-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa787-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa787-104">SYNTAX</span></span>

### <span data-ttu-id="fa787-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="fa787-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa787-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="fa787-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa787-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fa787-107">DESCRIPTION</span></span>
<span data-ttu-id="fa787-108">Polecenie cmdlet **Set-AzureRmVMDataDisk** modyfikuje właściwości dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fa787-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="fa787-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa787-109">EXAMPLES</span></span>

### <span data-ttu-id="fa787-110">Przykład 1: modyfikowanie trybu buforowania na dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="fa787-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="fa787-111">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie ContosoVM07 przy użyciu polecenia **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="fa787-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="fa787-112">Polecenie zapisuje je w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="fa787-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="fa787-113">Drugie polecenie modyfikuje tryb buforowania dla dysku danych o nazwie DataDisk01 na maszynie wirtualnej w $VM.</span><span class="sxs-lookup"><span data-stu-id="fa787-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="fa787-114">Polecenie przekazuje wynik do polecenia cmdlet Update-AzureRmVM, które implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="fa787-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="fa787-115">Zmiana w trybie gotówki powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fa787-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="fa787-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa787-116">PARAMETERS</span></span>

### <span data-ttu-id="fa787-117">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="fa787-117">-Caching</span></span>
<span data-ttu-id="fa787-118">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="fa787-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="fa787-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fa787-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa787-120">Odczytu</span><span class="sxs-lookup"><span data-stu-id="fa787-120">ReadOnly</span></span>
- <span data-ttu-id="fa787-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fa787-121">ReadWrite</span></span>

<span data-ttu-id="fa787-122">Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="fa787-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="fa787-123">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fa787-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="fa787-124">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="fa787-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa787-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa787-125">-DefaultProfile</span></span>
<span data-ttu-id="fa787-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa787-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa787-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fa787-127">-DiskSizeInGB</span></span>
<span data-ttu-id="fa787-128">Określa rozmiar dysku danych (w gigabajtach).</span><span class="sxs-lookup"><span data-stu-id="fa787-128">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa787-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="fa787-129">-Lun</span></span>
<span data-ttu-id="fa787-130">Określa logiczny numer jednostki (LUN) dysku danych, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="fa787-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa787-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa787-131">-Name</span></span>
<span data-ttu-id="fa787-132">Określa nazwę dysku danych zmodyfikowanego przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa787-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa787-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="fa787-133">-StorageAccountType</span></span>
<span data-ttu-id="fa787-134">Typ konta dysk zarządzany maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fa787-134">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="fa787-135">-VM</span><span class="sxs-lookup"><span data-stu-id="fa787-135">-VM</span></span>
<span data-ttu-id="fa787-136">Umożliwia określenie maszyny wirtualnej, dla której to polecenie cmdlet modyfikuje dysk danych.</span><span class="sxs-lookup"><span data-stu-id="fa787-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="fa787-137">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="fa787-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa787-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="fa787-138">-WriteAccelerator</span></span>
<span data-ttu-id="fa787-139">Określa, czy WriteAccelerator ma być włączony, czy wyłączony na dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="fa787-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="fa787-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa787-140">CommonParameters</span></span>
<span data-ttu-id="fa787-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa787-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa787-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa787-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa787-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa787-143">INPUTS</span></span>

### <span data-ttu-id="fa787-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fa787-144">PSVirtualMachine</span></span>
<span data-ttu-id="fa787-145">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="fa787-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="fa787-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa787-146">OUTPUTS</span></span>

### <span data-ttu-id="fa787-147">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fa787-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fa787-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa787-148">NOTES</span></span>

## <span data-ttu-id="fa787-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa787-149">RELATED LINKS</span></span>

[<span data-ttu-id="fa787-150">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fa787-150">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="fa787-151">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fa787-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


