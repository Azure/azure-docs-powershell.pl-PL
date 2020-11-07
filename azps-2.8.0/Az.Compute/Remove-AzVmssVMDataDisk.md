---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: cd41b7f09bbcf972d28aa38e9c1f4eb622e59b2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706237"
---
# <span data-ttu-id="e941d-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e941d-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="e941d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e941d-102">SYNOPSIS</span></span>
<span data-ttu-id="e941d-103">Usuwa dysk danych z zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e941d-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="e941d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e941d-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e941d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e941d-105">DESCRIPTION</span></span>
<span data-ttu-id="e941d-106">Polecenie cmdlet **Remove-AzVmssVMDataDisk** usuwa dysk danych z maszyny wirtualnej zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e941d-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="e941d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e941d-107">EXAMPLES</span></span>

### <span data-ttu-id="e941d-108">Przykład 1: usuwanie dysku danych z maszyny wirtualnej zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e941d-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="e941d-109">Pierwsze polecenie getsan istniejącą maszynę wirtualną VMSS określoną przez nazwę grupy zasobów, nazwę VMSS i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="e941d-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="e941d-110">Drugie polecenie usuwa z dysku dane numer LUN 0 z maszyny wirtualnej zestawu Skala maszyn wirtualnych przechowywanej w $VmssVM polecenie końcowe aktualizuje VMSS maszyny wirtualnej z usuniętym dyskiem danych.</span><span class="sxs-lookup"><span data-stu-id="e941d-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="e941d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e941d-111">PARAMETERS</span></span>

### <span data-ttu-id="e941d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e941d-112">-DefaultProfile</span></span>
<span data-ttu-id="e941d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e941d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e941d-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="e941d-114">-Lun</span></span>
<span data-ttu-id="e941d-115">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="e941d-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="e941d-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e941d-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="e941d-117">Skala maszyny wirtualnej ustawiona na profil maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e941d-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="e941d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e941d-118">CommonParameters</span></span>
<span data-ttu-id="e941d-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e941d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e941d-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e941d-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e941d-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e941d-121">INPUTS</span></span>

### <span data-ttu-id="e941d-122">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e941d-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="e941d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e941d-123">OUTPUTS</span></span>

### <span data-ttu-id="e941d-124">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e941d-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="e941d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e941d-125">NOTES</span></span>

## <span data-ttu-id="e941d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e941d-126">RELATED LINKS</span></span>
