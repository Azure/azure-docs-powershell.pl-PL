---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 35a8ca7832727bef41d588a5551ae1f3efc86180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008058"
---
# <span data-ttu-id="b467b-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b467b-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="b467b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b467b-102">SYNOPSIS</span></span>
<span data-ttu-id="b467b-103">Usuwa rozszerzenie z usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="b467b-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="b467b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b467b-104">SYNTAX</span></span>

### <span data-ttu-id="b467b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b467b-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b467b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b467b-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b467b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b467b-107">DESCRIPTION</span></span>
<span data-ttu-id="b467b-108">Polecenie **cmdlet Remove-AzVmssExtension** usuwa rozszerzenie z zestawu skal maszyny wirtualnej (VIRTUAL Machine Scale Set, MACHINESS).</span><span class="sxs-lookup"><span data-stu-id="b467b-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b467b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b467b-109">EXAMPLES</span></span>

### <span data-ttu-id="b467b-110">Przykład 1. Usuwanie rozszerzenia maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b467b-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="b467b-111">To polecenie usuwa rozszerzenie maszyny wirtualnej i aktualizuje maszyny wirtualne po modyfikacjach.</span><span class="sxs-lookup"><span data-stu-id="b467b-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="b467b-112">Przykład 2. Usuwanie wystąpienia z poziomu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b467b-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="b467b-113">To polecenie usuwa identyfikator rozszerzenia z maszyny wirtualnej należącej do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="b467b-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="b467b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b467b-114">PARAMETERS</span></span>

### <span data-ttu-id="b467b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b467b-115">-DefaultProfile</span></span>
<span data-ttu-id="b467b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b467b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b467b-117">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="b467b-117">-Id</span></span>
<span data-ttu-id="b467b-118">Określa identyfikator rozszerzenia, które to polecenie cmdlet usuwa z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b467b-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467b-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b467b-119">-Name</span></span>
<span data-ttu-id="b467b-120">Określa nazwę rozszerzenia, które to polecenie cmdlet usunie z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b467b-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467b-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b467b-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b467b-122">Określa maszyny wirtualnej, z której ma być usuwane rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="b467b-122">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b467b-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b467b-123">-Confirm</span></span>
<span data-ttu-id="b467b-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b467b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b467b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b467b-125">-WhatIf</span></span>
<span data-ttu-id="b467b-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b467b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b467b-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b467b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b467b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b467b-128">CommonParameters</span></span>
<span data-ttu-id="b467b-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b467b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b467b-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b467b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b467b-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b467b-131">INPUTS</span></span>

### <span data-ttu-id="b467b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b467b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b467b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b467b-133">System.String</span></span>

## <span data-ttu-id="b467b-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b467b-134">OUTPUTS</span></span>

### <span data-ttu-id="b467b-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b467b-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b467b-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b467b-136">NOTES</span></span>

## <span data-ttu-id="b467b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b467b-137">RELATED LINKS</span></span>

[<span data-ttu-id="b467b-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b467b-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
