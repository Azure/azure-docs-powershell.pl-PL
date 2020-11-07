---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: ce71ad0e82e7082c199d4823c3a3a59be972ec60
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706162"
---
# <span data-ttu-id="76fb2-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="76fb2-101">Set-AzVmss</span></span>

## <span data-ttu-id="76fb2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="76fb2-103">Ustawia określone akcje na określonym VMSS.</span><span class="sxs-lookup"><span data-stu-id="76fb2-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="76fb2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76fb2-104">SYNTAX</span></span>

### <span data-ttu-id="76fb2-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="76fb2-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76fb2-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="76fb2-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76fb2-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="76fb2-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76fb2-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="76fb2-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76fb2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="76fb2-109">DESCRIPTION</span></span>
<span data-ttu-id="76fb2-110">Polecenie cmdlet **Set-AzVmss** ustawia określone akcje na zestawie skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="76fb2-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="76fb2-111">Jedyna akcja obsługiwana przez ten aplet polecenia to Reimage.</span><span class="sxs-lookup"><span data-stu-id="76fb2-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="76fb2-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76fb2-112">EXAMPLES</span></span>

### <span data-ttu-id="76fb2-113">Przykład 1: odobrazowanie VMSS</span><span class="sxs-lookup"><span data-stu-id="76fb2-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="76fb2-114">To polecenie powoduje ponowne zdjęcie VMSS o nazwie ContosoVMSS należącej do grupy zasobów o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="76fb2-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="76fb2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76fb2-115">PARAMETERS</span></span>

### <span data-ttu-id="76fb2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76fb2-116">-AsJob</span></span>
<span data-ttu-id="76fb2-117">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="76fb2-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="76fb2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fb2-118">-DefaultProfile</span></span>
<span data-ttu-id="76fb2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76fb2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76fb2-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="76fb2-120">-InstanceId</span></span>
<span data-ttu-id="76fb2-121">Identyfikator wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="76fb2-121">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="76fb2-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="76fb2-122">-PerformMaintenance</span></span>
<span data-ttu-id="76fb2-123">Wskazuje, że to polecenie cmdlet przeprowadza konserwację co najmniej jednej maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="76fb2-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="76fb2-124">-Deploy</span><span class="sxs-lookup"><span data-stu-id="76fb2-124">-Redeploy</span></span>
<span data-ttu-id="76fb2-125">Wskazuje, że polecenie cmdlet powoduje ponowne wdrożenie co najmniej jednej maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="76fb2-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="76fb2-126">-Reimage</span><span class="sxs-lookup"><span data-stu-id="76fb2-126">-Reimage</span></span>
<span data-ttu-id="76fb2-127">Wskazuje, że polecenie cmdlet reobrazuje VMSS.</span><span class="sxs-lookup"><span data-stu-id="76fb2-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="76fb2-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="76fb2-128">-ReimageAll</span></span>
<span data-ttu-id="76fb2-129">Wskazuje, że polecenie cmdlet reobrazuje wszystkie dyski w VMSS.</span><span class="sxs-lookup"><span data-stu-id="76fb2-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="76fb2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76fb2-130">-ResourceGroupName</span></span>
<span data-ttu-id="76fb2-131">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="76fb2-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="76fb2-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="76fb2-132">-TempDisk</span></span>
<span data-ttu-id="76fb2-133">Określa, czy dysk tymczasowy ma zostać przeobrazek.</span><span class="sxs-lookup"><span data-stu-id="76fb2-133">Specifies whether to reimage temp disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fb2-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="76fb2-134">-VMScaleSetName</span></span>
<span data-ttu-id="76fb2-135">Gatunek nazwa VMSS, dla którego to polecenie cmdlet ustawia akcje.</span><span class="sxs-lookup"><span data-stu-id="76fb2-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="76fb2-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76fb2-136">-Confirm</span></span>
<span data-ttu-id="76fb2-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76fb2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76fb2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76fb2-138">-WhatIf</span></span>
<span data-ttu-id="76fb2-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76fb2-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76fb2-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76fb2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76fb2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fb2-141">CommonParameters</span></span>
<span data-ttu-id="76fb2-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76fb2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fb2-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76fb2-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fb2-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76fb2-144">INPUTS</span></span>

### <span data-ttu-id="76fb2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="76fb2-145">System.String</span></span>

### <span data-ttu-id="76fb2-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="76fb2-146">System.String[]</span></span>

## <span data-ttu-id="76fb2-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76fb2-147">OUTPUTS</span></span>

### <span data-ttu-id="76fb2-148">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="76fb2-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="76fb2-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76fb2-149">NOTES</span></span>

## <span data-ttu-id="76fb2-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76fb2-150">RELATED LINKS</span></span>

[<span data-ttu-id="76fb2-151">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="76fb2-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="76fb2-152">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="76fb2-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="76fb2-153">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="76fb2-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="76fb2-154">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="76fb2-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="76fb2-155">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="76fb2-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="76fb2-156">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="76fb2-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="76fb2-157">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="76fb2-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


