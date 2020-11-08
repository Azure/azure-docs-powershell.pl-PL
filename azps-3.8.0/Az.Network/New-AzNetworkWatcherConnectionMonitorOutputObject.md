---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049986"
---
# <span data-ttu-id="f6ae3-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="f6ae3-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="f6ae3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ae3-103">Tworzenie obiektu docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="f6ae3-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="f6ae3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6ae3-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6ae3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6ae3-105">DESCRIPTION</span></span>
<span data-ttu-id="f6ae3-106">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorOutputObject powoduje utworzenie obiektu docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="f6ae3-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="f6ae3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6ae3-107">EXAMPLES</span></span>

### <span data-ttu-id="f6ae3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6ae3-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="f6ae3-109">Wpisz: "obszar roboczy" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="f6ae3-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="f6ae3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6ae3-110">PARAMETERS</span></span>

### <span data-ttu-id="f6ae3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ae3-111">-DefaultProfile</span></span>
<span data-ttu-id="f6ae3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6ae3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6ae3-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="f6ae3-113">-OutputType</span></span>
<span data-ttu-id="f6ae3-114">Typ docelowy wyjścia monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="f6ae3-114">Connection monitor output destination type.</span></span> <span data-ttu-id="f6ae3-115">Obecnie \" jest obsługiwany tylko obszar roboczy \" .</span><span class="sxs-lookup"><span data-stu-id="f6ae3-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="f6ae3-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="f6ae3-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="f6ae3-117">Identyfikator zasobu obszaru roboczego analizy dzienników.</span><span class="sxs-lookup"><span data-stu-id="f6ae3-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="f6ae3-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6ae3-118">-Confirm</span></span>
<span data-ttu-id="f6ae3-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6ae3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6ae3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6ae3-120">-WhatIf</span></span>
<span data-ttu-id="f6ae3-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6ae3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6ae3-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f6ae3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6ae3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ae3-123">CommonParameters</span></span>
<span data-ttu-id="f6ae3-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6ae3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ae3-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6ae3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ae3-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6ae3-126">INPUTS</span></span>

### <span data-ttu-id="f6ae3-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f6ae3-127">None</span></span>

## <span data-ttu-id="f6ae3-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6ae3-128">OUTPUTS</span></span>

### <span data-ttu-id="f6ae3-129">Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="f6ae3-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="f6ae3-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6ae3-130">NOTES</span></span>

## <span data-ttu-id="f6ae3-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6ae3-131">RELATED LINKS</span></span>
