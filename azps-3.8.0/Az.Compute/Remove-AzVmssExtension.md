---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: ceca2477d66cb6ce19564899e67a3b66d6917cfe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052623"
---
# <span data-ttu-id="a6851-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a6851-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="a6851-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6851-102">SYNOPSIS</span></span>
<span data-ttu-id="a6851-103">Usuwa rozszerzenie z VMSS.</span><span class="sxs-lookup"><span data-stu-id="a6851-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="a6851-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6851-104">SYNTAX</span></span>

### <span data-ttu-id="a6851-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6851-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6851-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6851-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6851-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a6851-107">DESCRIPTION</span></span>
<span data-ttu-id="a6851-108">Polecenie cmdlet **Remove-AzVmssExtension** usuwa rozszerzenie z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a6851-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a6851-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6851-109">EXAMPLES</span></span>

### <span data-ttu-id="a6851-110">Przykład 1: Usuwanie rozszerzenia VMSS</span><span class="sxs-lookup"><span data-stu-id="a6851-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="a6851-111">To polecenie usuwa rozszerzenie VMSS i aktualizuje VMSS po modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="a6851-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="a6851-112">Przykład 2: usuwanie wystąpienia z wewnątrz elementu VMSS</span><span class="sxs-lookup"><span data-stu-id="a6851-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="a6851-113">To polecenie usuwa identyfikator rozszerzenia z VMSS należącego do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="a6851-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="a6851-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6851-114">PARAMETERS</span></span>

### <span data-ttu-id="a6851-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6851-115">-DefaultProfile</span></span>
<span data-ttu-id="a6851-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6851-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6851-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a6851-117">-Id</span></span>
<span data-ttu-id="a6851-118">Określa identyfikator rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="a6851-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a6851-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6851-119">-Name</span></span>
<span data-ttu-id="a6851-120">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="a6851-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a6851-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a6851-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a6851-122">Określa VMSS, z którego ma zostać usunięte rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="a6851-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="a6851-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6851-123">-Confirm</span></span>
<span data-ttu-id="a6851-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6851-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6851-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6851-125">-WhatIf</span></span>
<span data-ttu-id="a6851-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6851-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6851-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a6851-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6851-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6851-128">CommonParameters</span></span>
<span data-ttu-id="a6851-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6851-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6851-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6851-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6851-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6851-131">INPUTS</span></span>

### <span data-ttu-id="a6851-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a6851-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a6851-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a6851-133">System.String</span></span>

## <span data-ttu-id="a6851-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6851-134">OUTPUTS</span></span>

### <span data-ttu-id="a6851-135">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a6851-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a6851-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6851-136">NOTES</span></span>

## <span data-ttu-id="a6851-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6851-137">RELATED LINKS</span></span>

[<span data-ttu-id="a6851-138">Dodaj-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a6851-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
