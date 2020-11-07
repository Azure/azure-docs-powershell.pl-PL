---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 3bc870be1628f5fbf22042155e6a889dbdaadc84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716533"
---
# <span data-ttu-id="aef3d-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="aef3d-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="aef3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aef3d-102">SYNOPSIS</span></span>
<span data-ttu-id="aef3d-103">Modyfikuje właściwości dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aef3d-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aef3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aef3d-104">SYNTAX</span></span>

### <span data-ttu-id="aef3d-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="aef3d-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aef3d-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="aef3d-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aef3d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aef3d-107">DESCRIPTION</span></span>
<span data-ttu-id="aef3d-108">Polecenie cmdlet **Set-AzureRmVMDataDisk** modyfikuje właściwości dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aef3d-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="aef3d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aef3d-109">EXAMPLES</span></span>

### <span data-ttu-id="aef3d-110">Przykład 1: modyfikowanie trybu buforowania na dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="aef3d-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="aef3d-111">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie ContosoVM07 przy użyciu polecenia **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="aef3d-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="aef3d-112">Polecenie zapisuje je w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="aef3d-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="aef3d-113">Drugie polecenie modyfikuje tryb buforowania dla dysku danych o nazwie DataDisk01 na maszynie wirtualnej w $VM.</span><span class="sxs-lookup"><span data-stu-id="aef3d-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="aef3d-114">Polecenie przekazuje wynik do polecenia cmdlet Update-AzureRmVM, które implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="aef3d-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="aef3d-115">Zmiana w trybie gotówki powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aef3d-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="aef3d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aef3d-116">PARAMETERS</span></span>

### <span data-ttu-id="aef3d-117">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="aef3d-117">-Caching</span></span>
<span data-ttu-id="aef3d-118">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="aef3d-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="aef3d-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="aef3d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aef3d-120">Odczytu</span><span class="sxs-lookup"><span data-stu-id="aef3d-120">ReadOnly</span></span>
- <span data-ttu-id="aef3d-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aef3d-121">ReadWrite</span></span>

<span data-ttu-id="aef3d-122">Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="aef3d-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="aef3d-123">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aef3d-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="aef3d-124">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="aef3d-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="aef3d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef3d-125">-DefaultProfile</span></span>
<span data-ttu-id="aef3d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aef3d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aef3d-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="aef3d-127">-DiskSizeInGB</span></span>
<span data-ttu-id="aef3d-128">Określa rozmiar dysku danych (w gigabajtach).</span><span class="sxs-lookup"><span data-stu-id="aef3d-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="aef3d-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="aef3d-129">-Lun</span></span>
<span data-ttu-id="aef3d-130">Określa logiczny numer jednostki (LUN) dysku danych, który jest modyfikowany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="aef3d-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="aef3d-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aef3d-131">-Name</span></span>
<span data-ttu-id="aef3d-132">Określa nazwę dysku danych zmodyfikowanego przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aef3d-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="aef3d-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="aef3d-133">-StorageAccountType</span></span>
<span data-ttu-id="aef3d-134">Typ konta dysk zarządzany maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aef3d-134">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="aef3d-135">-VM</span><span class="sxs-lookup"><span data-stu-id="aef3d-135">-VM</span></span>
<span data-ttu-id="aef3d-136">Umożliwia określenie maszyny wirtualnej, dla której to polecenie cmdlet modyfikuje dysk danych.</span><span class="sxs-lookup"><span data-stu-id="aef3d-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="aef3d-137">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="aef3d-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="aef3d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef3d-138">CommonParameters</span></span>
<span data-ttu-id="aef3d-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef3d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef3d-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aef3d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef3d-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aef3d-141">INPUTS</span></span>

## <span data-ttu-id="aef3d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aef3d-142">OUTPUTS</span></span>

## <span data-ttu-id="aef3d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aef3d-143">NOTES</span></span>

## <span data-ttu-id="aef3d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aef3d-144">RELATED LINKS</span></span>

[<span data-ttu-id="aef3d-145">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aef3d-145">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="aef3d-146">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aef3d-146">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


