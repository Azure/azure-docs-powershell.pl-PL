---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 3529ca1d26504558036f3496c9bc75ec10e666ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893529"
---
# <span data-ttu-id="afaa9-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="afaa9-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="afaa9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afaa9-102">SYNOPSIS</span></span>
<span data-ttu-id="afaa9-103">Usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="afaa9-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="afaa9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afaa9-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afaa9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="afaa9-105">DESCRIPTION</span></span>
<span data-ttu-id="afaa9-106">Polecenie cmdlet **Remove-AzVMDataDisk** usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="afaa9-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="afaa9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afaa9-107">EXAMPLES</span></span>

### <span data-ttu-id="afaa9-108">Przykład 1: usuwanie dysku danych z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="afaa9-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="afaa9-109">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="afaa9-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="afaa9-110">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="afaa9-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="afaa9-111">Drugie polecenie usuwa dysk danych o nazwie disk3 z maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="afaa9-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="afaa9-112">Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="afaa9-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="afaa9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afaa9-113">PARAMETERS</span></span>

### <span data-ttu-id="afaa9-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="afaa9-114">-DataDiskNames</span></span>
<span data-ttu-id="afaa9-115">Określa nazwy jednego lub kilku dysków danych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afaa9-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="afaa9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afaa9-116">-DefaultProfile</span></span>
<span data-ttu-id="afaa9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="afaa9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afaa9-118">-VM</span><span class="sxs-lookup"><span data-stu-id="afaa9-118">-VM</span></span>
<span data-ttu-id="afaa9-119">Określa lokalny obiekt maszyny wirtualnej, z którego ma zostać usunięty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="afaa9-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="afaa9-120">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="afaa9-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="afaa9-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="afaa9-121">-Confirm</span></span>
<span data-ttu-id="afaa9-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afaa9-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="afaa9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afaa9-123">-WhatIf</span></span>
<span data-ttu-id="afaa9-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afaa9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afaa9-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="afaa9-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="afaa9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afaa9-126">CommonParameters</span></span>
<span data-ttu-id="afaa9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afaa9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afaa9-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afaa9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afaa9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afaa9-129">INPUTS</span></span>

### <span data-ttu-id="afaa9-130">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="afaa9-130">PSVirtualMachine</span></span>
<span data-ttu-id="afaa9-131">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="afaa9-131">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="afaa9-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afaa9-132">OUTPUTS</span></span>

### <span data-ttu-id="afaa9-133">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="afaa9-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="afaa9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afaa9-134">NOTES</span></span>

## <span data-ttu-id="afaa9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afaa9-135">RELATED LINKS</span></span>

[<span data-ttu-id="afaa9-136">Dodaj-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="afaa9-136">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="afaa9-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="afaa9-137">Get-AzVM</span></span>](./Get-AzVM.md)


