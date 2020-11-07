---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
ms.openlocfilehash: c45574272d814ea899e7d291b729b6a8e6526da6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526954"
---
# <span data-ttu-id="a95d7-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="a95d7-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="a95d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a95d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a95d7-103">Przedstawia stan szyfrowania dysków wirtualnych w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a95d7-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a95d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a95d7-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a95d7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a95d7-105">DESCRIPTION</span></span>
<span data-ttu-id="a95d7-106">Przedstawia stan szyfrowania dysku zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a95d7-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="a95d7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a95d7-107">EXAMPLES</span></span>

### <span data-ttu-id="a95d7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a95d7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="a95d7-109">Przedstawia stan szyfrowania dysku wystąpienia maszyny wirtualnej 1 w zestawie skali maszyny wirtualnej o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="a95d7-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="a95d7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a95d7-110">PARAMETERS</span></span>

### <span data-ttu-id="a95d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95d7-111">-DefaultProfile</span></span>
<span data-ttu-id="a95d7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a95d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95d7-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="a95d7-113">-ExtensionName</span></span>
<span data-ttu-id="a95d7-114">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="a95d7-114">The extension name.</span></span>
<span data-ttu-id="a95d7-115">Jeśli ten parametr nie zostanie określony, używane są wartości domyślne AzureDiskEncryption dla maszyn wirtualnych i AzureDiskEncryptionForLinux dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="a95d7-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95d7-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a95d7-116">-InstanceId</span></span>
<span data-ttu-id="a95d7-117">Określa identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="a95d7-117">Specifies the instance ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95d7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95d7-118">-ResourceGroupName</span></span>
<span data-ttu-id="a95d7-119">Nazwa grupy zasobów zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a95d7-119">Resource group name of the virtual machine scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95d7-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a95d7-120">-VMScaleSetName</span></span>
<span data-ttu-id="a95d7-121">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a95d7-121">The virtual machine scale set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95d7-122">CommonParameters</span></span>
<span data-ttu-id="a95d7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a95d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95d7-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a95d7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95d7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a95d7-125">INPUTS</span></span>

### <span data-ttu-id="a95d7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a95d7-126">System.String</span></span>

## <span data-ttu-id="a95d7-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a95d7-127">OUTPUTS</span></span>

### <span data-ttu-id="a95d7-128">Microsoft. Azure. Commands. COMPUTE. models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="a95d7-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="a95d7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a95d7-129">NOTES</span></span>

## <span data-ttu-id="a95d7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a95d7-130">RELATED LINKS</span></span>