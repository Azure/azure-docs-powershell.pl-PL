---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 72ccf9994b303e9e191594f32bb2aa23f0abd9ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983290"
---
# <span data-ttu-id="f57c3-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f57c3-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="f57c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f57c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f57c3-103">Usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f57c3-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="f57c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f57c3-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f57c3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f57c3-105">DESCRIPTION</span></span>
<span data-ttu-id="f57c3-106">Polecenie **cmdlet Remove-AzVMDataData usuwa** dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f57c3-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="f57c3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f57c3-107">EXAMPLES</span></span>

### <span data-ttu-id="f57c3-108">Przykład 1. Usuwanie dysku danych z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f57c3-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="f57c3-109">Pierwsze polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="f57c3-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="f57c3-110">Polecenie przechowuje maszynę wirtualną w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="f57c3-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f57c3-111">Drugie polecenie usuwa dysk danych o nazwie Dysk3 z maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f57c3-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="f57c3-112">Ostatnie polecenie aktualizuje stan maszyny wirtualnej przechowywanej w u $VirtualMachine ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f57c3-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="f57c3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f57c3-113">PARAMETERS</span></span>

### <span data-ttu-id="f57c3-114">-DataNames</span><span class="sxs-lookup"><span data-stu-id="f57c3-114">-DataDiskNames</span></span>
<span data-ttu-id="f57c3-115">Określa nazwy dysków z danymi, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57c3-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f57c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f57c3-116">-DefaultProfile</span></span>
<span data-ttu-id="f57c3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f57c3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f57c3-118">— MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="f57c3-118">-VM</span></span>
<span data-ttu-id="f57c3-119">Określa lokalny obiekt maszyny wirtualnej, z którego ma być usuwany dysk danych.</span><span class="sxs-lookup"><span data-stu-id="f57c3-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="f57c3-120">Aby uzyskać obiekt maszyny wirtualnej, użyj Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57c3-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="f57c3-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f57c3-121">-Confirm</span></span>
<span data-ttu-id="f57c3-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f57c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f57c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f57c3-123">-WhatIf</span></span>
<span data-ttu-id="f57c3-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57c3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f57c3-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f57c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f57c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f57c3-126">CommonParameters</span></span>
<span data-ttu-id="f57c3-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f57c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f57c3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f57c3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f57c3-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f57c3-129">INPUTS</span></span>

### <span data-ttu-id="f57c3-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f57c3-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f57c3-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f57c3-131">OUTPUTS</span></span>

### <span data-ttu-id="f57c3-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f57c3-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f57c3-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f57c3-133">NOTES</span></span>

## <span data-ttu-id="f57c3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f57c3-134">RELATED LINKS</span></span>

[<span data-ttu-id="f57c3-135">Add-AzVMDataData</span><span class="sxs-lookup"><span data-stu-id="f57c3-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="f57c3-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f57c3-136">Get-AzVM</span></span>](./Get-AzVM.md)


