---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181555"
---
# <span data-ttu-id="d938c-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d938c-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="d938c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d938c-102">SYNOPSIS</span></span>
<span data-ttu-id="d938c-103">Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d938c-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="d938c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d938c-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d938c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d938c-105">DESCRIPTION</span></span>
<span data-ttu-id="d938c-106">Polecenie **cmdlet Remove-AzVMNetworkInterface** usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d938c-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="d938c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d938c-107">EXAMPLES</span></span>

## <span data-ttu-id="d938c-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d938c-108">PARAMETERS</span></span>

### <span data-ttu-id="d938c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d938c-109">-DefaultProfile</span></span>
<span data-ttu-id="d938c-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d938c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d938c-111">- NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="d938c-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="d938c-112">Określa tablicę identyfikatorów interfejsu sieciowego usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d938c-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d938c-113">- MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="d938c-113">-VM</span></span>
<span data-ttu-id="d938c-114">Określa maszynę wirtualną, z której to polecenie cmdlet usuwa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="d938c-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="d938c-115">Aby uzyskać obiekt maszyny wirtualnej, użyj Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d938c-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d938c-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d938c-116">-Confirm</span></span>
<span data-ttu-id="d938c-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d938c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d938c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d938c-118">-WhatIf</span></span>
<span data-ttu-id="d938c-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d938c-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d938c-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d938c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d938c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d938c-121">CommonParameters</span></span>
<span data-ttu-id="d938c-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d938c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d938c-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d938c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d938c-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d938c-124">INPUTS</span></span>

### <span data-ttu-id="d938c-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d938c-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d938c-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d938c-126">OUTPUTS</span></span>

### <span data-ttu-id="d938c-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d938c-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d938c-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d938c-128">NOTES</span></span>

## <span data-ttu-id="d938c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d938c-129">RELATED LINKS</span></span>

[<span data-ttu-id="d938c-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d938c-130">Get-AzVM</span></span>](./Get-AzVM.md)


