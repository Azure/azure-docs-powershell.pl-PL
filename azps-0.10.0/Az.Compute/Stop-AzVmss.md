---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: 6669952330d82fc7c5dac8f564b34de7c896511c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891609"
---
# <span data-ttu-id="33b3b-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33b3b-101">Stop-AzVmss</span></span>

## <span data-ttu-id="33b3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="33b3b-103">Zatrzymuje VMSS lub zestaw maszyn wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="33b3b-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="33b3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33b3b-104">SYNTAX</span></span>

### <span data-ttu-id="33b3b-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33b3b-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33b3b-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="33b3b-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33b3b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="33b3b-107">DESCRIPTION</span></span>
<span data-ttu-id="33b3b-108">Polecenie cmdlet **stop-AzVmss** zatrzymuje wszystkie maszyny wirtualne w zestawie skali maszyny wirtualnej (VMSS) lub zestaw maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="33b3b-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="33b3b-109">W celu wybrania zestawu maszyn wirtualnych można użyć parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="33b3b-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="33b3b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33b3b-110">EXAMPLES</span></span>

### <span data-ttu-id="33b3b-111">Przykład 1. Zatrzymaj wszystkie maszyny wirtualne w VMSS</span><span class="sxs-lookup"><span data-stu-id="33b3b-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="33b3b-112">To polecenie zatrzymuje wszystkie maszyny wirtualne należące do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="33b3b-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="33b3b-113">Przykład 2: zatrzymywanie określonego zestawu maszyn wirtualnych w VMSS</span><span class="sxs-lookup"><span data-stu-id="33b3b-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="33b3b-114">To polecenie zatrzymuje określony zestaw maszyn wirtualnych określony przez tablicę ciągów identyfikatora wystąpienia, która należy do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="33b3b-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="33b3b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33b3b-115">PARAMETERS</span></span>

### <span data-ttu-id="33b3b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33b3b-116">-AsJob</span></span>
<span data-ttu-id="33b3b-117">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="33b3b-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b3b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b3b-118">-DefaultProfile</span></span>
<span data-ttu-id="33b3b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33b3b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b3b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="33b3b-120">-Force</span></span>
<span data-ttu-id="33b3b-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="33b3b-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b3b-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="33b3b-122">-InstanceId</span></span>
<span data-ttu-id="33b3b-123">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpień maszyny wirtualnej, które zostały zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33b3b-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="33b3b-124">Na przykład: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="33b3b-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b3b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b3b-125">-ResourceGroupName</span></span>
<span data-ttu-id="33b3b-126">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="33b3b-126">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b3b-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="33b3b-127">-StayProvisioned</span></span>
<span data-ttu-id="33b3b-128">Jeśli zostanie określona, maszyna wirtualna będzie wprowadzać stan zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="33b3b-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="33b3b-129">Jeśli nie zostanie określona, maszyna wirtualna będzie wprowadzać stan wstrzymania.</span><span class="sxs-lookup"><span data-stu-id="33b3b-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="33b3b-130">Użytkownik nadal jest obciążany maszyną wirtualną w stanie zatrzymanym, ale nie dotyczy maszyn wirtualnych w stanie wstrzymania.</span><span class="sxs-lookup"><span data-stu-id="33b3b-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b3b-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="33b3b-131">-VMScaleSetName</span></span>
<span data-ttu-id="33b3b-132">Określa nazwę VMSS, dla którego to polecenie cmdlet zatrzymuje maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="33b3b-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b3b-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33b3b-133">-Confirm</span></span>
<span data-ttu-id="33b3b-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33b3b-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b3b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33b3b-135">-WhatIf</span></span>
<span data-ttu-id="33b3b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33b3b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33b3b-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="33b3b-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b3b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b3b-138">CommonParameters</span></span>
<span data-ttu-id="33b3b-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b3b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b3b-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33b3b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b3b-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33b3b-141">INPUTS</span></span>

### <span data-ttu-id="33b3b-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="33b3b-142">None</span></span>
<span data-ttu-id="33b3b-143">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="33b3b-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33b3b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33b3b-144">OUTPUTS</span></span>

### <span data-ttu-id="33b3b-145">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="33b3b-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="33b3b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33b3b-146">NOTES</span></span>

## <span data-ttu-id="33b3b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33b3b-147">RELATED LINKS</span></span>

[<span data-ttu-id="33b3b-148">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33b3b-148">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="33b3b-149">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="33b3b-149">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="33b3b-150">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33b3b-150">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="33b3b-151">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33b3b-151">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="33b3b-152">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33b3b-152">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="33b3b-153">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="33b3b-153">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="33b3b-154">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33b3b-154">Update-AzVmss</span></span>](./Update-AzVmss.md)


