---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244131"
---
# <span data-ttu-id="5d48b-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5d48b-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="5d48b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d48b-102">SYNOPSIS</span></span>
<span data-ttu-id="5d48b-103">Pokazuje stan szyfrowania dysku maszyn wirtualnych w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5d48b-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="5d48b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5d48b-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d48b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5d48b-105">DESCRIPTION</span></span>
<span data-ttu-id="5d48b-106">Pokazuje stan szyfrowania dysku zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5d48b-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="5d48b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5d48b-107">EXAMPLES</span></span>

### <span data-ttu-id="5d48b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d48b-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="5d48b-109">Pokazuje stan szyfrowania dysku wystąpienia 1 maszyny wirtualnej w zestawie skali maszyny wirtualnej o nazwie MASZYNY WIRTUALNE.001, które należy do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="5d48b-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5d48b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d48b-110">PARAMETERS</span></span>

### <span data-ttu-id="5d48b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d48b-111">-DefaultProfile</span></span>
<span data-ttu-id="5d48b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d48b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d48b-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="5d48b-113">-ExtensionName</span></span>
<span data-ttu-id="5d48b-114">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5d48b-114">The extension name.</span></span>
<span data-ttu-id="5d48b-115">Jeśli ten parametr nie jest określony, wartościami domyślnymi są azureDylogiaDyfrowaniaNaszyfrowaniaNaszycji Dla maszyn wirtualnych systemu Windows i AzureDriveEncryptionForLinux dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="5d48b-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="5d48b-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5d48b-116">-InstanceId</span></span>
<span data-ttu-id="5d48b-117">Określa identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="5d48b-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="5d48b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d48b-118">-ResourceGroupName</span></span>
<span data-ttu-id="5d48b-119">Nazwa grupy zasobów zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5d48b-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5d48b-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5d48b-120">-VMScaleSetName</span></span>
<span data-ttu-id="5d48b-121">Nazwa zestawu skalowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5d48b-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="5d48b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d48b-122">CommonParameters</span></span>
<span data-ttu-id="5d48b-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d48b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d48b-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d48b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d48b-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d48b-125">INPUTS</span></span>

### <span data-ttu-id="5d48b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5d48b-126">System.String</span></span>

## <span data-ttu-id="5d48b-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d48b-127">OUTPUTS</span></span>

### <span data-ttu-id="5d48b-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMGrafiiEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="5d48b-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="5d48b-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5d48b-129">NOTES</span></span>

## <span data-ttu-id="5d48b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d48b-130">RELATED LINKS</span></span>
