---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: d3677191bb3a196b97dcb8ff6c5b62b4aafd3a8b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891629"
---
# <span data-ttu-id="95b2a-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95b2a-101">Start-AzVmss</span></span>

## <span data-ttu-id="95b2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="95b2a-103">Uruchamia VMSS lub zestaw maszyn wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="95b2a-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="95b2a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95b2a-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95b2a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95b2a-105">DESCRIPTION</span></span>
<span data-ttu-id="95b2a-106">Polecenie cmdlet **Start-AzVmss** uruchamia wszystkie maszyny wirtualne w zestawie skali maszyny wirtualnej (VMSS) lub zestaw maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="95b2a-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="95b2a-107">W celu wybrania zestawu maszyn wirtualnych można użyć parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="95b2a-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="95b2a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95b2a-108">EXAMPLES</span></span>

### <span data-ttu-id="95b2a-109">Przykład 1. Uruchom określony zestaw maszyn wirtualnych w VMSS</span><span class="sxs-lookup"><span data-stu-id="95b2a-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="95b2a-110">To polecenie umożliwia uruchomienie określonego zestawu maszyn wirtualnych określonego przez tablicę ciągów identyfikatora wystąpienia, która należy do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="95b2a-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="95b2a-111">Przykład 2: uruchamianie wszystkich maszyn wirtualnych w ramach VMSS</span><span class="sxs-lookup"><span data-stu-id="95b2a-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="95b2a-112">To polecenie umożliwia uruchomienie wszystkich maszyn wirtualnych należących do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="95b2a-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="95b2a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95b2a-113">PARAMETERS</span></span>

### <span data-ttu-id="95b2a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95b2a-114">-AsJob</span></span>
<span data-ttu-id="95b2a-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="95b2a-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="95b2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b2a-116">-DefaultProfile</span></span>
<span data-ttu-id="95b2a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="95b2a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95b2a-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="95b2a-118">-InstanceId</span></span>
<span data-ttu-id="95b2a-119">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpień, które uruchamia polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95b2a-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="95b2a-120">Na przykład: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="95b2a-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="95b2a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95b2a-121">-ResourceGroupName</span></span>
<span data-ttu-id="95b2a-122">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="95b2a-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="95b2a-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="95b2a-123">-VMScaleSetName</span></span>
<span data-ttu-id="95b2a-124">Określa nazwę VMSS, którą to polecenie cmdlet uruchamia maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="95b2a-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="95b2a-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95b2a-125">-Confirm</span></span>
<span data-ttu-id="95b2a-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95b2a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95b2a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95b2a-127">-WhatIf</span></span>
<span data-ttu-id="95b2a-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95b2a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95b2a-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="95b2a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95b2a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b2a-130">CommonParameters</span></span>
<span data-ttu-id="95b2a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95b2a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b2a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b2a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b2a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95b2a-133">INPUTS</span></span>

### <span data-ttu-id="95b2a-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="95b2a-134">None</span></span>
<span data-ttu-id="95b2a-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="95b2a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95b2a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95b2a-136">OUTPUTS</span></span>

###  
<span data-ttu-id="95b2a-137">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="95b2a-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="95b2a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95b2a-138">NOTES</span></span>

## <span data-ttu-id="95b2a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95b2a-139">RELATED LINKS</span></span>

[<span data-ttu-id="95b2a-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95b2a-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="95b2a-141">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="95b2a-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="95b2a-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95b2a-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="95b2a-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95b2a-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="95b2a-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95b2a-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="95b2a-145">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="95b2a-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="95b2a-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="95b2a-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


