---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548180"
---
# <span data-ttu-id="57248-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="57248-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="57248-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57248-102">SYNOPSIS</span></span>
<span data-ttu-id="57248-103">Modyfikuje właściwości dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57248-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57248-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57248-104">SYNTAX</span></span>

### <span data-ttu-id="57248-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="57248-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="57248-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="57248-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="57248-107">Opis</span><span class="sxs-lookup"><span data-stu-id="57248-107">DESCRIPTION</span></span>
<span data-ttu-id="57248-108">Polecenie cmdlet **Set-AzureRmVMDataDisk** modyfikuje właściwości dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57248-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="57248-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57248-109">EXAMPLES</span></span>

### <span data-ttu-id="57248-110">Przykład 1: modyfikowanie trybu buforowania na dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="57248-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="57248-111">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie ContosoVM07 przy użyciu polecenia **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="57248-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="57248-112">Polecenie zapisuje je w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="57248-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="57248-113">Drugie polecenie modyfikuje tryb buforowania dla dysku danych o nazwie DataDisk01 na maszynie wirtualnej w $VM.</span><span class="sxs-lookup"><span data-stu-id="57248-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="57248-114">Polecenie przekazuje wynik do polecenia cmdlet Update-AzureRmVM, które implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="57248-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="57248-115">Zmiana trybu buforowania powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57248-115">A change to the caching mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="57248-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57248-116">PARAMETERS</span></span>

### <span data-ttu-id="57248-117">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="57248-117">-Caching</span></span>
<span data-ttu-id="57248-118">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="57248-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="57248-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="57248-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57248-120">Odczytu</span><span class="sxs-lookup"><span data-stu-id="57248-120">ReadOnly</span></span>
- <span data-ttu-id="57248-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="57248-121">ReadWrite</span></span>

<span data-ttu-id="57248-122">Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="57248-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="57248-123">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57248-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="57248-124">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="57248-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="57248-125">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="57248-125">-DiskSizeInGB</span></span>
<span data-ttu-id="57248-126">Określa rozmiar dysku danych (w gigabajtach).</span><span class="sxs-lookup"><span data-stu-id="57248-126">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="57248-127">-LUN</span><span class="sxs-lookup"><span data-stu-id="57248-127">-Lun</span></span>
<span data-ttu-id="57248-128">Określa logiczny numer jednostki (LUN) dysku danych, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="57248-128">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="57248-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57248-129">-Name</span></span>
<span data-ttu-id="57248-130">Określa nazwę dysku danych zmodyfikowanego przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57248-130">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="57248-131">-VM</span><span class="sxs-lookup"><span data-stu-id="57248-131">-VM</span></span>
<span data-ttu-id="57248-132">Umożliwia określenie maszyny wirtualnej, dla której to polecenie cmdlet modyfikuje dysk danych.</span><span class="sxs-lookup"><span data-stu-id="57248-132">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="57248-133">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="57248-133">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="57248-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57248-134">CommonParameters</span></span>
<span data-ttu-id="57248-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57248-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57248-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57248-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57248-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57248-137">INPUTS</span></span>

### <span data-ttu-id="57248-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="57248-138">None</span></span>
<span data-ttu-id="57248-139">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="57248-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57248-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57248-140">OUTPUTS</span></span>

## <span data-ttu-id="57248-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57248-141">NOTES</span></span>

## <span data-ttu-id="57248-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57248-142">RELATED LINKS</span></span>

[<span data-ttu-id="57248-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="57248-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="57248-144">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="57248-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


