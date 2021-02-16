---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184435"
---
# <span data-ttu-id="84c74-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="84c74-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="84c74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84c74-102">SYNOPSIS</span></span>
<span data-ttu-id="84c74-103">Tworzy element zakresu punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="84c74-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="84c74-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="84c74-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84c74-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="84c74-105">DESCRIPTION</span></span>
<span data-ttu-id="84c74-106">Polecenie New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet tworzy element zakresu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="84c74-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="84c74-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="84c74-107">EXAMPLES</span></span>

### <span data-ttu-id="84c74-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84c74-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="84c74-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84c74-109">PARAMETERS</span></span>

### <span data-ttu-id="84c74-110">— Adres</span><span class="sxs-lookup"><span data-stu-id="84c74-110">-Address</span></span>
<span data-ttu-id="84c74-111">Adres elementu zakresu.</span><span class="sxs-lookup"><span data-stu-id="84c74-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="84c74-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c74-112">-DefaultProfile</span></span>
<span data-ttu-id="84c74-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="84c74-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84c74-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84c74-114">-Confirm</span></span>
<span data-ttu-id="84c74-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="84c74-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c74-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c74-116">-WhatIf</span></span>
<span data-ttu-id="84c74-117">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84c74-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c74-118">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="84c74-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c74-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c74-119">CommonParameters</span></span>
<span data-ttu-id="84c74-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84c74-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c74-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84c74-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c74-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84c74-122">INPUTS</span></span>

### <span data-ttu-id="84c74-123">Brak</span><span class="sxs-lookup"><span data-stu-id="84c74-123">None</span></span>

## <span data-ttu-id="84c74-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84c74-124">OUTPUTS</span></span>

### <span data-ttu-id="84c74-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="84c74-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="84c74-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="84c74-126">NOTES</span></span>

## <span data-ttu-id="84c74-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84c74-127">RELATED LINKS</span></span>
