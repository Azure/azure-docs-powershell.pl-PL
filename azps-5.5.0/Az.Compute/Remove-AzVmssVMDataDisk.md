---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177490"
---
# <span data-ttu-id="beed1-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="beed1-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="beed1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beed1-102">SYNOPSIS</span></span>
<span data-ttu-id="beed1-103">Usuwa dysk danych z zestawu skalowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="beed1-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="beed1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="beed1-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beed1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="beed1-105">DESCRIPTION</span></span>
<span data-ttu-id="beed1-106">Polecenie **cmdlet Remove-AzVmssVMDataDataLet** usuwa dysk danych z zestawu skalowania MASZYNY WIRTUALNEj</span><span class="sxs-lookup"><span data-stu-id="beed1-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="beed1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="beed1-107">EXAMPLES</span></span>

### <span data-ttu-id="beed1-108">Przykład 1. Usuwanie dysku danych z zestawu skalowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="beed1-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="beed1-109">Pierwsze polecenie getsan istniejącej maszyny wirtualnej maszyny wirtualnej maszyny wirtualnej nadano na przykład nazwę grupy zasobów, nazwę maszyny wirtualnej i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="beed1-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="beed1-110">Drugie polecenie usuwa dysk danych 9 z zestawu skal wirtualnej maszyny wirtualnej przechowywanego w programie $VmssVM Ostateczne polecenie aktualizuje maszyny wirtualnej maszyny wirtualnej o usunięty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="beed1-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="beed1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="beed1-111">PARAMETERS</span></span>

### <span data-ttu-id="beed1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beed1-112">-DefaultProfile</span></span>
<span data-ttu-id="beed1-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="beed1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beed1-114">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="beed1-114">-Lun</span></span>
<span data-ttu-id="beed1-115">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="beed1-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="beed1-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="beed1-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="beed1-117">Skala maszyny wirtualnej ustawia profil maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="beed1-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="beed1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beed1-118">CommonParameters</span></span>
<span data-ttu-id="beed1-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beed1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beed1-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="beed1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beed1-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="beed1-121">INPUTS</span></span>

### <span data-ttu-id="beed1-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="beed1-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="beed1-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="beed1-123">OUTPUTS</span></span>

### <span data-ttu-id="beed1-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="beed1-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="beed1-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="beed1-125">NOTES</span></span>

## <span data-ttu-id="beed1-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="beed1-126">RELATED LINKS</span></span>
