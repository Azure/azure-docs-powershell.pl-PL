---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 8fe939bfb959a1a6bc2dc043dbc3948943aa2c05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706233"
---
# <span data-ttu-id="a5a6d-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="a5a6d-101">Restart-AzVM</span></span>

## <span data-ttu-id="a5a6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a6d-103">Ponowne uruchamianie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="a5a6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5a6d-104">SYNTAX</span></span>

### <span data-ttu-id="a5a6d-105">RestartResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5a6d-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a6d-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a5a6d-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a6d-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a5a6d-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5a6d-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a5a6d-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a6d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a5a6d-109">DESCRIPTION</span></span>
<span data-ttu-id="a5a6d-110">Polecenie cmdlet **restart-AzVM** powoduje ponowne uruchomienie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="a5a6d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5a6d-111">EXAMPLES</span></span>

### <span data-ttu-id="a5a6d-112">Przykład 1: ponowne uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a5a6d-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a5a6d-113">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="a5a6d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5a6d-114">PARAMETERS</span></span>

### <span data-ttu-id="a5a6d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5a6d-115">-AsJob</span></span>
<span data-ttu-id="a5a6d-116">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a5a6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a6d-117">-DefaultProfile</span></span>
<span data-ttu-id="a5a6d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5a6d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="a5a6d-119">-Id</span></span>
<span data-ttu-id="a5a6d-120">Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="a5a6d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5a6d-121">-Name</span></span>
<span data-ttu-id="a5a6d-122">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="a5a6d-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a5a6d-123">-NoWait</span></span>
<span data-ttu-id="a5a6d-124">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a5a6d-125">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a5a6d-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="a5a6d-126">-PerformMaintenance</span></span>
<span data-ttu-id="a5a6d-127">Aby przeprowadzić konserwację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-127">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="a5a6d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a6d-128">-ResourceGroupName</span></span>
<span data-ttu-id="a5a6d-129">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a5a6d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5a6d-130">-Confirm</span></span>
<span data-ttu-id="a5a6d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a6d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a6d-132">-WhatIf</span></span>
<span data-ttu-id="a5a6d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5a6d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a6d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a6d-135">CommonParameters</span></span>
<span data-ttu-id="a5a6d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a6d-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5a6d-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a6d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5a6d-138">INPUTS</span></span>

### <span data-ttu-id="a5a6d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a6d-139">System.String</span></span>

### <span data-ttu-id="a5a6d-140">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a5a6d-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a5a6d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5a6d-141">OUTPUTS</span></span>

### <span data-ttu-id="a5a6d-142">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a5a6d-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="a5a6d-143">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a5a6d-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a5a6d-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5a6d-144">NOTES</span></span>

## <span data-ttu-id="a5a6d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5a6d-145">RELATED LINKS</span></span>

[<span data-ttu-id="a5a6d-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a5a6d-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a5a6d-147">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="a5a6d-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="a5a6d-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="a5a6d-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="a5a6d-149">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="a5a6d-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="a5a6d-150">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="a5a6d-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="a5a6d-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a5a6d-151">Update-AzVM</span></span>](./Update-AzVM.md)


