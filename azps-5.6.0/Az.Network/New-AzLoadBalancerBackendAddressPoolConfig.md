---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 805afd046505f6b1f6695205e858c6215c57ec7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955793"
---
# <span data-ttu-id="211e0-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="211e0-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="211e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="211e0-102">SYNOPSIS</span></span>
<span data-ttu-id="211e0-103">Tworzy konfigurację puli adresów zaplecza dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="211e0-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="211e0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="211e0-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="211e0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="211e0-105">DESCRIPTION</span></span>
<span data-ttu-id="211e0-106">Polecenie **cmdlet New-AzLoadBalancerBackendAddressPoolConfig** tworzy konfigurację puli adresów zaplecza dla narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="211e0-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="211e0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="211e0-107">EXAMPLES</span></span>

### <span data-ttu-id="211e0-108">Przykład 1. Tworzenie konfiguracji puli adresów zaplecza dla równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="211e0-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="211e0-109">To polecenie tworzy konfigurację puli adresów zaplecza o nazwie BackendAddressPool02 dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="211e0-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="211e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="211e0-110">PARAMETERS</span></span>

### <span data-ttu-id="211e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211e0-111">-DefaultProfile</span></span>
<span data-ttu-id="211e0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="211e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="211e0-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="211e0-113">-Name</span></span>
<span data-ttu-id="211e0-114">Określa nazwę konfiguracji puli adresów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="211e0-114">Specifies the name of the address pool configuration to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="211e0-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="211e0-115">-Confirm</span></span>
<span data-ttu-id="211e0-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="211e0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="211e0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="211e0-117">-WhatIf</span></span>
<span data-ttu-id="211e0-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="211e0-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="211e0-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="211e0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="211e0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211e0-120">CommonParameters</span></span>
<span data-ttu-id="211e0-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="211e0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211e0-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="211e0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211e0-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="211e0-123">INPUTS</span></span>

### <span data-ttu-id="211e0-124">Brak</span><span class="sxs-lookup"><span data-stu-id="211e0-124">None</span></span>

## <span data-ttu-id="211e0-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="211e0-125">OUTPUTS</span></span>

### <span data-ttu-id="211e0-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="211e0-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="211e0-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="211e0-127">NOTES</span></span>

## <span data-ttu-id="211e0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="211e0-128">RELATED LINKS</span></span>

[<span data-ttu-id="211e0-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="211e0-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="211e0-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="211e0-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="211e0-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="211e0-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


