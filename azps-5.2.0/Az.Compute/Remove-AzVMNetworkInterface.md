---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355417"
---
# <span data-ttu-id="edd81-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="edd81-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="edd81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="edd81-102">SYNOPSIS</span></span>
<span data-ttu-id="edd81-103">Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="edd81-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="edd81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="edd81-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edd81-105">Opis</span><span class="sxs-lookup"><span data-stu-id="edd81-105">DESCRIPTION</span></span>
<span data-ttu-id="edd81-106">Polecenie cmdlet **Remove-AzVMNetworkInterface** Usuwa interfejs sieciowy z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="edd81-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="edd81-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="edd81-107">EXAMPLES</span></span>

## <span data-ttu-id="edd81-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edd81-108">PARAMETERS</span></span>

### <span data-ttu-id="edd81-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd81-109">-DefaultProfile</span></span>
<span data-ttu-id="edd81-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="edd81-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edd81-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="edd81-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="edd81-112">Określa tablicę identyfikatorów interfejsów sieciowych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edd81-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="edd81-113">-VM</span><span class="sxs-lookup"><span data-stu-id="edd81-113">-VM</span></span>
<span data-ttu-id="edd81-114">Umożliwia określenie maszyny wirtualnej, z poziomu której to polecenie cmdlet Usuwa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="edd81-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="edd81-115">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="edd81-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="edd81-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edd81-116">-Confirm</span></span>
<span data-ttu-id="edd81-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edd81-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edd81-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edd81-118">-WhatIf</span></span>
<span data-ttu-id="edd81-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edd81-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edd81-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="edd81-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edd81-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd81-121">CommonParameters</span></span>
<span data-ttu-id="edd81-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd81-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd81-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edd81-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd81-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edd81-124">INPUTS</span></span>

### <span data-ttu-id="edd81-125">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="edd81-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="edd81-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="edd81-126">OUTPUTS</span></span>

### <span data-ttu-id="edd81-127">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="edd81-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="edd81-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="edd81-128">NOTES</span></span>

## <span data-ttu-id="edd81-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edd81-129">RELATED LINKS</span></span>

[<span data-ttu-id="edd81-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="edd81-130">Get-AzVM</span></span>](./Get-AzVM.md)


