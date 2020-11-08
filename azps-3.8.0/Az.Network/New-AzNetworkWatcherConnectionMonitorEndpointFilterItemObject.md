---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointfilteritemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
ms.openlocfilehash: c06052ee28d849c5d07a941366efd15cbfeefe25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049996"
---
# <span data-ttu-id="f7cf5-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span><span class="sxs-lookup"><span data-stu-id="f7cf5-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span></span>

## <span data-ttu-id="f7cf5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="f7cf5-103">Umożliwia utworzenie elementu filtru punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="f7cf5-103">Creates a connection monitor endpoint filter item.</span></span>

## <span data-ttu-id="f7cf5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7cf5-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7cf5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="f7cf5-106">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject powoduje utworzenie elementu filtr punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="f7cf5-106">The New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet creates endpoint filter item.</span></span>

## <span data-ttu-id="f7cf5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7cf5-107">EXAMPLES</span></span>

### <span data-ttu-id="f7cf5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7cf5-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "10.0.0.1"
```

<span data-ttu-id="f7cf5-109">Typ: adres AgentAddress: 10.0.0.1</span><span class="sxs-lookup"><span data-stu-id="f7cf5-109">Type    : AgentAddress Address : 10.0.0.1</span></span>

## <span data-ttu-id="f7cf5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7cf5-110">PARAMETERS</span></span>

### <span data-ttu-id="f7cf5-111">-Address (adres)</span><span class="sxs-lookup"><span data-stu-id="f7cf5-111">-Address</span></span>
<span data-ttu-id="f7cf5-112">Adres elementu filtru.</span><span class="sxs-lookup"><span data-stu-id="f7cf5-112">The address of the filter item.</span></span>

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

### <span data-ttu-id="f7cf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7cf5-113">-DefaultProfile</span></span>
<span data-ttu-id="f7cf5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7cf5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7cf5-115">-Type</span><span class="sxs-lookup"><span data-stu-id="f7cf5-115">-Type</span></span>
<span data-ttu-id="f7cf5-116">Typ elementu znajdującego się w filtrze.</span><span class="sxs-lookup"><span data-stu-id="f7cf5-116">The type of item included in the filter.</span></span> <span data-ttu-id="f7cf5-117">Obecnie jest obsługiwana tylko "AgentAddress".</span><span class="sxs-lookup"><span data-stu-id="f7cf5-117">Currently only 'AgentAddress' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7cf5-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7cf5-118">-Confirm</span></span>
<span data-ttu-id="f7cf5-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7cf5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7cf5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7cf5-120">-WhatIf</span></span>
<span data-ttu-id="f7cf5-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7cf5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7cf5-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7cf5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7cf5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7cf5-123">CommonParameters</span></span>
<span data-ttu-id="f7cf5-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7cf5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7cf5-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7cf5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7cf5-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7cf5-126">INPUTS</span></span>

### <span data-ttu-id="f7cf5-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f7cf5-127">None</span></span>

## <span data-ttu-id="f7cf5-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7cf5-128">OUTPUTS</span></span>

### <span data-ttu-id="f7cf5-129">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorEndpointFilterItem</span><span class="sxs-lookup"><span data-stu-id="f7cf5-129">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorEndpointFilterItem</span></span>

## <span data-ttu-id="f7cf5-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7cf5-130">NOTES</span></span>

## <span data-ttu-id="f7cf5-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7cf5-131">RELATED LINKS</span></span>
