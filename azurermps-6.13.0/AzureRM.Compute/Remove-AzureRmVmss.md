---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 54c6f9f399cfabf7a418939b4662c9bcfdc83d34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551347"
---
# <span data-ttu-id="2b3ff-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b3ff-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="2b3ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3ff-103">Usuwa VMSS lub maszynę wirtualną znajdującą się w VMSS.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b3ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b3ff-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b3ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b3ff-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3ff-106">Polecenie cmdlet **Remove-AzureRmVmss** umożliwia usunięcie zestawu skali maszyny wirtualnej (VMSS) z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="2b3ff-107">Za pomocą tego polecenia cmdlet można również usunąć określoną maszynę wirtualną w VMSS.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="2b3ff-108">Za pomocą parametru *InstanceId* można usunąć określoną maszynę wirtualną w VMSS.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="2b3ff-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b3ff-109">EXAMPLES</span></span>

### <span data-ttu-id="2b3ff-110">Przykład 1: usuwanie VMSS</span><span class="sxs-lookup"><span data-stu-id="2b3ff-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="2b3ff-111">To polecenie usuwa VMSS o nazwie VMScaleSet001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="2b3ff-112">Przykład 2: usunięcie maszyny wirtualnej z poziomu VMSS</span><span class="sxs-lookup"><span data-stu-id="2b3ff-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="2b3ff-113">To polecenie powoduje usunięcie maszyny wirtualnej o IDENTYFIKATORze wystąpienia 3 z VMSS o nazwie VMScaleSet002 należącej do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="2b3ff-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b3ff-114">PARAMETERS</span></span>

### <span data-ttu-id="2b3ff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b3ff-115">-AsJob</span></span>
<span data-ttu-id="2b3ff-116">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2b3ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3ff-117">-DefaultProfile</span></span>
<span data-ttu-id="2b3ff-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b3ff-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2b3ff-119">-Force</span></span>
<span data-ttu-id="2b3ff-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b3ff-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2b3ff-121">-InstanceId</span></span>
<span data-ttu-id="2b3ff-122">Określa jako tablicę ciągów identyfikator wystąpień, które muszą zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="2b3ff-123">Na przykład: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="2b3ff-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="2b3ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b3ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b3ff-125">Określa nazwę grupy zasobów, do której należy VMSS.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="2b3ff-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2b3ff-126">-VMScaleSetName</span></span>
<span data-ttu-id="2b3ff-127">Gatunek nazwa VMSS, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="2b3ff-128">Jeśli określisz parametr *InstanceId* , polecenie cmdlet usunie określoną maszynę wirtualną z VMSS nazwaną przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="2b3ff-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b3ff-129">-Confirm</span></span>
<span data-ttu-id="2b3ff-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3ff-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b3ff-131">-WhatIf</span></span>
<span data-ttu-id="2b3ff-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b3ff-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3ff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3ff-134">CommonParameters</span></span>
<span data-ttu-id="2b3ff-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b3ff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3ff-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b3ff-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3ff-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b3ff-137">INPUTS</span></span>

### <span data-ttu-id="2b3ff-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2b3ff-138">System.String</span></span>

### <span data-ttu-id="2b3ff-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="2b3ff-139">System.String[]</span></span>

## <span data-ttu-id="2b3ff-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b3ff-140">OUTPUTS</span></span>

### <span data-ttu-id="2b3ff-141">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2b3ff-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2b3ff-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b3ff-142">NOTES</span></span>

## <span data-ttu-id="2b3ff-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b3ff-143">RELATED LINKS</span></span>

[<span data-ttu-id="2b3ff-144">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b3ff-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="2b3ff-145">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b3ff-145">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="2b3ff-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b3ff-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="2b3ff-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b3ff-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="2b3ff-148">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b3ff-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="2b3ff-149">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b3ff-149">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="2b3ff-150">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b3ff-150">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


