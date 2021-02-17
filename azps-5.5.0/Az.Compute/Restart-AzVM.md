---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238770"
---
# <span data-ttu-id="22ff0-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="22ff0-101">Restart-AzVM</span></span>

## <span data-ttu-id="22ff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="22ff0-103">Ponowne uruchomienie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22ff0-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="22ff0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="22ff0-104">SYNTAX</span></span>

### <span data-ttu-id="22ff0-105">RestartResourceGroupNameParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="22ff0-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ff0-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="22ff0-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ff0-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="22ff0-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22ff0-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="22ff0-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22ff0-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="22ff0-109">DESCRIPTION</span></span>
<span data-ttu-id="22ff0-110">Polecenie **cmdlet Restart-AzVM** powoduje ponowne uruchomienie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22ff0-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="22ff0-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="22ff0-111">EXAMPLES</span></span>

### <span data-ttu-id="22ff0-112">Przykład 1. Ponowne uruchamianie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="22ff0-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="22ff0-113">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w grupie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="22ff0-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="22ff0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22ff0-114">PARAMETERS</span></span>

### <span data-ttu-id="22ff0-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="22ff0-115">-AsJob</span></span>
<span data-ttu-id="22ff0-116">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="22ff0-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="22ff0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ff0-117">-DefaultProfile</span></span>
<span data-ttu-id="22ff0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="22ff0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22ff0-119">— Id</span><span class="sxs-lookup"><span data-stu-id="22ff0-119">-Id</span></span>
<span data-ttu-id="22ff0-120">Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22ff0-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ff0-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="22ff0-121">-Name</span></span>
<span data-ttu-id="22ff0-122">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22ff0-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ff0-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="22ff0-123">-NoWait</span></span>
<span data-ttu-id="22ff0-124">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="22ff0-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="22ff0-125">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="22ff0-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="22ff0-126">- PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="22ff0-126">-PerformMaintenance</span></span>
<span data-ttu-id="22ff0-127">Aby wykonać konserwację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22ff0-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ff0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ff0-128">-ResourceGroupName</span></span>
<span data-ttu-id="22ff0-129">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22ff0-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ff0-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22ff0-130">-Confirm</span></span>
<span data-ttu-id="22ff0-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="22ff0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ff0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ff0-132">-WhatIf</span></span>
<span data-ttu-id="22ff0-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22ff0-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22ff0-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="22ff0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ff0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ff0-135">CommonParameters</span></span>
<span data-ttu-id="22ff0-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ff0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ff0-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22ff0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ff0-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22ff0-138">INPUTS</span></span>

### <span data-ttu-id="22ff0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="22ff0-139">System.String</span></span>

### <span data-ttu-id="22ff0-140">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="22ff0-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="22ff0-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22ff0-141">OUTPUTS</span></span>

### <span data-ttu-id="22ff0-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="22ff0-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="22ff0-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="22ff0-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="22ff0-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="22ff0-144">NOTES</span></span>

## <span data-ttu-id="22ff0-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22ff0-145">RELATED LINKS</span></span>

[<span data-ttu-id="22ff0-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="22ff0-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="22ff0-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="22ff0-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="22ff0-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="22ff0-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="22ff0-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="22ff0-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="22ff0-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="22ff0-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="22ff0-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="22ff0-151">Update-AzVM</span></span>](./Update-AzVM.md)


