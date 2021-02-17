---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: c686eec33a2f4a9f972acbdb7261f86fc45a6fa1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238760"
---
# <span data-ttu-id="36ea8-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36ea8-101">Restart-AzVmss</span></span>

## <span data-ttu-id="36ea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="36ea8-103">Powoduje ponowne uruchomienie maszyny wirtualnej lub maszyny wirtualnej w ramach tej usługi.</span><span class="sxs-lookup"><span data-stu-id="36ea8-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="36ea8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36ea8-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ea8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="36ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="36ea8-106">Polecenie **cmdlet Restart-AzVmss** powoduje ponowne uruchomienie zestawu skalowania maszyny wirtualnej (MACHINESS).</span><span class="sxs-lookup"><span data-stu-id="36ea8-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="36ea8-107">To polecenie cmdlet może być również używane do ponownego uruchamiania określonej maszyny wirtualnej w maszyny wirtualnej przy użyciu *parametru InstanceId.*</span><span class="sxs-lookup"><span data-stu-id="36ea8-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="36ea8-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36ea8-108">EXAMPLES</span></span>

### <span data-ttu-id="36ea8-109">Przykład 1. Ponowne uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="36ea8-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="36ea8-110">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o nazwie VMSS001, która należy do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="36ea8-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="36ea8-111">Przykład 2. Ponowne uruchamianie określonej maszyny wirtualnej w ramach usług VIRTUALSS</span><span class="sxs-lookup"><span data-stu-id="36ea8-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="36ea8-112">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o identyfikatorze wystąpienia 1 w maszyny wirtualnej o nazwie VMSS001, która należy do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="36ea8-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="36ea8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36ea8-113">PARAMETERS</span></span>

### <span data-ttu-id="36ea8-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="36ea8-114">-AsJob</span></span>
<span data-ttu-id="36ea8-115">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="36ea8-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="36ea8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ea8-116">-DefaultProfile</span></span>
<span data-ttu-id="36ea8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="36ea8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36ea8-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="36ea8-118">-InstanceId</span></span>
<span data-ttu-id="36ea8-119">Określa jako tablicę ciągów identyfikator wystąpień, które wymagają ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="36ea8-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="36ea8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ea8-120">-ResourceGroupName</span></span>
<span data-ttu-id="36ea8-121">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="36ea8-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="36ea8-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="36ea8-122">-VMScaleSetName</span></span>
<span data-ttu-id="36ea8-123">Nazwa serwera MASZYNY.WIRTUALNEj, dla których zostanie uruchomione ponownie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ea8-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="36ea8-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36ea8-124">-Confirm</span></span>
<span data-ttu-id="36ea8-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36ea8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ea8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ea8-126">-WhatIf</span></span>
<span data-ttu-id="36ea8-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ea8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36ea8-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="36ea8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ea8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ea8-129">CommonParameters</span></span>
<span data-ttu-id="36ea8-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36ea8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ea8-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36ea8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ea8-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36ea8-132">INPUTS</span></span>

### <span data-ttu-id="36ea8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="36ea8-133">System.String</span></span>

### <span data-ttu-id="36ea8-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="36ea8-134">System.String[]</span></span>

## <span data-ttu-id="36ea8-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36ea8-135">OUTPUTS</span></span>

### <span data-ttu-id="36ea8-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="36ea8-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="36ea8-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36ea8-137">NOTES</span></span>

## <span data-ttu-id="36ea8-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36ea8-138">RELATED LINKS</span></span>

[<span data-ttu-id="36ea8-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36ea8-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="36ea8-140">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36ea8-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="36ea8-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36ea8-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="36ea8-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36ea8-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="36ea8-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36ea8-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="36ea8-144">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36ea8-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="36ea8-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36ea8-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


