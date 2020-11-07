---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: 1b816e51d93ed375a8b281bba360a103380e9476
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706459"
---
# <span data-ttu-id="b2491-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b2491-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="b2491-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2491-102">SYNOPSIS</span></span>
<span data-ttu-id="b2491-103">Wyłącza szyfrowanie dysków w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b2491-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="b2491-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2491-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2491-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b2491-105">DESCRIPTION</span></span>
<span data-ttu-id="b2491-106">Wyłącza szyfrowanie dysków w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b2491-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="b2491-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2491-107">EXAMPLES</span></span>

### <span data-ttu-id="b2491-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2491-108">Example 1</span></span>
```
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b2491-109">Wyłącza szyfrowanie dysków na zestawie skali maszyny wirtualnej o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="b2491-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="b2491-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2491-110">PARAMETERS</span></span>

### <span data-ttu-id="b2491-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2491-111">-AsJob</span></span>
<span data-ttu-id="b2491-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b2491-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2491-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2491-113">-DefaultProfile</span></span>
<span data-ttu-id="b2491-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2491-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2491-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="b2491-115">-ExtensionName</span></span>
<span data-ttu-id="b2491-116">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b2491-116">The extension name.</span></span>
<span data-ttu-id="b2491-117">Jeśli ten parametr nie zostanie określony, używane są wartości domyślne AzureDiskEncryption dla maszyn wirtualnych i AzureDiskEncryptionForLinux dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="b2491-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="b2491-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b2491-118">-Force</span></span>
<span data-ttu-id="b2491-119">Aby wymusić usunięcie rozszerzenia z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b2491-119">To force the removal of the extension from the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2491-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="b2491-120">-ForceUpdate</span></span>
<span data-ttu-id="b2491-121">Generowanie znacznika dla wymuszenia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="b2491-121">Generate a tag for force update.</span></span>  <span data-ttu-id="b2491-122">Należy to podać w celu wykonania powtarzających się operacji szyfrowania na tej samej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b2491-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2491-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2491-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2491-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2491-124">The resource group name.</span></span>

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

### <span data-ttu-id="b2491-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b2491-125">-VMScaleSetName</span></span>
<span data-ttu-id="b2491-126">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b2491-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="b2491-127">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="b2491-127">-VolumeType</span></span>
<span data-ttu-id="b2491-128">Typ woluminu (system operacyjny lub dane) do wykonania operacji szyfrowania</span><span class="sxs-lookup"><span data-stu-id="b2491-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2491-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2491-129">-Confirm</span></span>
<span data-ttu-id="b2491-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2491-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2491-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2491-131">-WhatIf</span></span>
<span data-ttu-id="b2491-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2491-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2491-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b2491-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2491-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2491-134">CommonParameters</span></span>
<span data-ttu-id="b2491-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2491-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2491-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2491-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2491-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2491-137">INPUTS</span></span>

### <span data-ttu-id="b2491-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b2491-138">System.String</span></span>

### <span data-ttu-id="b2491-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b2491-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b2491-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2491-140">OUTPUTS</span></span>

### <span data-ttu-id="b2491-141">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b2491-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b2491-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2491-142">NOTES</span></span>

## <span data-ttu-id="b2491-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2491-143">RELATED LINKS</span></span>
