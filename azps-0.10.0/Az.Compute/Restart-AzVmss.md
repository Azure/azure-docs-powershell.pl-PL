---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: b0e01f462bfb7576e942138cb42b3171fb6660b3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893477"
---
# <span data-ttu-id="36651-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36651-101">Restart-AzVmss</span></span>

## <span data-ttu-id="36651-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36651-102">SYNOPSIS</span></span>
<span data-ttu-id="36651-103">Ponowne uruchomienie VMSS lub maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="36651-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="36651-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36651-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36651-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36651-105">DESCRIPTION</span></span>
<span data-ttu-id="36651-106">Polecenie cmdlet **restart-AzVmss** powoduje ponowne uruchomienie zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="36651-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="36651-107">Tego polecenia cmdlet można również użyć w celu ponownego uruchomienia określonej maszyny wirtualnej w VMSS przy użyciu parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="36651-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="36651-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36651-108">EXAMPLES</span></span>

### <span data-ttu-id="36651-109">Przykład 1. Uruchom ponownie VMSS</span><span class="sxs-lookup"><span data-stu-id="36651-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="36651-110">To polecenie uruchamia ponownie VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="36651-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="36651-111">Przykład 2: ponowne uruchomienie określonej maszyny wirtualnej w obrębie VMSS</span><span class="sxs-lookup"><span data-stu-id="36651-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="36651-112">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o IDENTYFIKATORze wystąpienia 1 w VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="36651-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="36651-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36651-113">PARAMETERS</span></span>

### <span data-ttu-id="36651-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36651-114">-AsJob</span></span>
<span data-ttu-id="36651-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="36651-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="36651-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36651-116">-DefaultProfile</span></span>
<span data-ttu-id="36651-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36651-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36651-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="36651-118">-InstanceId</span></span>
<span data-ttu-id="36651-119">Określa jako tablicę ciągów identyfikator wystąpień, które muszą być ponownie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="36651-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="36651-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36651-120">-ResourceGroupName</span></span>
<span data-ttu-id="36651-121">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="36651-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="36651-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="36651-122">-VMScaleSetName</span></span>
<span data-ttu-id="36651-123">Gatunek nazwa VMSS, które zostanie ponownie rozuruchamiane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36651-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="36651-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36651-124">-Confirm</span></span>
<span data-ttu-id="36651-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36651-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36651-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36651-126">-WhatIf</span></span>
<span data-ttu-id="36651-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36651-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36651-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36651-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36651-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36651-129">CommonParameters</span></span>
<span data-ttu-id="36651-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36651-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36651-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36651-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36651-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36651-132">INPUTS</span></span>

### <span data-ttu-id="36651-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="36651-133">None</span></span>
<span data-ttu-id="36651-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="36651-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36651-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36651-135">OUTPUTS</span></span>

###  
<span data-ttu-id="36651-136">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="36651-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="36651-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36651-137">NOTES</span></span>

## <span data-ttu-id="36651-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36651-138">RELATED LINKS</span></span>

[<span data-ttu-id="36651-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36651-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="36651-140">Nowe — AzVmss</span><span class="sxs-lookup"><span data-stu-id="36651-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="36651-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36651-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="36651-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36651-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="36651-143">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="36651-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="36651-144">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="36651-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="36651-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="36651-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


