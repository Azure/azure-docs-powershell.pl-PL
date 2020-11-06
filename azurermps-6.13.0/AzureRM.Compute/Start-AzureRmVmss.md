---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 131fec8efa9075640d367726e5178caa54b9402a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524530"
---
# <span data-ttu-id="24c06-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="24c06-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="24c06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24c06-102">SYNOPSIS</span></span>
<span data-ttu-id="24c06-103">Uruchamia VMSS lub zestaw maszyn wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="24c06-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24c06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24c06-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24c06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="24c06-105">DESCRIPTION</span></span>
<span data-ttu-id="24c06-106">Polecenie cmdlet **Start-AzureRmVmss** uruchamia wszystkie maszyny wirtualne w zestawie skali maszyny wirtualnej (VMSS) lub zestaw maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="24c06-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="24c06-107">W celu wybrania zestawu maszyn wirtualnych można użyć parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="24c06-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="24c06-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24c06-108">EXAMPLES</span></span>

### <span data-ttu-id="24c06-109">Przykład 1. Uruchom określony zestaw maszyn wirtualnych w VMSS</span><span class="sxs-lookup"><span data-stu-id="24c06-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="24c06-110">To polecenie umożliwia uruchomienie określonego zestawu maszyn wirtualnych określonego przez tablicę ciągów identyfikatora wystąpienia, która należy do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="24c06-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="24c06-111">Przykład 2: uruchamianie wszystkich maszyn wirtualnych w ramach VMSS</span><span class="sxs-lookup"><span data-stu-id="24c06-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="24c06-112">To polecenie umożliwia uruchomienie wszystkich maszyn wirtualnych należących do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="24c06-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="24c06-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24c06-113">PARAMETERS</span></span>

### <span data-ttu-id="24c06-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24c06-114">-AsJob</span></span>
<span data-ttu-id="24c06-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="24c06-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="24c06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c06-116">-DefaultProfile</span></span>
<span data-ttu-id="24c06-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24c06-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24c06-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="24c06-118">-InstanceId</span></span>
<span data-ttu-id="24c06-119">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpień, które uruchamia polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24c06-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="24c06-120">Na przykład: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="24c06-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="24c06-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c06-121">-ResourceGroupName</span></span>
<span data-ttu-id="24c06-122">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="24c06-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="24c06-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="24c06-123">-VMScaleSetName</span></span>
<span data-ttu-id="24c06-124">Określa nazwę VMSS, którą to polecenie cmdlet uruchamia maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="24c06-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="24c06-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24c06-125">-Confirm</span></span>
<span data-ttu-id="24c06-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24c06-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c06-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c06-127">-WhatIf</span></span>
<span data-ttu-id="24c06-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24c06-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24c06-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24c06-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c06-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c06-130">CommonParameters</span></span>
<span data-ttu-id="24c06-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c06-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c06-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c06-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c06-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24c06-133">INPUTS</span></span>

### <span data-ttu-id="24c06-134">System. String</span><span class="sxs-lookup"><span data-stu-id="24c06-134">System.String</span></span>

### <span data-ttu-id="24c06-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="24c06-135">System.String[]</span></span>

## <span data-ttu-id="24c06-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24c06-136">OUTPUTS</span></span>

### <span data-ttu-id="24c06-137">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="24c06-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="24c06-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24c06-138">NOTES</span></span>

## <span data-ttu-id="24c06-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24c06-139">RELATED LINKS</span></span>

[<span data-ttu-id="24c06-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="24c06-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="24c06-141">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="24c06-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="24c06-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="24c06-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="24c06-143">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="24c06-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="24c06-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="24c06-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="24c06-145">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="24c06-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="24c06-146">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="24c06-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


