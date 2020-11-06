---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 4511aadaad23e47018a12365f6fb8fb346117b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525238"
---
# <span data-ttu-id="64793-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="64793-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="64793-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64793-102">SYNOPSIS</span></span>
<span data-ttu-id="64793-103">Aktualizuje stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="64793-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64793-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64793-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64793-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64793-105">DESCRIPTION</span></span>
<span data-ttu-id="64793-106">Polecenie cmdlet **Update-AzureRmVmss** powoduje zaktualizowanie stanu zestawu skali maszyny wirtualnej (VMSS) do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="64793-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="64793-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64793-107">EXAMPLES</span></span>

### <span data-ttu-id="64793-108">Przykład 1: aktualizowanie stanu VMSS do stanu lokalnego obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="64793-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="64793-109">To polecenie aktualizuje stan VMSS o nazwie VMSS001 należącego do grupy zasobów o nazwie Group001 do stanu lokalnego obiektu VMSS o nazwie LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="64793-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="64793-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64793-110">PARAMETERS</span></span>

### <span data-ttu-id="64793-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64793-111">-ResourceGroupName</span></span>
<span data-ttu-id="64793-112">Określa nazwę grupy zasobów, do której należy VMSS.</span><span class="sxs-lookup"><span data-stu-id="64793-112">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="64793-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64793-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="64793-114">Określa lokalny obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="64793-114">Specifies a local VMSS object.</span></span>
<span data-ttu-id="64793-115">Aby uzyskać obiekt VMSS, użyj polecenia cmdlet Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="64793-115">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="64793-116">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan VMSS.</span><span class="sxs-lookup"><span data-stu-id="64793-116">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64793-117">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="64793-117">-VMScaleSetName</span></span>
<span data-ttu-id="64793-118">Określa nazwę VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64793-118">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64793-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64793-119">-Confirm</span></span>
<span data-ttu-id="64793-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64793-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64793-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64793-121">-WhatIf</span></span>
<span data-ttu-id="64793-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64793-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="64793-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64793-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64793-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64793-124">CommonParameters</span></span>
<span data-ttu-id="64793-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64793-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64793-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64793-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64793-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64793-127">INPUTS</span></span>

### <span data-ttu-id="64793-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="64793-128">None</span></span>
<span data-ttu-id="64793-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="64793-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64793-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64793-130">OUTPUTS</span></span>

## <span data-ttu-id="64793-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64793-131">NOTES</span></span>

## <span data-ttu-id="64793-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64793-132">RELATED LINKS</span></span>

[<span data-ttu-id="64793-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="64793-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="64793-134">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="64793-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="64793-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="64793-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="64793-136">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="64793-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="64793-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="64793-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="64793-138">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="64793-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="64793-139">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="64793-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


