---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177546"
---
# <span data-ttu-id="87b53-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="87b53-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="87b53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87b53-102">SYNOPSIS</span></span>
<span data-ttu-id="87b53-103">Usuwa program obsługi rozszerzenia DSC z maszyny wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="87b53-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="87b53-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87b53-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87b53-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="87b53-105">DESCRIPTION</span></span>
<span data-ttu-id="87b53-106">Polecenie cmdlet **Remove-AzVMDscExtension** usuwa program obsługi rozszerzenia Pożądany stan konfiguracji (DSC) z maszyny wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="87b53-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="87b53-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87b53-107">EXAMPLES</span></span>

### <span data-ttu-id="87b53-108">Przykład 1. Usuwanie rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="87b53-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="87b53-109">To polecenie usuwa rozszerzenie o nazwie DSC na maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJ07.</span><span class="sxs-lookup"><span data-stu-id="87b53-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="87b53-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87b53-110">PARAMETERS</span></span>

### <span data-ttu-id="87b53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b53-111">-DefaultProfile</span></span>
<span data-ttu-id="87b53-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="87b53-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b53-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="87b53-113">-Name</span></span>
<span data-ttu-id="87b53-114">Określa nazwę rozszerzenia DSC, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87b53-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="87b53-115">Polecenie Set-AzVMDscExtension ustawia tę nazwę na Microsoft.Powershell.DSC, która jest wartością domyślną używaną przez **polecenie Remove-AzVMDscExtension.**</span><span class="sxs-lookup"><span data-stu-id="87b53-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="87b53-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="87b53-116">-NoWait</span></span>
<span data-ttu-id="87b53-117">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="87b53-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="87b53-118">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="87b53-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="87b53-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b53-119">-ResourceGroupName</span></span>
<span data-ttu-id="87b53-120">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="87b53-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b53-121">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="87b53-121">-VMName</span></span>
<span data-ttu-id="87b53-122">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="87b53-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="87b53-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87b53-123">-Confirm</span></span>
<span data-ttu-id="87b53-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="87b53-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87b53-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87b53-125">-WhatIf</span></span>
<span data-ttu-id="87b53-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87b53-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87b53-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="87b53-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87b53-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b53-128">CommonParameters</span></span>
<span data-ttu-id="87b53-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b53-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b53-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87b53-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b53-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87b53-131">INPUTS</span></span>

### <span data-ttu-id="87b53-132">System.String</span><span class="sxs-lookup"><span data-stu-id="87b53-132">System.String</span></span>

## <span data-ttu-id="87b53-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87b53-133">OUTPUTS</span></span>

### <span data-ttu-id="87b53-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="87b53-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="87b53-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87b53-135">NOTES</span></span>

## <span data-ttu-id="87b53-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87b53-136">RELATED LINKS</span></span>

[<span data-ttu-id="87b53-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="87b53-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="87b53-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="87b53-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


