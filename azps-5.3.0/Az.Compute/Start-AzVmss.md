---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503933"
---
# <span data-ttu-id="68013-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68013-101">Start-AzVmss</span></span>

## <span data-ttu-id="68013-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68013-102">SYNOPSIS</span></span>
<span data-ttu-id="68013-103">Uruchamia VMSS lub zestaw maszyn wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="68013-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="68013-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68013-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68013-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68013-105">DESCRIPTION</span></span>
<span data-ttu-id="68013-106">Polecenie cmdlet **Start-AzVmss** uruchamia wszystkie maszyny wirtualne w zestawie skali maszyny wirtualnej (VMSS) lub zestaw maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="68013-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="68013-107">W celu wybrania zestawu maszyn wirtualnych można użyć parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="68013-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="68013-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68013-108">EXAMPLES</span></span>

### <span data-ttu-id="68013-109">Przykład 1. Uruchom określony zestaw maszyn wirtualnych w VMSS</span><span class="sxs-lookup"><span data-stu-id="68013-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="68013-110">To polecenie umożliwia uruchomienie określonego zestawu maszyn wirtualnych określonego przez tablicę ciągów identyfikatora wystąpienia, która należy do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="68013-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="68013-111">Przykład 2: uruchamianie wszystkich maszyn wirtualnych w ramach VMSS</span><span class="sxs-lookup"><span data-stu-id="68013-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="68013-112">To polecenie umożliwia uruchomienie wszystkich maszyn wirtualnych należących do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="68013-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="68013-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68013-113">PARAMETERS</span></span>

### <span data-ttu-id="68013-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68013-114">-AsJob</span></span>
<span data-ttu-id="68013-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="68013-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="68013-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68013-116">-DefaultProfile</span></span>
<span data-ttu-id="68013-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68013-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68013-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="68013-118">-InstanceId</span></span>
<span data-ttu-id="68013-119">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpień, które uruchamia polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68013-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="68013-120">Na przykład: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="68013-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="68013-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68013-121">-ResourceGroupName</span></span>
<span data-ttu-id="68013-122">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="68013-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="68013-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="68013-123">-VMScaleSetName</span></span>
<span data-ttu-id="68013-124">Określa nazwę VMSS, którą to polecenie cmdlet uruchamia maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="68013-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="68013-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68013-125">-Confirm</span></span>
<span data-ttu-id="68013-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68013-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68013-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68013-127">-WhatIf</span></span>
<span data-ttu-id="68013-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68013-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68013-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68013-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68013-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68013-130">CommonParameters</span></span>
<span data-ttu-id="68013-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68013-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68013-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68013-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68013-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68013-133">INPUTS</span></span>

### <span data-ttu-id="68013-134">System. String</span><span class="sxs-lookup"><span data-stu-id="68013-134">System.String</span></span>

### <span data-ttu-id="68013-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="68013-135">System.String[]</span></span>

## <span data-ttu-id="68013-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68013-136">OUTPUTS</span></span>

### <span data-ttu-id="68013-137">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="68013-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="68013-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68013-138">NOTES</span></span>

## <span data-ttu-id="68013-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68013-139">RELATED LINKS</span></span>

[<span data-ttu-id="68013-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68013-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="68013-141">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="68013-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="68013-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68013-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="68013-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68013-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="68013-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68013-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="68013-145">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="68013-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="68013-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="68013-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


