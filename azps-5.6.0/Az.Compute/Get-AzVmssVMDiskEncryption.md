---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: a697ead2f971191d108d4fb348a213e35b363d63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994484"
---
# <span data-ttu-id="5a116-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5a116-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="5a116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a116-102">SYNOPSIS</span></span>
<span data-ttu-id="5a116-103">Pokazuje stan szyfrowania dysku maszyn wirtualnych w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a116-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="5a116-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a116-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a116-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a116-105">DESCRIPTION</span></span>
<span data-ttu-id="5a116-106">Pokazuje stan szyfrowania dysku zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a116-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="5a116-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a116-107">EXAMPLES</span></span>

### <span data-ttu-id="5a116-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a116-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="5a116-109">Pokazuje stan szyfrowania dysku wystąpienia maszyny wirtualnej 1 w zestawie skali maszyny wirtualnej o nazwie MASZYNY WIRTUALNE.001, które należy do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="5a116-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5a116-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a116-110">PARAMETERS</span></span>

### <span data-ttu-id="5a116-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a116-111">-DefaultProfile</span></span>
<span data-ttu-id="5a116-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a116-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a116-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="5a116-113">-ExtensionName</span></span>
<span data-ttu-id="5a116-114">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5a116-114">The extension name.</span></span>
<span data-ttu-id="5a116-115">Jeśli ten parametr nie jest określony, wartościami domyślnymi są azureDylogiaDyfrowaniaEncryptionu dla maszyn wirtualnych systemu Windows i AzureDriveEncryptionForLinux dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="5a116-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a116-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5a116-116">-InstanceId</span></span>
<span data-ttu-id="5a116-117">Określa identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="5a116-117">Specifies the instance ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a116-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a116-118">-ResourceGroupName</span></span>
<span data-ttu-id="5a116-119">Nazwa grupy zasobów zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a116-119">Resource group name of the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a116-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5a116-120">-VMScaleSetName</span></span>
<span data-ttu-id="5a116-121">Nazwa zestawu skalowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a116-121">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a116-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a116-122">CommonParameters</span></span>
<span data-ttu-id="5a116-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a116-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a116-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a116-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a116-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a116-125">INPUTS</span></span>

### <span data-ttu-id="5a116-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5a116-126">System.String</span></span>

## <span data-ttu-id="5a116-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a116-127">OUTPUTS</span></span>

### <span data-ttu-id="5a116-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMGrafiiEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="5a116-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="5a116-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a116-129">NOTES</span></span>

## <span data-ttu-id="5a116-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a116-130">RELATED LINKS</span></span>
