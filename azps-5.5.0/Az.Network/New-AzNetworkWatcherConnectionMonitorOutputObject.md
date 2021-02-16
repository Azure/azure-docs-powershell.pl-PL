---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: ec1bba32027d3ec96aef61f3abec7d51cec5c35b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184434"
---
# <span data-ttu-id="5a352-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="5a352-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="5a352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a352-102">SYNOPSIS</span></span>
<span data-ttu-id="5a352-103">Tworzenie obiektu docelowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="5a352-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="5a352-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a352-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a352-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a352-105">DESCRIPTION</span></span>
<span data-ttu-id="5a352-106">Polecenie New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet tworzy docelowy obiekt docelowy monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="5a352-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="5a352-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a352-107">EXAMPLES</span></span>

### <span data-ttu-id="5a352-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a352-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="5a352-109">Typ: "workspace" WorkspaceSettings: { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="5a352-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="5a352-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a352-110">PARAMETERS</span></span>

### <span data-ttu-id="5a352-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a352-111">-DefaultProfile</span></span>
<span data-ttu-id="5a352-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a352-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a352-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="5a352-113">-OutputType</span></span>
<span data-ttu-id="5a352-114">Typ docelowy docelowy monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="5a352-114">Connection monitor output destination type.</span></span> <span data-ttu-id="5a352-115">Obecnie obsługiwany jest \" tylko \" obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="5a352-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="5a352-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="5a352-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="5a352-117">Identyfikator zasobu obszaru roboczego analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="5a352-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="5a352-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a352-118">-Confirm</span></span>
<span data-ttu-id="5a352-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5a352-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a352-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a352-120">-WhatIf</span></span>
<span data-ttu-id="5a352-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a352-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a352-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5a352-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a352-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a352-123">CommonParameters</span></span>
<span data-ttu-id="5a352-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a352-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a352-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a352-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a352-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a352-126">INPUTS</span></span>

### <span data-ttu-id="5a352-127">Brak</span><span class="sxs-lookup"><span data-stu-id="5a352-127">None</span></span>

## <span data-ttu-id="5a352-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a352-128">OUTPUTS</span></span>

### <span data-ttu-id="5a352-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="5a352-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="5a352-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a352-130">NOTES</span></span>

## <span data-ttu-id="5a352-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a352-131">RELATED LINKS</span></span>
