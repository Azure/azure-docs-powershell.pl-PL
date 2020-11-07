---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2135b6244453cb7d958871c23b64016404d02502
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899126"
---
# <span data-ttu-id="85ddf-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="85ddf-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="85ddf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="85ddf-103">Uruchamia VMSS lub zestaw maszyn wirtualnych w VMSS.</span><span class="sxs-lookup"><span data-stu-id="85ddf-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85ddf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85ddf-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85ddf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85ddf-105">DESCRIPTION</span></span>
<span data-ttu-id="85ddf-106">Polecenie cmdlet **Start-AzureRmVmss** uruchamia wszystkie maszyny wirtualne w zestawie skali maszyny wirtualnej (VMSS) lub zestaw maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="85ddf-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="85ddf-107">W celu wybrania zestawu maszyn wirtualnych można użyć parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="85ddf-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="85ddf-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85ddf-108">EXAMPLES</span></span>

### <span data-ttu-id="85ddf-109">Przykład 1. Uruchom określony zestaw maszyn wirtualnych w VMSS</span><span class="sxs-lookup"><span data-stu-id="85ddf-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="85ddf-110">To polecenie umożliwia uruchomienie określonego zestawu maszyn wirtualnych określonego przez tablicę ciągów identyfikatora wystąpienia, która należy do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="85ddf-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="85ddf-111">Przykład 2: uruchamianie wszystkich maszyn wirtualnych w ramach VMSS</span><span class="sxs-lookup"><span data-stu-id="85ddf-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="85ddf-112">To polecenie umożliwia uruchomienie wszystkich maszyn wirtualnych należących do VMSS o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="85ddf-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="85ddf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85ddf-113">PARAMETERS</span></span>

### <span data-ttu-id="85ddf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85ddf-114">-AsJob</span></span>
<span data-ttu-id="85ddf-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="85ddf-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="85ddf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ddf-116">-DefaultProfile</span></span>
<span data-ttu-id="85ddf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85ddf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85ddf-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="85ddf-118">-InstanceId</span></span>
<span data-ttu-id="85ddf-119">Określa, jako tablicę ciągów, identyfikator lub identyfikatory wystąpień, które uruchamia polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85ddf-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="85ddf-120">Na przykład: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="85ddf-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="85ddf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ddf-121">-ResourceGroupName</span></span>
<span data-ttu-id="85ddf-122">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="85ddf-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="85ddf-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="85ddf-123">-VMScaleSetName</span></span>
<span data-ttu-id="85ddf-124">Określa nazwę VMSS, którą to polecenie cmdlet uruchamia maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="85ddf-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="85ddf-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85ddf-125">-Confirm</span></span>
<span data-ttu-id="85ddf-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85ddf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85ddf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85ddf-127">-WhatIf</span></span>
<span data-ttu-id="85ddf-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85ddf-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85ddf-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85ddf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85ddf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ddf-130">CommonParameters</span></span>
<span data-ttu-id="85ddf-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85ddf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ddf-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85ddf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ddf-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85ddf-133">INPUTS</span></span>

### <span data-ttu-id="85ddf-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="85ddf-134">None</span></span>
<span data-ttu-id="85ddf-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="85ddf-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85ddf-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85ddf-136">OUTPUTS</span></span>

###  
<span data-ttu-id="85ddf-137">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="85ddf-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="85ddf-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85ddf-138">NOTES</span></span>

## <span data-ttu-id="85ddf-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85ddf-139">RELATED LINKS</span></span>

[<span data-ttu-id="85ddf-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="85ddf-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="85ddf-141">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="85ddf-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="85ddf-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="85ddf-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="85ddf-143">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="85ddf-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="85ddf-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="85ddf-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="85ddf-145">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="85ddf-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="85ddf-146">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="85ddf-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


