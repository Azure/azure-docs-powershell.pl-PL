---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 7ede92fa653fe04072b75ce03dd6928421e01c6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524541"
---
# <span data-ttu-id="08bfd-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="08bfd-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="08bfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="08bfd-103">Usuwa rozszerzenie z VMSS.</span><span class="sxs-lookup"><span data-stu-id="08bfd-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08bfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08bfd-104">SYNTAX</span></span>

### <span data-ttu-id="08bfd-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08bfd-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08bfd-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08bfd-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08bfd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="08bfd-107">DESCRIPTION</span></span>
<span data-ttu-id="08bfd-108">Polecenie cmdlet **Remove-AzureRmVmssExtension** usuwa rozszerzenie z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="08bfd-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="08bfd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08bfd-109">EXAMPLES</span></span>

### <span data-ttu-id="08bfd-110">Przykład 1: Usuwanie rozszerzenia VMSS</span><span class="sxs-lookup"><span data-stu-id="08bfd-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzureRmVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="08bfd-111">To polecenie usuwa rozszerzenie VMSS i aktualizuje VMSS po modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="08bfd-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="08bfd-112">Przykład 2: usuwanie wystąpienia z wewnątrz elementu VMSS</span><span class="sxs-lookup"><span data-stu-id="08bfd-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzureRmVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="08bfd-113">To polecenie usuwa identyfikator rozszerzenia z VMSS należącego do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="08bfd-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="08bfd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08bfd-114">PARAMETERS</span></span>

### <span data-ttu-id="08bfd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bfd-115">-DefaultProfile</span></span>
<span data-ttu-id="08bfd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08bfd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08bfd-117">-ID</span><span class="sxs-lookup"><span data-stu-id="08bfd-117">-Id</span></span>
<span data-ttu-id="08bfd-118">Określa identyfikator rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="08bfd-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="08bfd-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08bfd-119">-Name</span></span>
<span data-ttu-id="08bfd-120">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="08bfd-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="08bfd-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="08bfd-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="08bfd-122">Określa VMSS, z którego ma zostać usunięte rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="08bfd-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="08bfd-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08bfd-123">-Confirm</span></span>
<span data-ttu-id="08bfd-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08bfd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08bfd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08bfd-125">-WhatIf</span></span>
<span data-ttu-id="08bfd-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08bfd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08bfd-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08bfd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08bfd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bfd-128">CommonParameters</span></span>
<span data-ttu-id="08bfd-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08bfd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bfd-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08bfd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bfd-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08bfd-131">INPUTS</span></span>

### <span data-ttu-id="08bfd-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="08bfd-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="08bfd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="08bfd-133">System.String</span></span>

## <span data-ttu-id="08bfd-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08bfd-134">OUTPUTS</span></span>

### <span data-ttu-id="08bfd-135">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="08bfd-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="08bfd-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08bfd-136">NOTES</span></span>

## <span data-ttu-id="08bfd-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08bfd-137">RELATED LINKS</span></span>

[<span data-ttu-id="08bfd-138">Dodaj-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="08bfd-138">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
