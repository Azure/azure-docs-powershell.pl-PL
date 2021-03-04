---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: e7287cff34420c7885f5cddef95e4ca3b09e881f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955505"
---
# <span data-ttu-id="a73af-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="a73af-101">Get-AzSignalR</span></span>

## <span data-ttu-id="a73af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a73af-102">SYNOPSIS</span></span>
<span data-ttu-id="a73af-103">Uzyskaj konkretną usługę SignalR lub wszystkie usługi SignalR w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a73af-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="a73af-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a73af-104">SYNTAX</span></span>

### <span data-ttu-id="a73af-105">ListSignalRServiceParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a73af-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a73af-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a73af-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a73af-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a73af-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a73af-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a73af-108">DESCRIPTION</span></span>
<span data-ttu-id="a73af-109">Uzyskaj konkretną usługę SignalR lub wszystkie usługi SignalR w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a73af-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="a73af-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a73af-110">EXAMPLES</span></span>

### <span data-ttu-id="a73af-111">Uzyskaj wszystkie usługi SignalR w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a73af-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="a73af-112">Uzyskiwanie wszystkich usług SignalR w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a73af-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="a73af-113">Uzyskaj konkretną usługę SignalR</span><span class="sxs-lookup"><span data-stu-id="a73af-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="a73af-114">Uzyskiwanie określonej usługi SignalR z domyślnej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a73af-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="a73af-115">Domyślną grupę zasobów można ustawić za pomocą ustawienia \` Set-AzDefault -ResourceGroupName myResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="a73af-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="a73af-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a73af-116">PARAMETERS</span></span>

### <span data-ttu-id="a73af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73af-117">-DefaultProfile</span></span>
<span data-ttu-id="a73af-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a73af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a73af-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a73af-119">-Name</span></span>
<span data-ttu-id="a73af-120">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="a73af-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73af-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a73af-121">-ResourceGroupName</span></span>
<span data-ttu-id="a73af-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a73af-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73af-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a73af-123">-ResourceId</span></span>
<span data-ttu-id="a73af-124">Identyfikator zasobu usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="a73af-124">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a73af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73af-125">CommonParameters</span></span>
<span data-ttu-id="a73af-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a73af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73af-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a73af-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73af-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a73af-128">INPUTS</span></span>

### <span data-ttu-id="a73af-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a73af-129">System.String</span></span>
## <span data-ttu-id="a73af-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a73af-130">OUTPUTS</span></span>

### <span data-ttu-id="a73af-131">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="a73af-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="a73af-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a73af-132">NOTES</span></span>

## <span data-ttu-id="a73af-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a73af-133">RELATED LINKS</span></span>
