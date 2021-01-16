---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358603"
---
# <span data-ttu-id="bb3b8-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="bb3b8-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="bb3b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="bb3b8-103">Ustawia stan usługi Orchestration dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="bb3b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb3b8-104">SYNTAX</span></span>

### <span data-ttu-id="bb3b8-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bb3b8-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb3b8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="bb3b8-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb3b8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="bb3b8-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb3b8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bb3b8-108">DESCRIPTION</span></span>
<span data-ttu-id="bb3b8-109">Ustawia stan usługi Orchestration dla VMSS.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="bb3b8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb3b8-110">EXAMPLES</span></span>

### <span data-ttu-id="bb3b8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb3b8-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="bb3b8-112">To polecenie zawiesza usługę naprawy automatyczne na VMSS "vmss1" w grupie zasobów "RG".</span><span class="sxs-lookup"><span data-stu-id="bb3b8-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="bb3b8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bb3b8-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="bb3b8-114">To polecenie powoduje wznowienie działania usługi automatycznej naprawy na VMSS "vmss1" w grupie zasobów "RG".</span><span class="sxs-lookup"><span data-stu-id="bb3b8-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="bb3b8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb3b8-115">PARAMETERS</span></span>

### <span data-ttu-id="bb3b8-116">-Action</span><span class="sxs-lookup"><span data-stu-id="bb3b8-116">-Action</span></span>
<span data-ttu-id="bb3b8-117">Akcja, którą należy wykonać.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-117">The action to be performed.</span></span>  <span data-ttu-id="bb3b8-118">Możliwe wartości: Życiorys, wstrzymanie.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3b8-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb3b8-119">-AsJob</span></span>
<span data-ttu-id="bb3b8-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bb3b8-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb3b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb3b8-121">-DefaultProfile</span></span>
<span data-ttu-id="bb3b8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb3b8-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb3b8-123">-InputObject</span></span>
<span data-ttu-id="bb3b8-124">Lokalny obiekt zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bb3b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb3b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb3b8-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="bb3b8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb3b8-127">-ResourceId</span></span>
<span data-ttu-id="bb3b8-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="bb3b8-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bb3b8-129">-ServiceName</span></span>
<span data-ttu-id="bb3b8-130">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-130">The name of the service.</span></span>

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

### <span data-ttu-id="bb3b8-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bb3b8-131">-VMScaleSetName</span></span>
<span data-ttu-id="bb3b8-132">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bb3b8-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb3b8-133">-Confirm</span></span>
<span data-ttu-id="bb3b8-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb3b8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb3b8-135">-WhatIf</span></span>
<span data-ttu-id="bb3b8-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb3b8-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb3b8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3b8-138">CommonParameters</span></span>
<span data-ttu-id="bb3b8-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb3b8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3b8-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb3b8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3b8-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb3b8-141">INPUTS</span></span>

### <span data-ttu-id="bb3b8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="bb3b8-142">System.String</span></span>

### <span data-ttu-id="bb3b8-143">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bb3b8-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bb3b8-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb3b8-144">OUTPUTS</span></span>

### <span data-ttu-id="bb3b8-145">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="bb3b8-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bb3b8-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb3b8-146">NOTES</span></span>

## <span data-ttu-id="bb3b8-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb3b8-147">RELATED LINKS</span></span>
