---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: 152be66a2e1582d9f8377e09e250d3cf044c64db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010785"
---
# <span data-ttu-id="3aaec-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3aaec-101">Stop-AzVmss</span></span>

## <span data-ttu-id="3aaec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aaec-102">SYNOPSIS</span></span>
<span data-ttu-id="3aaec-103">Zatrzymuje maszyny wirtualnej lub zestaw maszyn wirtualnych w ramach tej usługi.</span><span class="sxs-lookup"><span data-stu-id="3aaec-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="3aaec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3aaec-104">SYNTAX</span></span>

### <span data-ttu-id="3aaec-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3aaec-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aaec-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3aaec-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3aaec-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3aaec-107">DESCRIPTION</span></span>
<span data-ttu-id="3aaec-108">Polecenie **cmdlet Stop-AzVmss** zatrzymuje wszystkie maszyny wirtualne w zestawie skal maszyn wirtualnych (VMSS) lub zestawie maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="3aaec-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="3aaec-109">Aby wybrać zestaw maszyn wirtualnych, możesz użyć parametru *InstanceId.*</span><span class="sxs-lookup"><span data-stu-id="3aaec-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="3aaec-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3aaec-110">EXAMPLES</span></span>

### <span data-ttu-id="3aaec-111">Przykład 1. Zatrzymywanie wszystkich maszyn wirtualnych w ramach usługi VIRTUALSS</span><span class="sxs-lookup"><span data-stu-id="3aaec-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="3aaec-112">To polecenie zatrzymuje wszystkie maszyny wirtualne należące do maszyn wirtualnych o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="3aaec-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="3aaec-113">Przykład 2. Zatrzymywanie określonego zestawu maszyn wirtualnych w ramach usługi MASZYNY WIRTUALNE</span><span class="sxs-lookup"><span data-stu-id="3aaec-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="3aaec-114">To polecenie zatrzymuje określony zestaw maszyn wirtualnych określony przez tablicę ciągów identyfikatorów wystąpień należącą do usługi MASZYNY.WIRTUALNE o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="3aaec-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="3aaec-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3aaec-115">PARAMETERS</span></span>

### <span data-ttu-id="3aaec-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3aaec-116">-AsJob</span></span>
<span data-ttu-id="3aaec-117">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="3aaec-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3aaec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aaec-118">-DefaultProfile</span></span>
<span data-ttu-id="3aaec-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3aaec-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aaec-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3aaec-120">-Force</span></span>
<span data-ttu-id="3aaec-121">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3aaec-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3aaec-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3aaec-122">-InstanceId</span></span>
<span data-ttu-id="3aaec-123">Określa jako tablicę ciągów identyfikatory lub identyfikatory wystąpień maszyn wirtualnych, które zatrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aaec-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="3aaec-124">Na przykład: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="3aaec-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aaec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aaec-125">-ResourceGroupName</span></span>
<span data-ttu-id="3aaec-126">Określa nazwę grupy zasobów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="3aaec-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="3aaec-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="3aaec-127">-SkipShutdown</span></span>
<span data-ttu-id="3aaec-128">Aby zażądać zamknięcia maszyny wirtualnej bez prolongaty</span><span class="sxs-lookup"><span data-stu-id="3aaec-128">To request non-graceful VM shutdown</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaec-129">- StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="3aaec-129">-StayProvisioned</span></span>
<span data-ttu-id="3aaec-130">Jeśli zostanie określona, maszynę wirtualną zostanie w stanie zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="3aaec-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="3aaec-131">Jeśli nie zostanie określona, maszynę wirtualną wprowadź w stanie zatrzymania-deallocated.</span><span class="sxs-lookup"><span data-stu-id="3aaec-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="3aaec-132">Użytkownik nadal jest obciążony opłatami za maszyny wirtualne w stanie zatrzymania, ale nie za maszyny wirtualne w stanie zatrzymania deallocated.</span><span class="sxs-lookup"><span data-stu-id="3aaec-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="3aaec-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3aaec-133">-VMScaleSetName</span></span>
<span data-ttu-id="3aaec-134">Określa nazwę usługi VIRTUALSS, dla której to polecenie cmdlet zatrzyma maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="3aaec-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="3aaec-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3aaec-135">-Confirm</span></span>
<span data-ttu-id="3aaec-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3aaec-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aaec-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aaec-137">-WhatIf</span></span>
<span data-ttu-id="3aaec-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aaec-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3aaec-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3aaec-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aaec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aaec-140">CommonParameters</span></span>
<span data-ttu-id="3aaec-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aaec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aaec-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3aaec-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aaec-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3aaec-143">INPUTS</span></span>

### <span data-ttu-id="3aaec-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3aaec-144">System.String</span></span>

### <span data-ttu-id="3aaec-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3aaec-145">System.String[]</span></span>

## <span data-ttu-id="3aaec-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3aaec-146">OUTPUTS</span></span>

### <span data-ttu-id="3aaec-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3aaec-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3aaec-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3aaec-148">NOTES</span></span>

## <span data-ttu-id="3aaec-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3aaec-149">RELATED LINKS</span></span>

[<span data-ttu-id="3aaec-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3aaec-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="3aaec-151">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3aaec-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="3aaec-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3aaec-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="3aaec-153">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3aaec-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="3aaec-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3aaec-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="3aaec-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3aaec-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="3aaec-156">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3aaec-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


