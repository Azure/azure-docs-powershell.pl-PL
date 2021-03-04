---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: 298586f11bba29ce44e78bc3c19d4d9fc6be21f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958522"
---
# <span data-ttu-id="464a9-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="464a9-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="464a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="464a9-102">SYNOPSIS</span></span>
<span data-ttu-id="464a9-103">Tworzy element zakresu punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="464a9-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="464a9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="464a9-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="464a9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="464a9-105">DESCRIPTION</span></span>
<span data-ttu-id="464a9-106">Polecenie New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet tworzy element zakresu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="464a9-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="464a9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="464a9-107">EXAMPLES</span></span>

### <span data-ttu-id="464a9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="464a9-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="464a9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="464a9-109">PARAMETERS</span></span>

### <span data-ttu-id="464a9-110">— Adres</span><span class="sxs-lookup"><span data-stu-id="464a9-110">-Address</span></span>
<span data-ttu-id="464a9-111">Adres elementu zakresu.</span><span class="sxs-lookup"><span data-stu-id="464a9-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="464a9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="464a9-112">-DefaultProfile</span></span>
<span data-ttu-id="464a9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="464a9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="464a9-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="464a9-114">-Confirm</span></span>
<span data-ttu-id="464a9-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="464a9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="464a9-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="464a9-116">-WhatIf</span></span>
<span data-ttu-id="464a9-117">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="464a9-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="464a9-118">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="464a9-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="464a9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464a9-119">CommonParameters</span></span>
<span data-ttu-id="464a9-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="464a9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464a9-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="464a9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464a9-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="464a9-122">INPUTS</span></span>

### <span data-ttu-id="464a9-123">Brak</span><span class="sxs-lookup"><span data-stu-id="464a9-123">None</span></span>

## <span data-ttu-id="464a9-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="464a9-124">OUTPUTS</span></span>

### <span data-ttu-id="464a9-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="464a9-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="464a9-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="464a9-126">NOTES</span></span>

## <span data-ttu-id="464a9-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="464a9-127">RELATED LINKS</span></span>
