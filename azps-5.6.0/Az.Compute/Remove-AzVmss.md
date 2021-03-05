---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: 2ed7be0cf790a596a2a2fc9b23c0e6aa50f67623
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998887"
---
# <span data-ttu-id="56ee2-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56ee2-101">Remove-AzVmss</span></span>

## <span data-ttu-id="56ee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="56ee2-103">Usuwa maszyny wirtualnej lub maszyny wirtualnej, która znajduje się w tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="56ee2-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="56ee2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56ee2-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56ee2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="56ee2-105">DESCRIPTION</span></span>
<span data-ttu-id="56ee2-106">Polecenie **cmdlet Remove-AzVmss** usuwa zestaw skal maszyn wirtualnych (VMSS) z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="56ee2-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="56ee2-107">To polecenie cmdlet może być również używane do usuwania określonej maszyny wirtualnej w środowisku maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56ee2-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="56ee2-108">Za pomocą parametru *InstanceId* można usunąć określoną maszynę wirtualną w przestrzeni maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56ee2-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="56ee2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56ee2-109">EXAMPLES</span></span>

### <span data-ttu-id="56ee2-110">Przykład 1. Usuwanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="56ee2-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="56ee2-111">To polecenie usuwa maszyny wirtualne o nazwie VMScaleSet001, która należy do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="56ee2-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="56ee2-112">Przykład 2. Usuwanie maszyny wirtualnej z usługi maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="56ee2-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="56ee2-113">To polecenie usuwa maszynę wirtualną o identyfikatorze 3 z maszyny WIRTUALNEJ o nazwie MACHINEScaleSet002, która należy do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="56ee2-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="56ee2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56ee2-114">PARAMETERS</span></span>

### <span data-ttu-id="56ee2-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="56ee2-115">-AsJob</span></span>
<span data-ttu-id="56ee2-116">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="56ee2-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="56ee2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ee2-117">-DefaultProfile</span></span>
<span data-ttu-id="56ee2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56ee2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56ee2-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="56ee2-119">-Force</span></span>
<span data-ttu-id="56ee2-120">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="56ee2-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="56ee2-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="56ee2-121">-InstanceId</span></span>
<span data-ttu-id="56ee2-122">Określa jako tablicę ciągów identyfikator wystąpień, które muszą zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="56ee2-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="56ee2-123">Na przykład: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="56ee2-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="56ee2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ee2-124">-ResourceGroupName</span></span>
<span data-ttu-id="56ee2-125">Określa nazwę grupy zasobów, do której należy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56ee2-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="56ee2-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="56ee2-126">-VMScaleSetName</span></span>
<span data-ttu-id="56ee2-127">To polecenie cmdlet ma nazwę maszyny wirtualnej, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56ee2-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="56ee2-128">Jeśli określisz parametr *InstanceId,* polecenie cmdlet spowoduje usunięcie określonej maszyny wirtualnej z usług VIRTUALSS nazwanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="56ee2-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="56ee2-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56ee2-129">-Confirm</span></span>
<span data-ttu-id="56ee2-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="56ee2-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ee2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56ee2-131">-WhatIf</span></span>
<span data-ttu-id="56ee2-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56ee2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56ee2-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="56ee2-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ee2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ee2-134">CommonParameters</span></span>
<span data-ttu-id="56ee2-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ee2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ee2-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56ee2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ee2-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56ee2-137">INPUTS</span></span>

### <span data-ttu-id="56ee2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="56ee2-138">System.String</span></span>

### <span data-ttu-id="56ee2-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="56ee2-139">System.String[]</span></span>

## <span data-ttu-id="56ee2-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56ee2-140">OUTPUTS</span></span>

### <span data-ttu-id="56ee2-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="56ee2-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="56ee2-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56ee2-142">NOTES</span></span>

## <span data-ttu-id="56ee2-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56ee2-143">RELATED LINKS</span></span>

[<span data-ttu-id="56ee2-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56ee2-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="56ee2-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56ee2-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="56ee2-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56ee2-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="56ee2-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56ee2-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="56ee2-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56ee2-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="56ee2-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56ee2-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="56ee2-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56ee2-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


