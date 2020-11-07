---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 11b387e4022bce98e1275bb2af09bc97beff0041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717595"
---
# <span data-ttu-id="67e7b-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="67e7b-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="67e7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="67e7b-103">Zatrzymuje VMSS lub zestaw maszyn wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="67e7b-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67e7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67e7b-104">SYNTAX</span></span>

### <span data-ttu-id="67e7b-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="67e7b-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e7b-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="67e7b-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67e7b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="67e7b-107">DESCRIPTION</span></span>
<span data-ttu-id="67e7b-108">Polecenie cmdlet **stop-AzureRmVmss** zatrzymuje wszystkie maszyny wirtualne w zestawie skali maszyny wirtualnej (VMSS) lub zestaw maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="67e7b-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="67e7b-109">W celu wybrania zestawu maszyn wirtualnych można użyć parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="67e7b-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="67e7b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67e7b-110">EXAMPLES</span></span>

### <span data-ttu-id="67e7b-111">Przykład 1. Zatrzymaj wszystkie maszyny wirtualne w VMSS</span><span class="sxs-lookup"><span data-stu-id="67e7b-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="67e7b-112">To polecenie zatrzymuje wszystkie maszyny wirtualne należące do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="67e7b-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="67e7b-113">Przykład 2: zatrzymywanie określonego zestawu maszyn wirtualnych w VMSS</span><span class="sxs-lookup"><span data-stu-id="67e7b-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="67e7b-114">To polecenie zatrzymuje określony zestaw maszyn wirtualnych określony przez tablicę ciągów identyfikatora wystąpienia, która należy do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="67e7b-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="67e7b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67e7b-115">PARAMETERS</span></span>

### <span data-ttu-id="67e7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e7b-116">-DefaultProfile</span></span>
<span data-ttu-id="67e7b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67e7b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e7b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="67e7b-118">-Force</span></span>
<span data-ttu-id="67e7b-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="67e7b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67e7b-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="67e7b-120">-InstanceId</span></span>
<span data-ttu-id="67e7b-121">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpień maszyny wirtualnej, które zostały zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67e7b-121">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="67e7b-122">Na przykład: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="67e7b-122">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e7b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e7b-123">-ResourceGroupName</span></span>
<span data-ttu-id="67e7b-124">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="67e7b-124">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e7b-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="67e7b-125">-StayProvisioned</span></span>
<span data-ttu-id="67e7b-126">Jeśli zostanie określona, maszyna wirtualna będzie wprowadzać stan zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="67e7b-126">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="67e7b-127">Jeśli nie zostanie określona, maszyna wirtualna będzie wprowadzać stan wstrzymania.</span><span class="sxs-lookup"><span data-stu-id="67e7b-127">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="67e7b-128">Użytkownik nadal jest obciążany maszyną wirtualną w stanie zatrzymanym, ale nie dotyczy maszyn wirtualnych w stanie wstrzymania.</span><span class="sxs-lookup"><span data-stu-id="67e7b-128">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


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

### <span data-ttu-id="67e7b-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="67e7b-129">-VMScaleSetName</span></span>
<span data-ttu-id="67e7b-130">Określa nazwę VMSS, dla którego to polecenie cmdlet zatrzymuje maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="67e7b-130">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e7b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67e7b-131">-Confirm</span></span>
<span data-ttu-id="67e7b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67e7b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67e7b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e7b-133">-WhatIf</span></span>
<span data-ttu-id="67e7b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67e7b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67e7b-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67e7b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67e7b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e7b-136">CommonParameters</span></span>
<span data-ttu-id="67e7b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e7b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e7b-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e7b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e7b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67e7b-139">INPUTS</span></span>

## <span data-ttu-id="67e7b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67e7b-140">OUTPUTS</span></span>

## <span data-ttu-id="67e7b-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67e7b-141">NOTES</span></span>

## <span data-ttu-id="67e7b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67e7b-142">RELATED LINKS</span></span>

[<span data-ttu-id="67e7b-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="67e7b-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="67e7b-144">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="67e7b-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="67e7b-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="67e7b-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="67e7b-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="67e7b-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="67e7b-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="67e7b-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="67e7b-148">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="67e7b-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="67e7b-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="67e7b-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


