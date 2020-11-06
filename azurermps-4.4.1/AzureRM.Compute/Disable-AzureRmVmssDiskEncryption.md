---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 8cb68b45637496cb87e387c6755fe861fe3e21f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553991"
---
# <span data-ttu-id="4ba85-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4ba85-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="4ba85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ba85-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba85-103">Wyłącza szyfrowanie dysków w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4ba85-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ba85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ba85-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ba85-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ba85-105">DESCRIPTION</span></span>
<span data-ttu-id="4ba85-106">Wyłącza szyfrowanie dysków w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4ba85-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="4ba85-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ba85-107">EXAMPLES</span></span>

### <span data-ttu-id="4ba85-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4ba85-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="4ba85-109">Wyłącza szyfrowanie dysków na zestawie skali maszyny wirtualnej o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="4ba85-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="4ba85-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ba85-110">PARAMETERS</span></span>

### <span data-ttu-id="4ba85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba85-111">-DefaultProfile</span></span>
<span data-ttu-id="4ba85-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba85-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba85-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="4ba85-113">-ExtensionName</span></span>
<span data-ttu-id="4ba85-114">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="4ba85-114">The extension name.</span></span>
<span data-ttu-id="4ba85-115">Jeśli ten parametr nie zostanie określony, używane są wartości domyślne AzureDiskEncryption dla maszyn wirtualnych i AzureDiskEncryptionForLinux dla systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="4ba85-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="4ba85-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4ba85-116">-Force</span></span>
<span data-ttu-id="4ba85-117">Aby wymusić usunięcie rozszerzenia z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4ba85-117">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="4ba85-118">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="4ba85-118">-ForceUpdate</span></span>
<span data-ttu-id="4ba85-119">Generowanie znacznika dla wymuszenia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="4ba85-119">Generate a tag for force update.</span></span>  <span data-ttu-id="4ba85-120">Należy to podać w celu wykonania powtarzających się operacji szyfrowania na tej samej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4ba85-120">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="4ba85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba85-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ba85-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ba85-122">The resource group name.</span></span>

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

### <span data-ttu-id="4ba85-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4ba85-123">-VMScaleSetName</span></span>
<span data-ttu-id="4ba85-124">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4ba85-124">The virtual machine name.</span></span>

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

### <span data-ttu-id="4ba85-125">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="4ba85-125">-VolumeType</span></span>
<span data-ttu-id="4ba85-126">Typ woluminu (system operacyjny lub dane) do wykonania operacji szyfrowania</span><span class="sxs-lookup"><span data-stu-id="4ba85-126">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="4ba85-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ba85-127">-Confirm</span></span>
<span data-ttu-id="4ba85-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ba85-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba85-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba85-129">-WhatIf</span></span>
<span data-ttu-id="4ba85-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ba85-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ba85-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ba85-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba85-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba85-132">CommonParameters</span></span>
<span data-ttu-id="4ba85-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ba85-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba85-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba85-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba85-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ba85-135">INPUTS</span></span>

### <span data-ttu-id="4ba85-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4ba85-136">System.String</span></span>

## <span data-ttu-id="4ba85-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ba85-137">OUTPUTS</span></span>

### <span data-ttu-id="4ba85-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4ba85-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4ba85-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ba85-139">NOTES</span></span>

## <span data-ttu-id="4ba85-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ba85-140">RELATED LINKS</span></span>

