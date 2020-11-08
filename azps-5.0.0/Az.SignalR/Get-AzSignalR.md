---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: f739c5fa018a4d4f4ebf553c76dbacd35ee315c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232461"
---
# <span data-ttu-id="72839-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="72839-101">Get-AzSignalR</span></span>

## <span data-ttu-id="72839-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72839-102">SYNOPSIS</span></span>
<span data-ttu-id="72839-103">Uzyskaj określoną usługę sygnalizującą lub wszystkie usługi sygnalizujące w grupie zasobów lub abonament.</span><span class="sxs-lookup"><span data-stu-id="72839-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="72839-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72839-104">SYNTAX</span></span>

### <span data-ttu-id="72839-105">ListSignalRServiceParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72839-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72839-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="72839-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72839-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72839-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72839-108">Opis</span><span class="sxs-lookup"><span data-stu-id="72839-108">DESCRIPTION</span></span>
<span data-ttu-id="72839-109">Uzyskaj określoną usługę sygnalizującą lub wszystkie usługi sygnalizujące w grupie zasobów lub abonament.</span><span class="sxs-lookup"><span data-stu-id="72839-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="72839-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72839-110">EXAMPLES</span></span>

### <span data-ttu-id="72839-111">Uzyskiwanie wszystkich usług sygnalizacji w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="72839-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="72839-112">Uzyskiwanie wszystkich usług sygnalizacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="72839-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="72839-113">Uzyskaj określoną usługę sygnalizującą</span><span class="sxs-lookup"><span data-stu-id="72839-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="72839-114">Uzyskiwanie określonej usługi sygnalizującego z domyślnej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="72839-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="72839-115">Domyślną grupę zasobów można ustawić przez \` Set-AzDefault-ResourceGroupName moja zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="72839-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="72839-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72839-116">PARAMETERS</span></span>

### <span data-ttu-id="72839-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72839-117">-DefaultProfile</span></span>
<span data-ttu-id="72839-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72839-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72839-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72839-119">-Name</span></span>
<span data-ttu-id="72839-120">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="72839-120">SignalR service name.</span></span>

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

### <span data-ttu-id="72839-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72839-121">-ResourceGroupName</span></span>
<span data-ttu-id="72839-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72839-122">Resource group name.</span></span>

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

### <span data-ttu-id="72839-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72839-123">-ResourceId</span></span>
<span data-ttu-id="72839-124">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="72839-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="72839-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72839-125">CommonParameters</span></span>
<span data-ttu-id="72839-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72839-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72839-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72839-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72839-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72839-128">INPUTS</span></span>

### <span data-ttu-id="72839-129">System. String</span><span class="sxs-lookup"><span data-stu-id="72839-129">System.String</span></span>
## <span data-ttu-id="72839-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72839-130">OUTPUTS</span></span>

### <span data-ttu-id="72839-131">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="72839-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="72839-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72839-132">NOTES</span></span>

## <span data-ttu-id="72839-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72839-133">RELATED LINKS</span></span>
