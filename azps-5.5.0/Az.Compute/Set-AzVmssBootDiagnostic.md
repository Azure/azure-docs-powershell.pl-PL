---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196954"
---
# <span data-ttu-id="b8829-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b8829-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="b8829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8829-102">SYNOPSIS</span></span>
<span data-ttu-id="b8829-103">Ustawia profil diagnostyki rozruchu zestawu skal maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b8829-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="b8829-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8829-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8829-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8829-105">DESCRIPTION</span></span>
<span data-ttu-id="b8829-106">Ustawia profil diagnostyki rozruchu zestawu skal maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b8829-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="b8829-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8829-107">EXAMPLES</span></span>

### <span data-ttu-id="b8829-108">Przykład 1. Ustawianie właściwości profilu diagnostycznego rozruchu dla usługi MASZYNY WIRTUALNE</span><span class="sxs-lookup"><span data-stu-id="b8829-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="b8829-109">To polecenie ustawia właściwość profilu diagnostycznego rozruchu dla maszyn wirtualnych o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="b8829-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="b8829-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8829-110">PARAMETERS</span></span>

### <span data-ttu-id="b8829-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8829-111">-DefaultProfile</span></span>
<span data-ttu-id="b8829-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8829-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8829-113">— włączone</span><span class="sxs-lookup"><span data-stu-id="b8829-113">-Enabled</span></span>
<span data-ttu-id="b8829-114">Czy diagnostyka rozruchu powinna być włączona na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b8829-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8829-115">— StorageUri</span><span class="sxs-lookup"><span data-stu-id="b8829-115">-StorageUri</span></span>
<span data-ttu-id="b8829-116">URI konta magazynu, które ma być służące do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="b8829-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8829-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b8829-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b8829-118">Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="b8829-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="b8829-119">Aby utworzyć obiekt, New-AzVmssConfig użyć polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8829-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="b8829-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8829-120">-Confirm</span></span>
<span data-ttu-id="b8829-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8829-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8829-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8829-122">-WhatIf</span></span>
<span data-ttu-id="b8829-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8829-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8829-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b8829-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8829-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8829-125">CommonParameters</span></span>
<span data-ttu-id="b8829-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8829-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8829-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8829-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8829-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8829-128">INPUTS</span></span>

### <span data-ttu-id="b8829-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b8829-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b8829-130">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8829-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b8829-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b8829-131">System.String</span></span>

## <span data-ttu-id="b8829-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b8829-132">OUTPUTS</span></span>

### <span data-ttu-id="b8829-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b8829-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b8829-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8829-134">NOTES</span></span>

## <span data-ttu-id="b8829-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8829-135">RELATED LINKS</span></span>
