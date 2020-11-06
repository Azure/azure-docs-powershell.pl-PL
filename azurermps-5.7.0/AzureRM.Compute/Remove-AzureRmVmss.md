---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 9837098586212cfa777c01fcb76a0db05f39eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546859"
---
# <span data-ttu-id="e19e0-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e19e0-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="e19e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e19e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e19e0-103">Usuwa VMSS lub maszynę wirtualną znajdującą się w VMSS.</span><span class="sxs-lookup"><span data-stu-id="e19e0-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e19e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e19e0-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e19e0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e19e0-105">DESCRIPTION</span></span>
<span data-ttu-id="e19e0-106">Polecenie cmdlet **Remove-AzureRmVmss** umożliwia usunięcie zestawu skali maszyny wirtualnej (VMSS) z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e19e0-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="e19e0-107">Za pomocą tego polecenia cmdlet można również usunąć określoną maszynę wirtualną w VMSS.</span><span class="sxs-lookup"><span data-stu-id="e19e0-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="e19e0-108">Za pomocą parametru *InstanceId* można usunąć określoną maszynę wirtualną w VMSS.</span><span class="sxs-lookup"><span data-stu-id="e19e0-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="e19e0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e19e0-109">EXAMPLES</span></span>

### <span data-ttu-id="e19e0-110">Przykład 1: usuwanie VMSS</span><span class="sxs-lookup"><span data-stu-id="e19e0-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="e19e0-111">To polecenie usuwa VMSS o nazwie VMScaleSet001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="e19e0-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="e19e0-112">Przykład 2: usunięcie maszyny wirtualnej z poziomu VMSS</span><span class="sxs-lookup"><span data-stu-id="e19e0-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="e19e0-113">To polecenie powoduje usunięcie maszyny wirtualnej o IDENTYFIKATORze wystąpienia 3 z VMSS o nazwie VMScaleSet002 należącej do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="e19e0-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="e19e0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e19e0-114">PARAMETERS</span></span>

### <span data-ttu-id="e19e0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e19e0-115">-Force</span></span>
<span data-ttu-id="e19e0-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e19e0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e19e0-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e19e0-117">-InstanceId</span></span>
<span data-ttu-id="e19e0-118">Określa jako tablicę ciągów identyfikator wystąpień, które muszą zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e19e0-118">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="e19e0-119">Na przykład: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="e19e0-119">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="e19e0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e19e0-120">-ResourceGroupName</span></span>
<span data-ttu-id="e19e0-121">Określa nazwę grupy zasobów, do której należy VMSS.</span><span class="sxs-lookup"><span data-stu-id="e19e0-121">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="e19e0-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e19e0-122">-VMScaleSetName</span></span>
<span data-ttu-id="e19e0-123">Gatunek nazwa VMSS, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e19e0-123">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="e19e0-124">Jeśli określisz parametr *InstanceId* , polecenie cmdlet usunie określoną maszynę wirtualną z VMSS nazwaną przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e19e0-124">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="e19e0-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e19e0-125">-Confirm</span></span>
<span data-ttu-id="e19e0-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e19e0-126">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="e19e0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e19e0-127">-WhatIf</span></span>
<span data-ttu-id="e19e0-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e19e0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e19e0-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e19e0-129">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="e19e0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19e0-130">CommonParameters</span></span>
<span data-ttu-id="e19e0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e19e0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19e0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e19e0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19e0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e19e0-133">INPUTS</span></span>

### <span data-ttu-id="e19e0-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e19e0-134">None</span></span>
<span data-ttu-id="e19e0-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e19e0-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e19e0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e19e0-136">OUTPUTS</span></span>

## <span data-ttu-id="e19e0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e19e0-137">NOTES</span></span>

## <span data-ttu-id="e19e0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e19e0-138">RELATED LINKS</span></span>

[<span data-ttu-id="e19e0-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e19e0-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="e19e0-140">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e19e0-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="e19e0-141">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e19e0-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="e19e0-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e19e0-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="e19e0-143">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e19e0-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="e19e0-144">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e19e0-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="e19e0-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e19e0-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


