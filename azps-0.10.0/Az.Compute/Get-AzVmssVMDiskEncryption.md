---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 681ebd8bffda495fcc29087feed1ac45bb77e0f6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893694"
---
# <span data-ttu-id="88243-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="88243-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="88243-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88243-102">SYNOPSIS</span></span>
<span data-ttu-id="88243-103">Przedstawia stan szyfrowania dysków wirtualnych w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88243-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="88243-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88243-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88243-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88243-105">DESCRIPTION</span></span>
<span data-ttu-id="88243-106">Przedstawia stan szyfrowania dysku zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88243-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="88243-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88243-107">EXAMPLES</span></span>

### <span data-ttu-id="88243-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88243-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="88243-109">Przedstawia stan szyfrowania dysku wystąpienia maszyny wirtualnej 1 w zestawie skali maszyny wirtualnej o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="88243-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="88243-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88243-110">PARAMETERS</span></span>

### <span data-ttu-id="88243-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88243-111">-DefaultProfile</span></span>
<span data-ttu-id="88243-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88243-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88243-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="88243-113">-ExtensionName</span></span>
<span data-ttu-id="88243-114">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="88243-114">The extension name.</span></span>
<span data-ttu-id="88243-115">Jeśli ten parametr nie zostanie określony, używane są wartości domyślne AzureDiskEncryption dla maszyn wirtualnych i AzureDiskEncryptionForLinux dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="88243-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="88243-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="88243-116">-InstanceId</span></span>
<span data-ttu-id="88243-117">Określa identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="88243-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="88243-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88243-118">-ResourceGroupName</span></span>
<span data-ttu-id="88243-119">Nazwa grupy zasobów zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88243-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="88243-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="88243-120">-VMScaleSetName</span></span>
<span data-ttu-id="88243-121">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88243-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="88243-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88243-122">CommonParameters</span></span>
<span data-ttu-id="88243-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88243-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88243-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88243-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88243-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88243-125">INPUTS</span></span>

### <span data-ttu-id="88243-126">System. String</span><span class="sxs-lookup"><span data-stu-id="88243-126">System.String</span></span>

## <span data-ttu-id="88243-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88243-127">OUTPUTS</span></span>

### <span data-ttu-id="88243-128">Microsoft. Azure. Commands. COMPUTE. models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="88243-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="88243-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88243-129">NOTES</span></span>

## <span data-ttu-id="88243-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88243-130">RELATED LINKS</span></span>

