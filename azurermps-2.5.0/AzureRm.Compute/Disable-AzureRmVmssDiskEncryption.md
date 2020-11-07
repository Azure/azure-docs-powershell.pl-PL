---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
ms.openlocfilehash: b130be059432a6ca21fb0c1669660ebed34c670e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898999"
---
# <span data-ttu-id="cae3e-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="cae3e-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="cae3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cae3e-102">SYNOPSIS</span></span>
<span data-ttu-id="cae3e-103">Wyłącza szyfrowanie dysków w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cae3e-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cae3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cae3e-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae3e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cae3e-105">DESCRIPTION</span></span>
<span data-ttu-id="cae3e-106">Wyłącza szyfrowanie dysków w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cae3e-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="cae3e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cae3e-107">EXAMPLES</span></span>

### <span data-ttu-id="cae3e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cae3e-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="cae3e-109">Wyłącza szyfrowanie dysków na zestawie skali maszyny wirtualnej o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="cae3e-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="cae3e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cae3e-110">PARAMETERS</span></span>

### <span data-ttu-id="cae3e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cae3e-111">-AsJob</span></span>
<span data-ttu-id="cae3e-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cae3e-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae3e-113">-DefaultProfile</span></span>
<span data-ttu-id="cae3e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cae3e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cae3e-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="cae3e-115">-ExtensionName</span></span>
<span data-ttu-id="cae3e-116">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="cae3e-116">The extension name.</span></span>
<span data-ttu-id="cae3e-117">Jeśli ten parametr nie zostanie określony, używane są wartości domyślne AzureDiskEncryption dla maszyn wirtualnych i AzureDiskEncryptionForLinux dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="cae3e-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="cae3e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cae3e-118">-Force</span></span>
<span data-ttu-id="cae3e-119">Aby wymusić usunięcie rozszerzenia z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cae3e-119">To force the removal of the extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae3e-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="cae3e-120">-ForceUpdate</span></span>
<span data-ttu-id="cae3e-121">Generowanie znacznika dla wymuszenia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="cae3e-121">Generate a tag for force update.</span></span>  <span data-ttu-id="cae3e-122">Należy to podać w celu wykonania powtarzających się operacji szyfrowania na tej samej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cae3e-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae3e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae3e-123">-ResourceGroupName</span></span>
<span data-ttu-id="cae3e-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cae3e-124">The resource group name.</span></span>

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

### <span data-ttu-id="cae3e-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cae3e-125">-VMScaleSetName</span></span>
<span data-ttu-id="cae3e-126">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cae3e-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="cae3e-127">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="cae3e-127">-VolumeType</span></span>
<span data-ttu-id="cae3e-128">Typ woluminu (system operacyjny lub dane) do wykonania operacji szyfrowania</span><span class="sxs-lookup"><span data-stu-id="cae3e-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae3e-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cae3e-129">-Confirm</span></span>
<span data-ttu-id="cae3e-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae3e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae3e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae3e-131">-WhatIf</span></span>
<span data-ttu-id="cae3e-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae3e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cae3e-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cae3e-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae3e-134">CommonParameters</span></span>
<span data-ttu-id="cae3e-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae3e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cae3e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae3e-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cae3e-137">INPUTS</span></span>

### <span data-ttu-id="cae3e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cae3e-138">System.String</span></span>

## <span data-ttu-id="cae3e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cae3e-139">OUTPUTS</span></span>

### <span data-ttu-id="cae3e-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cae3e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cae3e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cae3e-141">NOTES</span></span>

## <span data-ttu-id="cae3e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cae3e-142">RELATED LINKS</span></span>

