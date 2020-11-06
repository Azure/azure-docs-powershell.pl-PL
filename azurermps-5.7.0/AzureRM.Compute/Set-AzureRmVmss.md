---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: e3b053d4e8e9ccf9c68d8eb5fabe479f7f58ced1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546855"
---
# <span data-ttu-id="3ed45-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ed45-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="3ed45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ed45-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed45-103">Ustawia określone akcje na określonym VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ed45-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ed45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ed45-104">SYNTAX</span></span>

### <span data-ttu-id="3ed45-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3ed45-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Reimage] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ed45-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3ed45-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-ReimageAll] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ed45-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3ed45-107">DESCRIPTION</span></span>
<span data-ttu-id="3ed45-108">Polecenie cmdlet **Set-AzureRmVmss** ustawia określone akcje na zestawie skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3ed45-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="3ed45-109">Jedyna akcja obsługiwana przez ten aplet polecenia to Reimage.</span><span class="sxs-lookup"><span data-stu-id="3ed45-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="3ed45-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ed45-110">EXAMPLES</span></span>

### <span data-ttu-id="3ed45-111">Przykład 1: odobrazowanie VMSS</span><span class="sxs-lookup"><span data-stu-id="3ed45-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="3ed45-112">To polecenie powoduje ponowne zdjęcie VMSS o nazwie ContosoVMSS należącej do grupy zasobów o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="3ed45-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="3ed45-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ed45-113">PARAMETERS</span></span>

### <span data-ttu-id="3ed45-114">-Reimage</span><span class="sxs-lookup"><span data-stu-id="3ed45-114">-Reimage</span></span>
<span data-ttu-id="3ed45-115">Wskazuje, że polecenie cmdlet reobrazuje VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ed45-115">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed45-116">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="3ed45-116">-ReimageAll</span></span>
<span data-ttu-id="3ed45-117">Wskazuje, że polecenie cmdlet reobrazuje wszystkie dyski w VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ed45-117">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ed45-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed45-118">-ResourceGroupName</span></span>
<span data-ttu-id="3ed45-119">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ed45-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="3ed45-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3ed45-120">-VMScaleSetName</span></span>
<span data-ttu-id="3ed45-121">Gatunek nazwa VMSS, dla którego to polecenie cmdlet ustawia akcje.</span><span class="sxs-lookup"><span data-stu-id="3ed45-121">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="3ed45-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ed45-122">-Confirm</span></span>
<span data-ttu-id="3ed45-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ed45-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ed45-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ed45-124">-WhatIf</span></span>
<span data-ttu-id="3ed45-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ed45-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ed45-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3ed45-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ed45-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed45-127">CommonParameters</span></span>
<span data-ttu-id="3ed45-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ed45-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed45-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ed45-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed45-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ed45-130">INPUTS</span></span>

### <span data-ttu-id="3ed45-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3ed45-131">None</span></span>
<span data-ttu-id="3ed45-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3ed45-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ed45-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ed45-133">OUTPUTS</span></span>

### <span data-ttu-id="3ed45-134">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3ed45-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3ed45-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ed45-135">NOTES</span></span>

## <span data-ttu-id="3ed45-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ed45-136">RELATED LINKS</span></span>

[<span data-ttu-id="3ed45-137">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ed45-137">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="3ed45-138">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ed45-138">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="3ed45-139">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ed45-139">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="3ed45-140">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ed45-140">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="3ed45-141">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ed45-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="3ed45-142">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ed45-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="3ed45-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3ed45-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


