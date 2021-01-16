---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341305"
---
# <span data-ttu-id="8ce38-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ce38-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="8ce38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ce38-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce38-103">Tworzy konfigurację puli adresów zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8ce38-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="8ce38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ce38-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ce38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8ce38-105">DESCRIPTION</span></span>
<span data-ttu-id="8ce38-106">Polecenie cmdlet **New-AzLoadBalancerBackendAddressPoolConfig** umożliwia utworzenie konfiguracji puli adresów zaplecza modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce38-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8ce38-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ce38-107">EXAMPLES</span></span>

### <span data-ttu-id="8ce38-108">Przykład 1. Tworzenie konfiguracji puli adresów zaplecza modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="8ce38-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="8ce38-109">To polecenie tworzy konfigurację puli adresów zaplecza o nazwie BackendAddressPool02 dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8ce38-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="8ce38-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ce38-110">PARAMETERS</span></span>

### <span data-ttu-id="8ce38-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce38-111">-DefaultProfile</span></span>
<span data-ttu-id="8ce38-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce38-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ce38-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ce38-113">-Name</span></span>
<span data-ttu-id="8ce38-114">Określa nazwę konfiguracji puli adresów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="8ce38-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="8ce38-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ce38-115">-Confirm</span></span>
<span data-ttu-id="8ce38-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ce38-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ce38-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce38-117">-WhatIf</span></span>
<span data-ttu-id="8ce38-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ce38-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ce38-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ce38-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ce38-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce38-120">CommonParameters</span></span>
<span data-ttu-id="8ce38-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ce38-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce38-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce38-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce38-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ce38-123">INPUTS</span></span>

### <span data-ttu-id="8ce38-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8ce38-124">None</span></span>

## <span data-ttu-id="8ce38-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ce38-125">OUTPUTS</span></span>

### <span data-ttu-id="8ce38-126">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8ce38-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="8ce38-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ce38-127">NOTES</span></span>

## <span data-ttu-id="8ce38-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ce38-128">RELATED LINKS</span></span>

[<span data-ttu-id="8ce38-129">Dodaj-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ce38-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8ce38-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ce38-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8ce38-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8ce38-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


