---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501901"
---
# <span data-ttu-id="7c92b-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="7c92b-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="7c92b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c92b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c92b-103">Przedstawia stan szyfrowania dysku zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7c92b-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="7c92b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c92b-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c92b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7c92b-105">DESCRIPTION</span></span>
<span data-ttu-id="7c92b-106">Przedstawia stan szyfrowania dysku zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7c92b-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="7c92b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c92b-107">EXAMPLES</span></span>

### <span data-ttu-id="7c92b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7c92b-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="7c92b-109">Zawiera stan szyfrowania dysku zestawu skali maszyny wirtualnej o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="7c92b-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="7c92b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c92b-110">PARAMETERS</span></span>

### <span data-ttu-id="7c92b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c92b-111">-DefaultProfile</span></span>
<span data-ttu-id="7c92b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c92b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c92b-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="7c92b-113">-ExtensionName</span></span>
<span data-ttu-id="7c92b-114">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="7c92b-114">The extension name.</span></span>
<span data-ttu-id="7c92b-115">Jeśli ten parametr nie zostanie określony, używane są wartości domyślne AzureDiskEncryption dla maszyn wirtualnych i AzureDiskEncryptionForLinux dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="7c92b-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="7c92b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c92b-116">-ResourceGroupName</span></span>
<span data-ttu-id="7c92b-117">Nazwa grupy zasobów zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7c92b-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="7c92b-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7c92b-118">-VMScaleSetName</span></span>
<span data-ttu-id="7c92b-119">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7c92b-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="7c92b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c92b-120">CommonParameters</span></span>
<span data-ttu-id="7c92b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c92b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c92b-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c92b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c92b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c92b-123">INPUTS</span></span>

### <span data-ttu-id="7c92b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7c92b-124">System.String</span></span>

## <span data-ttu-id="7c92b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c92b-125">OUTPUTS</span></span>

### <span data-ttu-id="7c92b-126">Microsoft. Azure. Commands. COMPUTE. models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="7c92b-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="7c92b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c92b-127">NOTES</span></span>

## <span data-ttu-id="7c92b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c92b-128">RELATED LINKS</span></span>
