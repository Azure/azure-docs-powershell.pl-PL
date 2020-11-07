---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 9f4727fc9bc5a735f837d3bec5eced9cd20e9254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719148"
---
# <span data-ttu-id="bffbe-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bffbe-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="bffbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bffbe-102">SYNOPSIS</span></span>
<span data-ttu-id="bffbe-103">Ponowne uruchomienie VMSS lub maszyny wirtualnej w VMSS.</span><span class="sxs-lookup"><span data-stu-id="bffbe-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bffbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bffbe-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bffbe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bffbe-105">DESCRIPTION</span></span>
<span data-ttu-id="bffbe-106">Polecenie cmdlet **restart-AzureRmVmss** powoduje ponowne uruchomienie zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="bffbe-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="bffbe-107">Tego polecenia cmdlet można również użyć w celu ponownego uruchomienia określonej maszyny wirtualnej w VMSS przy użyciu parametru *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="bffbe-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="bffbe-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bffbe-108">EXAMPLES</span></span>

### <span data-ttu-id="bffbe-109">Przykład 1. Uruchom ponownie VMSS</span><span class="sxs-lookup"><span data-stu-id="bffbe-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="bffbe-110">To polecenie uruchamia ponownie VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="bffbe-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="bffbe-111">Przykład 2: ponowne uruchomienie określonej maszyny wirtualnej w obrębie VMSS</span><span class="sxs-lookup"><span data-stu-id="bffbe-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="bffbe-112">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej o IDENTYFIKATORze wystąpienia 1 w VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="bffbe-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="bffbe-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bffbe-113">PARAMETERS</span></span>

### <span data-ttu-id="bffbe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bffbe-114">-AsJob</span></span>
<span data-ttu-id="bffbe-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="bffbe-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bffbe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bffbe-116">-DefaultProfile</span></span>
<span data-ttu-id="bffbe-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bffbe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bffbe-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="bffbe-118">-InstanceId</span></span>
<span data-ttu-id="bffbe-119">Określa jako tablicę ciągów identyfikator wystąpień, które muszą być ponownie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bffbe-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="bffbe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bffbe-120">-ResourceGroupName</span></span>
<span data-ttu-id="bffbe-121">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="bffbe-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="bffbe-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bffbe-122">-VMScaleSetName</span></span>
<span data-ttu-id="bffbe-123">Gatunek nazwa VMSS, które zostanie ponownie rozuruchamiane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bffbe-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="bffbe-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bffbe-124">-Confirm</span></span>
<span data-ttu-id="bffbe-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bffbe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bffbe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bffbe-126">-WhatIf</span></span>
<span data-ttu-id="bffbe-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bffbe-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bffbe-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bffbe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bffbe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bffbe-129">CommonParameters</span></span>
<span data-ttu-id="bffbe-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bffbe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bffbe-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bffbe-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bffbe-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bffbe-132">INPUTS</span></span>

### <span data-ttu-id="bffbe-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bffbe-133">System.String</span></span>

### <span data-ttu-id="bffbe-134">System. String []</span><span class="sxs-lookup"><span data-stu-id="bffbe-134">System.String[]</span></span>

## <span data-ttu-id="bffbe-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bffbe-135">OUTPUTS</span></span>

### <span data-ttu-id="bffbe-136">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="bffbe-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bffbe-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bffbe-137">NOTES</span></span>

## <span data-ttu-id="bffbe-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bffbe-138">RELATED LINKS</span></span>

[<span data-ttu-id="bffbe-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bffbe-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="bffbe-140">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bffbe-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="bffbe-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bffbe-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="bffbe-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bffbe-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="bffbe-143">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bffbe-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="bffbe-144">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bffbe-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="bffbe-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bffbe-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


