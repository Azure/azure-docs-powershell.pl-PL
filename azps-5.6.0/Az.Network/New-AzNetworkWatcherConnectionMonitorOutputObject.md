---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 895659481999ab5801538bec3b88765e1d48aeca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958497"
---
# <span data-ttu-id="2ff58-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="2ff58-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="2ff58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ff58-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff58-103">Tworzenie obiektu docelowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="2ff58-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="2ff58-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ff58-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ff58-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ff58-105">DESCRIPTION</span></span>
<span data-ttu-id="2ff58-106">Polecenie New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet tworzy docelowy obiekt docelowy monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="2ff58-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="2ff58-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ff58-107">EXAMPLES</span></span>

### <span data-ttu-id="2ff58-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ff58-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="2ff58-109">Typ: "workspace" WorkspaceSettings: { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="2ff58-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="2ff58-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ff58-110">PARAMETERS</span></span>

### <span data-ttu-id="2ff58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff58-111">-DefaultProfile</span></span>
<span data-ttu-id="2ff58-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ff58-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ff58-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="2ff58-113">-OutputType</span></span>
<span data-ttu-id="2ff58-114">Typ docelowy docelowy monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="2ff58-114">Connection monitor output destination type.</span></span> <span data-ttu-id="2ff58-115">Obecnie obsługiwany jest \" tylko \" obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="2ff58-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="2ff58-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="2ff58-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="2ff58-117">Identyfikator zasobu obszaru roboczego analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="2ff58-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="2ff58-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ff58-118">-Confirm</span></span>
<span data-ttu-id="2ff58-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ff58-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff58-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ff58-120">-WhatIf</span></span>
<span data-ttu-id="2ff58-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff58-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ff58-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2ff58-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ff58-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff58-123">CommonParameters</span></span>
<span data-ttu-id="2ff58-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff58-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff58-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ff58-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff58-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ff58-126">INPUTS</span></span>

### <span data-ttu-id="2ff58-127">Brak</span><span class="sxs-lookup"><span data-stu-id="2ff58-127">None</span></span>

## <span data-ttu-id="2ff58-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ff58-128">OUTPUTS</span></span>

### <span data-ttu-id="2ff58-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="2ff58-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="2ff58-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ff58-130">NOTES</span></span>

## <span data-ttu-id="2ff58-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ff58-131">RELATED LINKS</span></span>
