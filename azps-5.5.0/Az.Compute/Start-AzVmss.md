---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200650"
---
# <span data-ttu-id="a72f3-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a72f3-101">Start-AzVmss</span></span>

## <span data-ttu-id="a72f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a72f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a72f3-103">Uruchamia usługę VIRTUALSS lub zestaw maszyn wirtualnych w ramach tej usługi.</span><span class="sxs-lookup"><span data-stu-id="a72f3-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="a72f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a72f3-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a72f3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a72f3-105">DESCRIPTION</span></span>
<span data-ttu-id="a72f3-106">Polecenie **cmdlet Start-AzVmss** uruchamia wszystkie maszyny wirtualne w zestawie skal maszyn wirtualnych (VMSS) lub zestawie maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="a72f3-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="a72f3-107">Aby wybrać zestaw maszyn wirtualnych, możesz użyć parametru *InstanceId.*</span><span class="sxs-lookup"><span data-stu-id="a72f3-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="a72f3-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a72f3-108">EXAMPLES</span></span>

### <span data-ttu-id="a72f3-109">Przykład 1. Uruchamianie określonego zestawu maszyn wirtualnych w ramach usługi VIRTUALSS</span><span class="sxs-lookup"><span data-stu-id="a72f3-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="a72f3-110">To polecenie uruchamia określony zestaw maszyn wirtualnych określony przez tablicę ciągów identyfikatorów wystąpień należącą do usługi MASZYNY.WIRTUALNE o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="a72f3-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="a72f3-111">Przykład 2. Uruchamianie wszystkich maszyn wirtualnych w ramach usługi MASZYNY WIRTUALNE</span><span class="sxs-lookup"><span data-stu-id="a72f3-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="a72f3-112">To polecenie uruchamia wszystkie maszyny wirtualne, które należą do maszyn wirtualnych o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="a72f3-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="a72f3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a72f3-113">PARAMETERS</span></span>

### <span data-ttu-id="a72f3-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a72f3-114">-AsJob</span></span>
<span data-ttu-id="a72f3-115">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="a72f3-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a72f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72f3-116">-DefaultProfile</span></span>
<span data-ttu-id="a72f3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a72f3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a72f3-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a72f3-118">-InstanceId</span></span>
<span data-ttu-id="a72f3-119">Określa jako tablicę ciągów identyfikatory lub identyfikatory wystąpień, których uruchamia polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a72f3-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="a72f3-120">Na przykład: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="a72f3-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="a72f3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a72f3-121">-ResourceGroupName</span></span>
<span data-ttu-id="a72f3-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a72f3-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="a72f3-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a72f3-123">-VMScaleSetName</span></span>
<span data-ttu-id="a72f3-124">Określa nazwę usługi VIRTUALSS, za pomocą których to polecenie cmdlet uruchamia maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="a72f3-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="a72f3-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a72f3-125">-Confirm</span></span>
<span data-ttu-id="a72f3-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a72f3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a72f3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a72f3-127">-WhatIf</span></span>
<span data-ttu-id="a72f3-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a72f3-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a72f3-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a72f3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a72f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72f3-130">CommonParameters</span></span>
<span data-ttu-id="a72f3-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a72f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72f3-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a72f3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72f3-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a72f3-133">INPUTS</span></span>

### <span data-ttu-id="a72f3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a72f3-134">System.String</span></span>

### <span data-ttu-id="a72f3-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a72f3-135">System.String[]</span></span>

## <span data-ttu-id="a72f3-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a72f3-136">OUTPUTS</span></span>

### <span data-ttu-id="a72f3-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a72f3-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a72f3-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a72f3-138">NOTES</span></span>

## <span data-ttu-id="a72f3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a72f3-139">RELATED LINKS</span></span>

[<span data-ttu-id="a72f3-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a72f3-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="a72f3-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a72f3-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="a72f3-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a72f3-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="a72f3-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a72f3-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="a72f3-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a72f3-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="a72f3-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a72f3-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="a72f3-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a72f3-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


