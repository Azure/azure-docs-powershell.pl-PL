---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 5ceb420f30525817ebccd6d3f38a53e6c1cad66e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893333"
---
# <span data-ttu-id="185b0-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="185b0-101">Set-AzVmss</span></span>

## <span data-ttu-id="185b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="185b0-102">SYNOPSIS</span></span>
<span data-ttu-id="185b0-103">Ustawia określone akcje na określonym VMSS.</span><span class="sxs-lookup"><span data-stu-id="185b0-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="185b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="185b0-104">SYNTAX</span></span>

### <span data-ttu-id="185b0-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="185b0-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="185b0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="185b0-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="185b0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="185b0-107">DESCRIPTION</span></span>
<span data-ttu-id="185b0-108">Polecenie cmdlet **Set-AzVmss** ustawia określone akcje na zestawie skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="185b0-108">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="185b0-109">Jedyna akcja obsługiwana przez ten aplet polecenia to Reimage.</span><span class="sxs-lookup"><span data-stu-id="185b0-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="185b0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="185b0-110">EXAMPLES</span></span>

### <span data-ttu-id="185b0-111">Przykład 1: odobrazowanie VMSS</span><span class="sxs-lookup"><span data-stu-id="185b0-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="185b0-112">To polecenie powoduje ponowne zdjęcie VMSS o nazwie ContosoVMSS należącej do grupy zasobów o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="185b0-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="185b0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="185b0-113">PARAMETERS</span></span>

### <span data-ttu-id="185b0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="185b0-114">-AsJob</span></span>
<span data-ttu-id="185b0-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="185b0-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="185b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185b0-116">-DefaultProfile</span></span>
<span data-ttu-id="185b0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="185b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="185b0-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="185b0-118">-InstanceId</span></span>
<span data-ttu-id="185b0-119">Identyfikator wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="185b0-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="185b0-120">-Reimage</span><span class="sxs-lookup"><span data-stu-id="185b0-120">-Reimage</span></span>
<span data-ttu-id="185b0-121">Wskazuje, że polecenie cmdlet reobrazuje VMSS.</span><span class="sxs-lookup"><span data-stu-id="185b0-121">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="185b0-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="185b0-122">-ReimageAll</span></span>
<span data-ttu-id="185b0-123">Wskazuje, że polecenie cmdlet reobrazuje wszystkie dyski w VMSS.</span><span class="sxs-lookup"><span data-stu-id="185b0-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="185b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="185b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="185b0-125">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="185b0-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="185b0-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="185b0-126">-VMScaleSetName</span></span>
<span data-ttu-id="185b0-127">Gatunek nazwa VMSS, dla którego to polecenie cmdlet ustawia akcje.</span><span class="sxs-lookup"><span data-stu-id="185b0-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="185b0-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="185b0-128">-Confirm</span></span>
<span data-ttu-id="185b0-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="185b0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="185b0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="185b0-130">-WhatIf</span></span>
<span data-ttu-id="185b0-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="185b0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="185b0-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="185b0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="185b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185b0-133">CommonParameters</span></span>
<span data-ttu-id="185b0-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="185b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185b0-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="185b0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185b0-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="185b0-136">INPUTS</span></span>

### <span data-ttu-id="185b0-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="185b0-137">None</span></span>
<span data-ttu-id="185b0-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="185b0-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="185b0-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="185b0-139">OUTPUTS</span></span>

### <span data-ttu-id="185b0-140">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="185b0-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="185b0-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="185b0-141">NOTES</span></span>

## <span data-ttu-id="185b0-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="185b0-142">RELATED LINKS</span></span>

[<span data-ttu-id="185b0-143">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="185b0-143">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="185b0-144">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="185b0-144">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="185b0-145">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="185b0-145">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="185b0-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="185b0-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="185b0-147">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="185b0-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="185b0-148">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="185b0-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="185b0-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="185b0-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


