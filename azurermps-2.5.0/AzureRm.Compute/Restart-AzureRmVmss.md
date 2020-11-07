---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 6582b8d0a141522e6ac8bb4dad23f1da5e31000d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899140"
---
# <span data-ttu-id="13d04-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13d04-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="13d04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13d04-102">SYNOPSIS</span></span>
<span data-ttu-id="13d04-103">Ponowne uruchomienie VMSS lub maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="13d04-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13d04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13d04-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13d04-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13d04-105">DESCRIPTION</span></span>
<span data-ttu-id="13d04-106">Polecenie cmdlet **restart-AzureRmVmss** powoduje ponowne uruchomienie zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="13d04-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="13d04-107">Tego polecenia cmdlet można również użyć w celu ponownego uruchomienia określonej maszyny wirtualnej w VMSS przy użyciu parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="13d04-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="13d04-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13d04-108">EXAMPLES</span></span>

### <span data-ttu-id="13d04-109">Przykład 1. Uruchom ponownie VMSS</span><span class="sxs-lookup"><span data-stu-id="13d04-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="13d04-110">To polecenie uruchamia ponownie VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="13d04-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="13d04-111">Przykład 2: ponowne uruchomienie określonej maszyny wirtualnej w obrębie VMSS</span><span class="sxs-lookup"><span data-stu-id="13d04-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="13d04-112">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o IDENTYFIKATORze wystąpienia 1 w VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="13d04-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="13d04-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13d04-113">PARAMETERS</span></span>

### <span data-ttu-id="13d04-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13d04-114">-AsJob</span></span>
<span data-ttu-id="13d04-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="13d04-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="13d04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d04-116">-DefaultProfile</span></span>
<span data-ttu-id="13d04-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13d04-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13d04-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="13d04-118">-InstanceId</span></span>
<span data-ttu-id="13d04-119">Określa jako tablicę ciągów identyfikator wystąpień, które muszą być ponownie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="13d04-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="13d04-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d04-120">-ResourceGroupName</span></span>
<span data-ttu-id="13d04-121">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="13d04-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="13d04-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="13d04-122">-VMScaleSetName</span></span>
<span data-ttu-id="13d04-123">Gatunek nazwa VMSS, które zostanie ponownie rozuruchamiane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13d04-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="13d04-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13d04-124">-Confirm</span></span>
<span data-ttu-id="13d04-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13d04-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13d04-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13d04-126">-WhatIf</span></span>
<span data-ttu-id="13d04-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13d04-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13d04-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13d04-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13d04-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d04-129">CommonParameters</span></span>
<span data-ttu-id="13d04-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13d04-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d04-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d04-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d04-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13d04-132">INPUTS</span></span>

### <span data-ttu-id="13d04-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="13d04-133">None</span></span>
<span data-ttu-id="13d04-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="13d04-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="13d04-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13d04-135">OUTPUTS</span></span>

###  
<span data-ttu-id="13d04-136">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="13d04-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="13d04-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13d04-137">NOTES</span></span>

## <span data-ttu-id="13d04-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13d04-138">RELATED LINKS</span></span>

[<span data-ttu-id="13d04-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13d04-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="13d04-140">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13d04-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="13d04-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13d04-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="13d04-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13d04-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="13d04-143">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13d04-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="13d04-144">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13d04-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="13d04-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13d04-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


