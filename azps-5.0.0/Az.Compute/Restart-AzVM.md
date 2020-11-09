---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304338"
---
# <span data-ttu-id="3e67e-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e67e-101">Restart-AzVM</span></span>

## <span data-ttu-id="3e67e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e67e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e67e-103">Ponowne uruchamianie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3e67e-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="3e67e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e67e-104">SYNTAX</span></span>

### <span data-ttu-id="3e67e-105">RestartResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e67e-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e67e-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e67e-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e67e-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e67e-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e67e-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e67e-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e67e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3e67e-109">DESCRIPTION</span></span>
<span data-ttu-id="3e67e-110">Polecenie cmdlet **restart-AzVM** powoduje ponowne uruchomienie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3e67e-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="3e67e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e67e-111">EXAMPLES</span></span>

### <span data-ttu-id="3e67e-112">Przykład 1: ponowne uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3e67e-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="3e67e-113">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3e67e-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="3e67e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e67e-114">PARAMETERS</span></span>

### <span data-ttu-id="3e67e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e67e-115">-AsJob</span></span>
<span data-ttu-id="3e67e-116">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="3e67e-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3e67e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e67e-117">-DefaultProfile</span></span>
<span data-ttu-id="3e67e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e67e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e67e-119">-ID</span><span class="sxs-lookup"><span data-stu-id="3e67e-119">-Id</span></span>
<span data-ttu-id="3e67e-120">Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3e67e-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="3e67e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e67e-121">-Name</span></span>
<span data-ttu-id="3e67e-122">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3e67e-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="3e67e-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3e67e-123">-NoWait</span></span>
<span data-ttu-id="3e67e-124">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="3e67e-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3e67e-125">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="3e67e-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3e67e-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="3e67e-126">-PerformMaintenance</span></span>
<span data-ttu-id="3e67e-127">Aby przeprowadzić konserwację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3e67e-127">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="3e67e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e67e-128">-ResourceGroupName</span></span>
<span data-ttu-id="3e67e-129">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3e67e-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3e67e-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e67e-130">-Confirm</span></span>
<span data-ttu-id="3e67e-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e67e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e67e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e67e-132">-WhatIf</span></span>
<span data-ttu-id="3e67e-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e67e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e67e-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e67e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e67e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e67e-135">CommonParameters</span></span>
<span data-ttu-id="3e67e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e67e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e67e-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e67e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e67e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e67e-138">INPUTS</span></span>

### <span data-ttu-id="3e67e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3e67e-139">System.String</span></span>

### <span data-ttu-id="3e67e-140">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e67e-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3e67e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e67e-141">OUTPUTS</span></span>

### <span data-ttu-id="3e67e-142">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="3e67e-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="3e67e-143">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3e67e-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3e67e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e67e-144">NOTES</span></span>

## <span data-ttu-id="3e67e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e67e-145">RELATED LINKS</span></span>

[<span data-ttu-id="3e67e-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e67e-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3e67e-147">Nowe — AzVM</span><span class="sxs-lookup"><span data-stu-id="3e67e-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="3e67e-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e67e-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="3e67e-149">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="3e67e-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="3e67e-150">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="3e67e-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="3e67e-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e67e-151">Update-AzVM</span></span>](./Update-AzVM.md)


