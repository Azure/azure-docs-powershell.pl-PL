---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342082"
---
# <span data-ttu-id="4a946-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4a946-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="4a946-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a946-102">SYNOPSIS</span></span>
<span data-ttu-id="4a946-103">Przedstawia stan szyfrowania dysku zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4a946-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="4a946-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a946-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a946-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4a946-105">DESCRIPTION</span></span>
<span data-ttu-id="4a946-106">Przedstawia stan szyfrowania dysku zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4a946-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="4a946-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a946-107">EXAMPLES</span></span>

### <span data-ttu-id="4a946-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a946-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="4a946-109">Zawiera stan szyfrowania dysku zestawu skali maszyny wirtualnej o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="4a946-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="4a946-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a946-110">PARAMETERS</span></span>

### <span data-ttu-id="4a946-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a946-111">-DefaultProfile</span></span>
<span data-ttu-id="4a946-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a946-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a946-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="4a946-113">-ExtensionName</span></span>
<span data-ttu-id="4a946-114">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="4a946-114">The extension name.</span></span>
<span data-ttu-id="4a946-115">Jeśli ten parametr nie zostanie określony, używane są wartości domyślne AzureDiskEncryption dla maszyn wirtualnych i AzureDiskEncryptionForLinux dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="4a946-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="4a946-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a946-116">-ResourceGroupName</span></span>
<span data-ttu-id="4a946-117">Nazwa grupy zasobów zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4a946-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="4a946-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4a946-118">-VMScaleSetName</span></span>
<span data-ttu-id="4a946-119">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4a946-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="4a946-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a946-120">CommonParameters</span></span>
<span data-ttu-id="4a946-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a946-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a946-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a946-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a946-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a946-123">INPUTS</span></span>

### <span data-ttu-id="4a946-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4a946-124">System.String</span></span>

## <span data-ttu-id="4a946-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a946-125">OUTPUTS</span></span>

### <span data-ttu-id="4a946-126">Microsoft. Azure. Commands. COMPUTE. models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="4a946-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="4a946-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a946-127">NOTES</span></span>

## <span data-ttu-id="4a946-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a946-128">RELATED LINKS</span></span>
