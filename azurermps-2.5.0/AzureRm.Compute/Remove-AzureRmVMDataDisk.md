---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: ea8b069be4b153e6e4ca295a917e1c3e81629094
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898794"
---
# <span data-ttu-id="b47e4-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b47e4-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="b47e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b47e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b47e4-103">Usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b47e4-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b47e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b47e4-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b47e4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b47e4-105">DESCRIPTION</span></span>
<span data-ttu-id="b47e4-106">Polecenie cmdlet **Remove-AzureRmVMDataDisk** usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b47e4-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="b47e4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b47e4-107">EXAMPLES</span></span>

### <span data-ttu-id="b47e4-108">Przykład 1: usuwanie dysku danych z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b47e4-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="b47e4-109">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="b47e4-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="b47e4-110">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b47e4-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="b47e4-111">Drugie polecenie usuwa dysk danych o nazwie disk3 z maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b47e4-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="b47e4-112">Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b47e4-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="b47e4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b47e4-113">PARAMETERS</span></span>

### <span data-ttu-id="b47e4-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="b47e4-114">-DataDiskNames</span></span>
<span data-ttu-id="b47e4-115">Określa nazwy jednego lub kilku dysków danych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b47e4-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b47e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47e4-116">-DefaultProfile</span></span>
<span data-ttu-id="b47e4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b47e4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b47e4-118">-VM</span><span class="sxs-lookup"><span data-stu-id="b47e4-118">-VM</span></span>
<span data-ttu-id="b47e4-119">Określa lokalny obiekt maszyny wirtualnej, z którego ma zostać usunięty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="b47e4-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="b47e4-120">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="b47e4-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="b47e4-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b47e4-121">-Confirm</span></span>
<span data-ttu-id="b47e4-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b47e4-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="b47e4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b47e4-123">-WhatIf</span></span>
<span data-ttu-id="b47e4-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b47e4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b47e4-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b47e4-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="b47e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47e4-126">CommonParameters</span></span>
<span data-ttu-id="b47e4-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b47e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47e4-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b47e4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47e4-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b47e4-129">INPUTS</span></span>

### <span data-ttu-id="b47e4-130">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b47e4-130">PSVirtualMachine</span></span>
<span data-ttu-id="b47e4-131">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="b47e4-131">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="b47e4-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b47e4-132">OUTPUTS</span></span>

### <span data-ttu-id="b47e4-133">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b47e4-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b47e4-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b47e4-134">NOTES</span></span>

## <span data-ttu-id="b47e4-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b47e4-135">RELATED LINKS</span></span>

[<span data-ttu-id="b47e4-136">Dodaj-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b47e4-136">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="b47e4-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b47e4-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


