---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 58a45d6f9e3a24ca11c298935fc0d9676617737e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986161"
---
# <span data-ttu-id="32537-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="32537-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="32537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32537-102">SYNOPSIS</span></span>
<span data-ttu-id="32537-103">Ustawia profil diagnostyki rozruchu zestawu skal maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32537-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="32537-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="32537-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32537-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="32537-105">DESCRIPTION</span></span>
<span data-ttu-id="32537-106">Ustawia profil diagnostyki rozruchu zestawu skal maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32537-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="32537-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="32537-107">EXAMPLES</span></span>

### <span data-ttu-id="32537-108">Przykład 1. Ustawianie właściwości profilu diagnostycznego rozruchu dla usługi MASZYNY WIRTUALNE</span><span class="sxs-lookup"><span data-stu-id="32537-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="32537-109">To polecenie ustawia właściwość profilu diagnostycznego rozruchu dla usług maszyny wirtualnej o nazwie ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="32537-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="32537-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32537-110">PARAMETERS</span></span>

### <span data-ttu-id="32537-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32537-111">-DefaultProfile</span></span>
<span data-ttu-id="32537-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="32537-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32537-113">— włączone</span><span class="sxs-lookup"><span data-stu-id="32537-113">-Enabled</span></span>
<span data-ttu-id="32537-114">Czy diagnostyka rozruchu powinna być włączona na zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="32537-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="32537-115">— StorageUri</span><span class="sxs-lookup"><span data-stu-id="32537-115">-StorageUri</span></span>
<span data-ttu-id="32537-116">URI konta magazynu, które ma być służące do umieszczania danych wyjściowych konsoli i zrzutu ekranu.</span><span class="sxs-lookup"><span data-stu-id="32537-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="32537-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32537-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="32537-118">Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="32537-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="32537-119">Obiekt można New-AzVmssConfig za pomocą polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32537-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="32537-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="32537-120">-Confirm</span></span>
<span data-ttu-id="32537-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="32537-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32537-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32537-122">-WhatIf</span></span>
<span data-ttu-id="32537-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32537-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32537-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="32537-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32537-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32537-125">CommonParameters</span></span>
<span data-ttu-id="32537-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32537-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32537-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32537-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32537-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32537-128">INPUTS</span></span>

### <span data-ttu-id="32537-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32537-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="32537-130">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32537-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="32537-131">System.String</span><span class="sxs-lookup"><span data-stu-id="32537-131">System.String</span></span>

## <span data-ttu-id="32537-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32537-132">OUTPUTS</span></span>

### <span data-ttu-id="32537-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32537-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="32537-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="32537-134">NOTES</span></span>

## <span data-ttu-id="32537-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32537-135">RELATED LINKS</span></span>
