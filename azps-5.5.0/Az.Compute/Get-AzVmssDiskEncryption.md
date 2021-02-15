---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238860"
---
# <span data-ttu-id="273aa-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="273aa-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="273aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="273aa-102">SYNOPSIS</span></span>
<span data-ttu-id="273aa-103">Pokazuje stan szyfrowania dysku zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="273aa-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="273aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="273aa-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="273aa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="273aa-105">DESCRIPTION</span></span>
<span data-ttu-id="273aa-106">Pokazuje stan szyfrowania dysku zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="273aa-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="273aa-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="273aa-107">EXAMPLES</span></span>

### <span data-ttu-id="273aa-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="273aa-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="273aa-109">Pokazuje stan szyfrowania dysku zestawu skali maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJS001, który należy do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="273aa-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="273aa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="273aa-110">PARAMETERS</span></span>

### <span data-ttu-id="273aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273aa-111">-DefaultProfile</span></span>
<span data-ttu-id="273aa-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="273aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="273aa-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="273aa-113">-ExtensionName</span></span>
<span data-ttu-id="273aa-114">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="273aa-114">The extension name.</span></span>
<span data-ttu-id="273aa-115">Jeśli ten parametr nie jest określony, wartościami domyślnymi są azureDylogiaDyfrowaniaNaszyfrowaniaNaszycji Dla maszyn wirtualnych systemu Windows i AzureDriveEncryptionForLinux dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="273aa-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="273aa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273aa-116">-ResourceGroupName</span></span>
<span data-ttu-id="273aa-117">Nazwa grupy zasobów zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="273aa-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273aa-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="273aa-118">-VMScaleSetName</span></span>
<span data-ttu-id="273aa-119">Nazwa zestawu skalowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="273aa-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273aa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273aa-120">CommonParameters</span></span>
<span data-ttu-id="273aa-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="273aa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273aa-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="273aa-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273aa-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="273aa-123">INPUTS</span></span>

### <span data-ttu-id="273aa-124">System.String</span><span class="sxs-lookup"><span data-stu-id="273aa-124">System.String</span></span>

## <span data-ttu-id="273aa-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="273aa-125">OUTPUTS</span></span>

### <span data-ttu-id="273aa-126">Microsoft.Azure.Commands.Compute.Models.PSVmssGrafiiEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="273aa-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="273aa-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="273aa-127">NOTES</span></span>

## <span data-ttu-id="273aa-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="273aa-128">RELATED LINKS</span></span>
