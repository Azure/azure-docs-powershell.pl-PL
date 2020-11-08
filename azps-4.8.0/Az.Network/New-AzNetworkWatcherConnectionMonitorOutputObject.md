---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221967"
---
# <span data-ttu-id="4d6bb-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="4d6bb-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="4d6bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4d6bb-103">Tworzenie obiektu docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="4d6bb-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="4d6bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d6bb-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d6bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d6bb-105">DESCRIPTION</span></span>
<span data-ttu-id="4d6bb-106">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorOutputObject powoduje utworzenie obiektu docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="4d6bb-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="4d6bb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d6bb-107">EXAMPLES</span></span>

### <span data-ttu-id="4d6bb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d6bb-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="4d6bb-109">Wpisz: "obszar roboczy" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="4d6bb-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="4d6bb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d6bb-110">PARAMETERS</span></span>

### <span data-ttu-id="4d6bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d6bb-111">-DefaultProfile</span></span>
<span data-ttu-id="4d6bb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d6bb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d6bb-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="4d6bb-113">-OutputType</span></span>
<span data-ttu-id="4d6bb-114">Typ docelowy wyjścia monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="4d6bb-114">Connection monitor output destination type.</span></span> <span data-ttu-id="4d6bb-115">Obecnie \" jest obsługiwany tylko obszar roboczy \" .</span><span class="sxs-lookup"><span data-stu-id="4d6bb-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="4d6bb-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="4d6bb-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="4d6bb-117">Identyfikator zasobu obszaru roboczego analizy dzienników.</span><span class="sxs-lookup"><span data-stu-id="4d6bb-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="4d6bb-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d6bb-118">-Confirm</span></span>
<span data-ttu-id="4d6bb-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d6bb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d6bb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d6bb-120">-WhatIf</span></span>
<span data-ttu-id="4d6bb-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d6bb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d6bb-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d6bb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d6bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d6bb-123">CommonParameters</span></span>
<span data-ttu-id="4d6bb-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d6bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d6bb-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d6bb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d6bb-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d6bb-126">INPUTS</span></span>

### <span data-ttu-id="4d6bb-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4d6bb-127">None</span></span>

## <span data-ttu-id="4d6bb-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d6bb-128">OUTPUTS</span></span>

### <span data-ttu-id="4d6bb-129">Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="4d6bb-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="4d6bb-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d6bb-130">NOTES</span></span>

## <span data-ttu-id="4d6bb-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d6bb-131">RELATED LINKS</span></span>
