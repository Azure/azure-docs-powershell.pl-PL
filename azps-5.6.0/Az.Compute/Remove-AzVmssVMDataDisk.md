---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: c44369915c38219491bd8dfdc1ca288487da27f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971441"
---
# <span data-ttu-id="f9863-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f9863-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="f9863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9863-102">SYNOPSIS</span></span>
<span data-ttu-id="f9863-103">Usuwa dysk danych z zestawu skalowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f9863-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="f9863-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f9863-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9863-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f9863-105">DESCRIPTION</span></span>
<span data-ttu-id="f9863-106">Polecenie **cmdlet Remove-AzVmssVMDataDataLet** usuwa dysk danych z zestawu skalowania MASZYNY WIRTUALNEj</span><span class="sxs-lookup"><span data-stu-id="f9863-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="f9863-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f9863-107">EXAMPLES</span></span>

### <span data-ttu-id="f9863-108">Przykład 1. Usuwanie dysku danych z zestawu skalowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f9863-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="f9863-109">Pierwsze polecenie pobierz istniejące maszyny wirtualnej maszyny wirtualnej maszyny wirtualnej nadano na przykład nazwę grupy zasobów, nazwę maszyny wirtualnej i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="f9863-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="f9863-110">Drugie polecenie usuwa dysk danych 9 z zestawu skal wirtualnej maszyny wirtualnej przechowywanego w programie $VmssVM Ostateczne polecenie aktualizuje maszyny wirtualnej maszyny wirtualnej o usunięty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="f9863-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="f9863-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9863-111">PARAMETERS</span></span>

### <span data-ttu-id="f9863-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9863-112">-DefaultProfile</span></span>
<span data-ttu-id="f9863-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9863-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9863-114">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="f9863-114">-Lun</span></span>
<span data-ttu-id="f9863-115">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="f9863-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9863-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f9863-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="f9863-117">Skala maszyny wirtualnej ustawia profil maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f9863-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9863-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9863-118">CommonParameters</span></span>
<span data-ttu-id="f9863-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9863-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9863-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9863-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9863-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9863-121">INPUTS</span></span>

### <span data-ttu-id="f9863-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f9863-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="f9863-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9863-123">OUTPUTS</span></span>

### <span data-ttu-id="f9863-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f9863-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="f9863-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f9863-125">NOTES</span></span>

## <span data-ttu-id="f9863-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9863-126">RELATED LINKS</span></span>
