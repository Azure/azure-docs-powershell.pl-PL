---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 3c1edb8302ac0921a8f396230637b842d88eab77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717014"
---
# <span data-ttu-id="e8664-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e8664-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="e8664-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8664-102">SYNOPSIS</span></span>
<span data-ttu-id="e8664-103">Usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8664-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8664-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8664-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8664-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8664-105">DESCRIPTION</span></span>
<span data-ttu-id="e8664-106">Polecenie cmdlet **Remove-AzureRmVMDataDisk** usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8664-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="e8664-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8664-107">EXAMPLES</span></span>

### <span data-ttu-id="e8664-108">Przykład 1: usuwanie dysku danych z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e8664-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="e8664-109">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="e8664-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="e8664-110">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e8664-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="e8664-111">Drugie polecenie usuwa dysk danych o nazwie disk3 z maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e8664-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="e8664-112">Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e8664-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="e8664-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8664-113">PARAMETERS</span></span>

### <span data-ttu-id="e8664-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="e8664-114">-DataDiskNames</span></span>
<span data-ttu-id="e8664-115">Określa nazwy jednego lub kilku dysków danych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8664-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8664-116">-VM</span><span class="sxs-lookup"><span data-stu-id="e8664-116">-VM</span></span>
<span data-ttu-id="e8664-117">Określa lokalny obiekt maszyny wirtualnej, z którego ma zostać usunięty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="e8664-117">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="e8664-118">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="e8664-118">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="e8664-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8664-119">-Confirm</span></span>
<span data-ttu-id="e8664-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8664-120">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8664-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8664-121">-WhatIf</span></span>
<span data-ttu-id="e8664-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8664-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8664-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8664-123">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8664-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8664-124">CommonParameters</span></span>
<span data-ttu-id="e8664-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8664-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8664-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8664-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8664-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8664-127">INPUTS</span></span>

### <span data-ttu-id="e8664-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e8664-128">None</span></span>
<span data-ttu-id="e8664-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e8664-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8664-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8664-130">OUTPUTS</span></span>

## <span data-ttu-id="e8664-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8664-131">NOTES</span></span>

## <span data-ttu-id="e8664-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8664-132">RELATED LINKS</span></span>

[<span data-ttu-id="e8664-133">Dodaj-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e8664-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="e8664-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e8664-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


