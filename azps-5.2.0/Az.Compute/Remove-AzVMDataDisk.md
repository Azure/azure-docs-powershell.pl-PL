---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 6b618511c5d3d8a636fb96fa335314bf3c4ee5bb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363778"
---
# <span data-ttu-id="ffdcd-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ffdcd-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="ffdcd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffdcd-102">SYNOPSIS</span></span>
<span data-ttu-id="ffdcd-103">Usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="ffdcd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffdcd-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffdcd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ffdcd-105">DESCRIPTION</span></span>
<span data-ttu-id="ffdcd-106">Polecenie cmdlet **Remove-AzVMDataDisk** usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="ffdcd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffdcd-107">EXAMPLES</span></span>

### <span data-ttu-id="ffdcd-108">Przykład 1: usuwanie dysku danych z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ffdcd-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="ffdcd-109">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="ffdcd-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="ffdcd-110">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ffdcd-111">Drugie polecenie usuwa dysk danych o nazwie disk3 z maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ffdcd-112">Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="ffdcd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffdcd-113">PARAMETERS</span></span>

### <span data-ttu-id="ffdcd-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="ffdcd-114">-DataDiskNames</span></span>
<span data-ttu-id="ffdcd-115">Określa nazwy jednego lub kilku dysków danych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffdcd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffdcd-116">-DefaultProfile</span></span>
<span data-ttu-id="ffdcd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffdcd-118">-VM</span><span class="sxs-lookup"><span data-stu-id="ffdcd-118">-VM</span></span>
<span data-ttu-id="ffdcd-119">Określa lokalny obiekt maszyny wirtualnej, z którego ma zostać usunięty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="ffdcd-120">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="ffdcd-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ffdcd-121">-Confirm</span></span>
<span data-ttu-id="ffdcd-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffdcd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffdcd-123">-WhatIf</span></span>
<span data-ttu-id="ffdcd-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffdcd-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffdcd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffdcd-126">CommonParameters</span></span>
<span data-ttu-id="ffdcd-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffdcd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffdcd-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffdcd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffdcd-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffdcd-129">INPUTS</span></span>

### <span data-ttu-id="ffdcd-130">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ffdcd-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ffdcd-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffdcd-131">OUTPUTS</span></span>

### <span data-ttu-id="ffdcd-132">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ffdcd-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ffdcd-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffdcd-133">NOTES</span></span>

## <span data-ttu-id="ffdcd-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffdcd-134">RELATED LINKS</span></span>

[<span data-ttu-id="ffdcd-135">Dodaj-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ffdcd-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="ffdcd-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ffdcd-136">Get-AzVM</span></span>](./Get-AzVM.md)


