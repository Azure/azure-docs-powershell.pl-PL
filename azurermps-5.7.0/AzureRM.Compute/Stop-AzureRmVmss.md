---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552980"
---
# <span data-ttu-id="faf1d-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf1d-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="faf1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="faf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="faf1d-103">Zatrzymuje VMSS lub zestaw maszyn wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="faf1d-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faf1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="faf1d-104">SYNTAX</span></span>

### <span data-ttu-id="faf1d-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="faf1d-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf1d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="faf1d-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faf1d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="faf1d-107">DESCRIPTION</span></span>
<span data-ttu-id="faf1d-108">Polecenie cmdlet **stop-AzureRmVmss** zatrzymuje wszystkie maszyny wirtualne w zestawie skali maszyny wirtualnej (VMSS) lub zestaw maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="faf1d-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="faf1d-109">W celu wybrania zestawu maszyn wirtualnych można użyć parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="faf1d-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="faf1d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="faf1d-110">EXAMPLES</span></span>

### <span data-ttu-id="faf1d-111">Przykład 1. Zatrzymaj wszystkie maszyny wirtualne w VMSS</span><span class="sxs-lookup"><span data-stu-id="faf1d-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="faf1d-112">To polecenie zatrzymuje wszystkie maszyny wirtualne należące do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="faf1d-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="faf1d-113">Przykład 2: zatrzymywanie określonego zestawu maszyn wirtualnych w VMSS</span><span class="sxs-lookup"><span data-stu-id="faf1d-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="faf1d-114">To polecenie zatrzymuje określony zestaw maszyn wirtualnych określony przez tablicę ciągów identyfikatora wystąpienia, która należy do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="faf1d-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="faf1d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="faf1d-115">PARAMETERS</span></span>

### <span data-ttu-id="faf1d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="faf1d-116">-Force</span></span>
<span data-ttu-id="faf1d-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="faf1d-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf1d-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="faf1d-118">-InstanceId</span></span>
<span data-ttu-id="faf1d-119">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpień maszyny wirtualnej, które zostały zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faf1d-119">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="faf1d-120">Na przykład: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="faf1d-120">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="faf1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="faf1d-122">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="faf1d-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="faf1d-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="faf1d-123">-StayProvisioned</span></span>
<span data-ttu-id="faf1d-124">Jeśli zostanie określona, maszyna wirtualna będzie wprowadzać stan zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="faf1d-124">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="faf1d-125">Jeśli nie zostanie określona, maszyna wirtualna będzie wprowadzać stan wstrzymania.</span><span class="sxs-lookup"><span data-stu-id="faf1d-125">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="faf1d-126">Użytkownik nadal jest obciążany maszyną wirtualną w stanie zatrzymanym, ale nie dotyczy maszyn wirtualnych w stanie wstrzymania.</span><span class="sxs-lookup"><span data-stu-id="faf1d-126">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf1d-127">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="faf1d-127">-VMScaleSetName</span></span>
<span data-ttu-id="faf1d-128">Określa nazwę VMSS, dla którego to polecenie cmdlet zatrzymuje maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="faf1d-128">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="faf1d-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="faf1d-129">-Confirm</span></span>
<span data-ttu-id="faf1d-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faf1d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faf1d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf1d-131">-WhatIf</span></span>
<span data-ttu-id="faf1d-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faf1d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="faf1d-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="faf1d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faf1d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf1d-134">CommonParameters</span></span>
<span data-ttu-id="faf1d-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf1d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf1d-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf1d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf1d-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="faf1d-137">INPUTS</span></span>

### <span data-ttu-id="faf1d-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="faf1d-138">None</span></span>
<span data-ttu-id="faf1d-139">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="faf1d-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="faf1d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="faf1d-140">OUTPUTS</span></span>

## <span data-ttu-id="faf1d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="faf1d-141">NOTES</span></span>

## <span data-ttu-id="faf1d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="faf1d-142">RELATED LINKS</span></span>

[<span data-ttu-id="faf1d-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf1d-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="faf1d-144">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf1d-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="faf1d-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf1d-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="faf1d-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf1d-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="faf1d-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf1d-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="faf1d-148">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf1d-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="faf1d-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="faf1d-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


