---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 1fdd45c36d085b376ed900f0054dd98bc28c7525
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706146"
---
# <span data-ttu-id="3344a-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="3344a-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="3344a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3344a-102">SYNOPSIS</span></span>
<span data-ttu-id="3344a-103">Modyfikuje stan wystąpienia VMSS.</span><span class="sxs-lookup"><span data-stu-id="3344a-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="3344a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3344a-104">SYNTAX</span></span>

### <span data-ttu-id="3344a-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3344a-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3344a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3344a-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3344a-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="3344a-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3344a-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="3344a-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3344a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3344a-109">DESCRIPTION</span></span>
<span data-ttu-id="3344a-110">Polecenie cmdlet **Set-AzVmssVM** modyfikuje stan wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3344a-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="3344a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3344a-111">EXAMPLES</span></span>

## <span data-ttu-id="3344a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3344a-112">PARAMETERS</span></span>

### <span data-ttu-id="3344a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3344a-113">-AsJob</span></span>
<span data-ttu-id="3344a-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3344a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3344a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3344a-115">-DefaultProfile</span></span>
<span data-ttu-id="3344a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3344a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3344a-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3344a-117">-InstanceId</span></span>
<span data-ttu-id="3344a-118">Określa identyfikator wystąpienia VMSS, dla którego to polecenie cmdlet modyfikuje stan.</span><span class="sxs-lookup"><span data-stu-id="3344a-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3344a-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="3344a-119">-PerformMaintenance</span></span>
<span data-ttu-id="3344a-120">Wskazuje, że to polecenie cmdlet przeprowadza konserwację na maszynie wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="3344a-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3344a-121">-Deploy</span><span class="sxs-lookup"><span data-stu-id="3344a-121">-Redeploy</span></span>
<span data-ttu-id="3344a-122">Wskazuje, że polecenie cmdlet powoduje ponowne wdrożenie maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="3344a-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3344a-123">-Reimage</span><span class="sxs-lookup"><span data-stu-id="3344a-123">-Reimage</span></span>
<span data-ttu-id="3344a-124">Wskazuje, że to polecenie cmdlet reobrazuje wystąpienie VMSS.</span><span class="sxs-lookup"><span data-stu-id="3344a-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3344a-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="3344a-125">-ReimageAll</span></span>
<span data-ttu-id="3344a-126">Wskazuje, że polecenie cmdlet powoduje odobrazowanie wszystkich dysków w wystąpieniu VMSS.</span><span class="sxs-lookup"><span data-stu-id="3344a-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3344a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3344a-127">-ResourceGroupName</span></span>
<span data-ttu-id="3344a-128">Określa nazwę grupy zasobów zawierającej wystąpienie VMSS.</span><span class="sxs-lookup"><span data-stu-id="3344a-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="3344a-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3344a-129">-VMScaleSetName</span></span>
<span data-ttu-id="3344a-130">Określa nazwę wystąpienia VMSS, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3344a-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3344a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3344a-131">-Confirm</span></span>
<span data-ttu-id="3344a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3344a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3344a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3344a-133">-WhatIf</span></span>
<span data-ttu-id="3344a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3344a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3344a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3344a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3344a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3344a-136">CommonParameters</span></span>
<span data-ttu-id="3344a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3344a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3344a-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3344a-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3344a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3344a-139">INPUTS</span></span>

### <span data-ttu-id="3344a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3344a-140">System.String</span></span>

## <span data-ttu-id="3344a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3344a-141">OUTPUTS</span></span>

### <span data-ttu-id="3344a-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3344a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3344a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3344a-143">NOTES</span></span>

## <span data-ttu-id="3344a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3344a-144">RELATED LINKS</span></span>

[<span data-ttu-id="3344a-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="3344a-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)