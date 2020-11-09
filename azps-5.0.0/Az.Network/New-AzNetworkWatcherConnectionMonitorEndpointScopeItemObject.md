---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309211"
---
# <span data-ttu-id="c3cab-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="c3cab-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="c3cab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3cab-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cab-103">Tworzy element zakresu punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="c3cab-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="c3cab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3cab-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3cab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3cab-105">DESCRIPTION</span></span>
<span data-ttu-id="c3cab-106">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject umożliwia utworzenie elementu zakresu punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="c3cab-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="c3cab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3cab-107">EXAMPLES</span></span>

### <span data-ttu-id="c3cab-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3cab-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="c3cab-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3cab-109">PARAMETERS</span></span>

### <span data-ttu-id="c3cab-110">-Address (adres)</span><span class="sxs-lookup"><span data-stu-id="c3cab-110">-Address</span></span>
<span data-ttu-id="c3cab-111">Adres elementu zakresu.</span><span class="sxs-lookup"><span data-stu-id="c3cab-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="c3cab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3cab-112">-DefaultProfile</span></span>
<span data-ttu-id="c3cab-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cab-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3cab-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3cab-114">-Confirm</span></span>
<span data-ttu-id="c3cab-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3cab-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3cab-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3cab-116">-WhatIf</span></span>
<span data-ttu-id="c3cab-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3cab-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3cab-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c3cab-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3cab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cab-119">CommonParameters</span></span>
<span data-ttu-id="c3cab-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cab-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3cab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cab-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3cab-122">INPUTS</span></span>

### <span data-ttu-id="c3cab-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c3cab-123">None</span></span>

## <span data-ttu-id="c3cab-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3cab-124">OUTPUTS</span></span>

### <span data-ttu-id="c3cab-125">Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="c3cab-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="c3cab-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3cab-126">NOTES</span></span>

## <span data-ttu-id="c3cab-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3cab-127">RELATED LINKS</span></span>
