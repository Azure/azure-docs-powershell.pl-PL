---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 3bec7d92716f31a3aac3c204548ad01f534fa405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710231"
---
# <span data-ttu-id="8a4f6-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="8a4f6-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="8a4f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4f6-103">Ręczna aktualizacja platformy domeny Przeprowadź aktualizację maszyn wirtualnych w zestawie skali maszyny wirtualnej sieci szkieletowej usługi Fabric.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="8a4f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a4f6-104">SYNTAX</span></span>

### <span data-ttu-id="8a4f6-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a4f6-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a4f6-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8a4f6-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a4f6-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8a4f6-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a4f6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8a4f6-108">DESCRIPTION</span></span>
<span data-ttu-id="8a4f6-109">Wymuszaj ręczne aktualizowanie domeny w celu zaktualizowania maszyn wirtualnych w zestawie skali maszyny wirtualnej sieci szkieletowej usługi Fabric.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="8a4f6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a4f6-110">EXAMPLES</span></span>

### <span data-ttu-id="8a4f6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a4f6-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="8a4f6-112">To polecenie wymusza zaktualizowanie aktualizacji usługi sieci szkieletowej w witrynie UD 0 dla zestawu skali maszyny wirtualnej określonego na podstawie nazwy grupy zasobów i nazwy zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="8a4f6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8a4f6-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="8a4f6-114">To polecenie wymusza zaktualizowanie aktualizacji usługi sieci szkieletowej w witrynie UD 1 dla zestawu skali maszyny wirtualnej określonego przez obiekt zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="8a4f6-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8a4f6-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resoureId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="8a4f6-116">To polecenie wymusza zaktualizowanie aktualizacji usługi sieci szkieletowej w witrynie UD 2 dla zestawu skali maszyny wirtualnej określonego przez identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="8a4f6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a4f6-117">PARAMETERS</span></span>

### <span data-ttu-id="8a4f6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a4f6-118">-AsJob</span></span>
<span data-ttu-id="8a4f6-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8a4f6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a4f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4f6-120">-DefaultProfile</span></span>
<span data-ttu-id="8a4f6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a4f6-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="8a4f6-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="8a4f6-123">Domena aktualizacji platformy, dla której jest wymagane Przeprowadź Ręczne odzyskiwanie.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="8a4f6-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a4f6-126">-ResourceId</span></span>
<span data-ttu-id="8a4f6-127">Identyfikator zasobu zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a4f6-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8a4f6-129">Obiekt zestawu skali lokalnego maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8a4f6-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8a4f6-130">-VMScaleSetName</span></span>
<span data-ttu-id="8a4f6-131">Nazwa zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8a4f6-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4f6-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a4f6-132">-Confirm</span></span>
<span data-ttu-id="8a4f6-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a4f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a4f6-134">-WhatIf</span></span>
<span data-ttu-id="8a4f6-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a4f6-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a4f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4f6-137">CommonParameters</span></span>
<span data-ttu-id="8a4f6-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a4f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4f6-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a4f6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4f6-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a4f6-140">INPUTS</span></span>

### <span data-ttu-id="8a4f6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8a4f6-141">System.String</span></span>

### <span data-ttu-id="8a4f6-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a4f6-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8a4f6-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a4f6-143">OUTPUTS</span></span>

### <span data-ttu-id="8a4f6-144">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="8a4f6-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="8a4f6-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a4f6-145">NOTES</span></span>

## <span data-ttu-id="8a4f6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a4f6-146">RELATED LINKS</span></span>