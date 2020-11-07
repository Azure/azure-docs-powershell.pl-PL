---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2d33f111928d0b022c7836d0b5c86fb5ec6f203e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898521"
---
# <span data-ttu-id="3457f-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3457f-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="3457f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3457f-102">SYNOPSIS</span></span>
<span data-ttu-id="3457f-103">Ustawia określone akcje na określonym VMSS.</span><span class="sxs-lookup"><span data-stu-id="3457f-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3457f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3457f-104">SYNTAX</span></span>

### <span data-ttu-id="3457f-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3457f-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3457f-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3457f-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3457f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3457f-107">DESCRIPTION</span></span>
<span data-ttu-id="3457f-108">Polecenie cmdlet **Set-AzureRmVmss** ustawia określone akcje na zestawie skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3457f-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="3457f-109">Jedyna akcja obsługiwana przez ten aplet polecenia to Reimage.</span><span class="sxs-lookup"><span data-stu-id="3457f-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="3457f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3457f-110">EXAMPLES</span></span>

### <span data-ttu-id="3457f-111">Przykład 1: odobrazowanie VMSS</span><span class="sxs-lookup"><span data-stu-id="3457f-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="3457f-112">To polecenie powoduje ponowne zdjęcie VMSS o nazwie ContosoVMSS należącej do grupy zasobów o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="3457f-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="3457f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3457f-113">PARAMETERS</span></span>

### <span data-ttu-id="3457f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3457f-114">-AsJob</span></span>
<span data-ttu-id="3457f-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="3457f-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3457f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3457f-116">-DefaultProfile</span></span>
<span data-ttu-id="3457f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3457f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3457f-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3457f-118">-InstanceId</span></span>
<span data-ttu-id="3457f-119">Identyfikator wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3457f-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="3457f-120">-Reimage</span><span class="sxs-lookup"><span data-stu-id="3457f-120">-Reimage</span></span>
<span data-ttu-id="3457f-121">Wskazuje, że polecenie cmdlet reobrazuje VMSS.</span><span class="sxs-lookup"><span data-stu-id="3457f-121">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3457f-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="3457f-122">-ReimageAll</span></span>
<span data-ttu-id="3457f-123">Wskazuje, że polecenie cmdlet reobrazuje wszystkie dyski w VMSS.</span><span class="sxs-lookup"><span data-stu-id="3457f-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="3457f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3457f-124">-ResourceGroupName</span></span>
<span data-ttu-id="3457f-125">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="3457f-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="3457f-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3457f-126">-VMScaleSetName</span></span>
<span data-ttu-id="3457f-127">Gatunek nazwa VMSS, dla którego to polecenie cmdlet ustawia akcje.</span><span class="sxs-lookup"><span data-stu-id="3457f-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="3457f-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3457f-128">-Confirm</span></span>
<span data-ttu-id="3457f-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3457f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3457f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3457f-130">-WhatIf</span></span>
<span data-ttu-id="3457f-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3457f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3457f-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3457f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3457f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3457f-133">CommonParameters</span></span>
<span data-ttu-id="3457f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3457f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3457f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3457f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3457f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3457f-136">INPUTS</span></span>

### <span data-ttu-id="3457f-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3457f-137">None</span></span>
<span data-ttu-id="3457f-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3457f-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3457f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3457f-139">OUTPUTS</span></span>

### <span data-ttu-id="3457f-140">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3457f-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3457f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3457f-141">NOTES</span></span>

## <span data-ttu-id="3457f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3457f-142">RELATED LINKS</span></span>

[<span data-ttu-id="3457f-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3457f-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="3457f-144">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3457f-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="3457f-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3457f-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="3457f-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3457f-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="3457f-147">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3457f-147">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="3457f-148">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3457f-148">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="3457f-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3457f-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


