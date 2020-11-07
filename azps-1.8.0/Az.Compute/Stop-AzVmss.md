---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: d00a51a722fa03742c56387ee27faa4f6228ded7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710175"
---
# <span data-ttu-id="8793d-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8793d-101">Stop-AzVmss</span></span>

## <span data-ttu-id="8793d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8793d-102">SYNOPSIS</span></span>
<span data-ttu-id="8793d-103">Zatrzymuje VMSS lub zestaw maszyn wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="8793d-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="8793d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8793d-104">SYNTAX</span></span>

### <span data-ttu-id="8793d-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8793d-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8793d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8793d-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8793d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8793d-107">DESCRIPTION</span></span>
<span data-ttu-id="8793d-108">Polecenie cmdlet **stop-AzVmss** zatrzymuje wszystkie maszyny wirtualne w zestawie skali maszyny wirtualnej (VMSS) lub zestaw maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="8793d-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="8793d-109">W celu wybrania zestawu maszyn wirtualnych można użyć parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="8793d-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="8793d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8793d-110">EXAMPLES</span></span>

### <span data-ttu-id="8793d-111">Przykład 1. Zatrzymaj wszystkie maszyny wirtualne w VMSS</span><span class="sxs-lookup"><span data-stu-id="8793d-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="8793d-112">To polecenie zatrzymuje wszystkie maszyny wirtualne należące do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="8793d-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="8793d-113">Przykład 2: zatrzymywanie określonego zestawu maszyn wirtualnych w VMSS</span><span class="sxs-lookup"><span data-stu-id="8793d-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="8793d-114">To polecenie zatrzymuje określony zestaw maszyn wirtualnych określony przez tablicę ciągów identyfikatora wystąpienia, która należy do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="8793d-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="8793d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8793d-115">PARAMETERS</span></span>

### <span data-ttu-id="8793d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8793d-116">-AsJob</span></span>
<span data-ttu-id="8793d-117">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="8793d-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8793d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8793d-118">-DefaultProfile</span></span>
<span data-ttu-id="8793d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8793d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8793d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8793d-120">-Force</span></span>
<span data-ttu-id="8793d-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8793d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8793d-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8793d-122">-InstanceId</span></span>
<span data-ttu-id="8793d-123">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpień maszyny wirtualnej, które zostały zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8793d-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="8793d-124">Na przykład: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="8793d-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="8793d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8793d-125">-ResourceGroupName</span></span>
<span data-ttu-id="8793d-126">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="8793d-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="8793d-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="8793d-127">-StayProvisioned</span></span>
<span data-ttu-id="8793d-128">Jeśli zostanie określona, maszyna wirtualna będzie wprowadzać stan zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="8793d-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="8793d-129">Jeśli nie zostanie określona, maszyna wirtualna będzie wprowadzać stan wstrzymania.</span><span class="sxs-lookup"><span data-stu-id="8793d-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="8793d-130">Użytkownik nadal jest obciążany maszyną wirtualną w stanie zatrzymanym, ale nie dotyczy maszyn wirtualnych w stanie wstrzymania.</span><span class="sxs-lookup"><span data-stu-id="8793d-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="8793d-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8793d-131">-VMScaleSetName</span></span>
<span data-ttu-id="8793d-132">Określa nazwę VMSS, dla którego to polecenie cmdlet zatrzymuje maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="8793d-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="8793d-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8793d-133">-Confirm</span></span>
<span data-ttu-id="8793d-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8793d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8793d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8793d-135">-WhatIf</span></span>
<span data-ttu-id="8793d-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8793d-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8793d-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8793d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8793d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8793d-138">CommonParameters</span></span>
<span data-ttu-id="8793d-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8793d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8793d-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8793d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8793d-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8793d-141">INPUTS</span></span>

### <span data-ttu-id="8793d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8793d-142">System.String</span></span>

### <span data-ttu-id="8793d-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="8793d-143">System.String[]</span></span>

## <span data-ttu-id="8793d-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8793d-144">OUTPUTS</span></span>

### <span data-ttu-id="8793d-145">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8793d-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8793d-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8793d-146">NOTES</span></span>

## <span data-ttu-id="8793d-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8793d-147">RELATED LINKS</span></span>

[<span data-ttu-id="8793d-148">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8793d-148">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="8793d-149">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="8793d-149">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="8793d-150">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8793d-150">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="8793d-151">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8793d-151">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="8793d-152">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8793d-152">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="8793d-153">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="8793d-153">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="8793d-154">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8793d-154">Update-AzVmss</span></span>](./Update-AzVmss.md)


