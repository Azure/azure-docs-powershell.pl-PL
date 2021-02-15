---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: f739c5fa018a4d4f4ebf553c76dbacd35ee315c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189043"
---
# <span data-ttu-id="451aa-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="451aa-101">Get-AzSignalR</span></span>

## <span data-ttu-id="451aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="451aa-102">SYNOPSIS</span></span>
<span data-ttu-id="451aa-103">Uzyskaj konkretną usługę SignalR lub wszystkie usługi SignalR w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="451aa-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="451aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="451aa-104">SYNTAX</span></span>

### <span data-ttu-id="451aa-105">ListSignalRServiceParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="451aa-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="451aa-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="451aa-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="451aa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="451aa-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="451aa-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="451aa-108">DESCRIPTION</span></span>
<span data-ttu-id="451aa-109">Uzyskaj konkretną usługę SignalR lub wszystkie usługi SignalR w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="451aa-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="451aa-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="451aa-110">EXAMPLES</span></span>

### <span data-ttu-id="451aa-111">Uzyskaj wszystkie usługi SignalR w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="451aa-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="451aa-112">Uzyskiwanie wszystkich usług SignalR w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="451aa-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="451aa-113">Uzyskiwanie określonej usługi SignalR</span><span class="sxs-lookup"><span data-stu-id="451aa-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="451aa-114">Uzyskiwanie określonej usługi SignalR z domyślnej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="451aa-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="451aa-115">Domyślną grupę zasobów można ustawić za pomocą ustawienia \` Set-AzDefault -ResourceGroupName myResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="451aa-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="451aa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="451aa-116">PARAMETERS</span></span>

### <span data-ttu-id="451aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="451aa-117">-DefaultProfile</span></span>
<span data-ttu-id="451aa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="451aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="451aa-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="451aa-119">-Name</span></span>
<span data-ttu-id="451aa-120">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="451aa-120">SignalR service name.</span></span>

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

### <span data-ttu-id="451aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="451aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="451aa-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="451aa-122">Resource group name.</span></span>

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

### <span data-ttu-id="451aa-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="451aa-123">-ResourceId</span></span>
<span data-ttu-id="451aa-124">Identyfikator zasobu usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="451aa-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="451aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451aa-125">CommonParameters</span></span>
<span data-ttu-id="451aa-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="451aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451aa-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="451aa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451aa-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="451aa-128">INPUTS</span></span>

### <span data-ttu-id="451aa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="451aa-129">System.String</span></span>
## <span data-ttu-id="451aa-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="451aa-130">OUTPUTS</span></span>

### <span data-ttu-id="451aa-131">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="451aa-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="451aa-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="451aa-132">NOTES</span></span>

## <span data-ttu-id="451aa-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="451aa-133">RELATED LINKS</span></span>
