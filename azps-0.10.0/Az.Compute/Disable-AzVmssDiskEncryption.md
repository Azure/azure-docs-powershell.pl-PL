---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: 43a8f6efc69113888454511faa346aea7baa837a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893830"
---
# <span data-ttu-id="80553-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="80553-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="80553-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80553-102">SYNOPSIS</span></span>
<span data-ttu-id="80553-103">Wyłącza szyfrowanie dysków w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80553-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="80553-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80553-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80553-105">Opis</span><span class="sxs-lookup"><span data-stu-id="80553-105">DESCRIPTION</span></span>
<span data-ttu-id="80553-106">Wyłącza szyfrowanie dysków w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80553-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="80553-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80553-107">EXAMPLES</span></span>

### <span data-ttu-id="80553-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80553-108">Example 1</span></span>
```
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="80553-109">Wyłącza szyfrowanie dysków na zestawie skali maszyny wirtualnej o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="80553-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="80553-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80553-110">PARAMETERS</span></span>

### <span data-ttu-id="80553-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80553-111">-AsJob</span></span>
<span data-ttu-id="80553-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="80553-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80553-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80553-113">-DefaultProfile</span></span>
<span data-ttu-id="80553-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80553-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80553-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="80553-115">-ExtensionName</span></span>
<span data-ttu-id="80553-116">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="80553-116">The extension name.</span></span>
<span data-ttu-id="80553-117">Jeśli ten parametr nie zostanie określony, używane są wartości domyślne AzureDiskEncryption dla maszyn wirtualnych i AzureDiskEncryptionForLinux dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="80553-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="80553-118">-Force</span><span class="sxs-lookup"><span data-stu-id="80553-118">-Force</span></span>
<span data-ttu-id="80553-119">Aby wymusić usunięcie rozszerzenia z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80553-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="80553-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="80553-120">-ForceUpdate</span></span>
<span data-ttu-id="80553-121">Generowanie znacznika dla wymuszenia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="80553-121">Generate a tag for force update.</span></span>  <span data-ttu-id="80553-122">Należy to podać w celu wykonania powtarzających się operacji szyfrowania na tej samej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80553-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="80553-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80553-123">-ResourceGroupName</span></span>
<span data-ttu-id="80553-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="80553-124">The resource group name.</span></span>

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

### <span data-ttu-id="80553-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="80553-125">-VMScaleSetName</span></span>
<span data-ttu-id="80553-126">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80553-126">The virtual machine name.</span></span>

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

### <span data-ttu-id="80553-127">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="80553-127">-VolumeType</span></span>
<span data-ttu-id="80553-128">Typ woluminu (system operacyjny lub dane) do wykonania operacji szyfrowania</span><span class="sxs-lookup"><span data-stu-id="80553-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="80553-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80553-129">-Confirm</span></span>
<span data-ttu-id="80553-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80553-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80553-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80553-131">-WhatIf</span></span>
<span data-ttu-id="80553-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80553-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80553-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80553-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80553-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80553-134">CommonParameters</span></span>
<span data-ttu-id="80553-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80553-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80553-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80553-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80553-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80553-137">INPUTS</span></span>

### <span data-ttu-id="80553-138">System. String</span><span class="sxs-lookup"><span data-stu-id="80553-138">System.String</span></span>

## <span data-ttu-id="80553-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80553-139">OUTPUTS</span></span>

### <span data-ttu-id="80553-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="80553-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="80553-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80553-141">NOTES</span></span>

## <span data-ttu-id="80553-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80553-142">RELATED LINKS</span></span>

