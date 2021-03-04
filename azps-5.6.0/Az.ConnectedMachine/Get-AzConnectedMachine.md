---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: c97567c2832d82ec739b62bfe8bb6c08e173f9e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012410"
---
# <span data-ttu-id="bf5ab-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="bf5ab-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="bf5ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf5ab-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5ab-103">Pobiera informacje o widoku modelu lub widoku wystąpienia komputera hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="bf5ab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bf5ab-104">SYNTAX</span></span>

### <span data-ttu-id="bf5ab-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="bf5ab-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bf5ab-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="bf5ab-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bf5ab-107">Lista</span><span class="sxs-lookup"><span data-stu-id="bf5ab-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf5ab-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bf5ab-108">DESCRIPTION</span></span>
<span data-ttu-id="bf5ab-109">Pobiera informacje o widoku modelu lub widoku wystąpienia komputera hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="bf5ab-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bf5ab-110">EXAMPLES</span></span>

### <span data-ttu-id="bf5ab-111">Przykład 1. Lista wszystkich połączonych komputerów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bf5ab-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="bf5ab-112">Wyświetla listę wszystkich połączonych komputerów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="bf5ab-113">Jeśli subskrypcja nie zostanie określona, będzie ona używać subskrypcji z bieżącego kontekstu programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="bf5ab-114">Przykład 2. Lista wszystkich połączonych komputerów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="bf5ab-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="bf5ab-115">Lista wszystkich połączonych komputerów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="bf5ab-116">Przykład 3. Uzyskiwanie połączonego komputera w grupie zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="bf5ab-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="bf5ab-117">Uzyskiwanie połączonego komputera w grupie zasobów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="bf5ab-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf5ab-118">PARAMETERS</span></span>

### <span data-ttu-id="bf5ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5ab-119">-DefaultProfile</span></span>
<span data-ttu-id="bf5ab-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf5ab-121">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="bf5ab-121">-Expand</span></span>
<span data-ttu-id="bf5ab-122">Wyrażenie rozwijania, które ma być stosowane do operacji.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf5ab-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bf5ab-123">-Name</span></span>
<span data-ttu-id="bf5ab-124">Nazwa komputera hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-124">The name of the hybrid machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf5ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf5ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf5ab-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf5ab-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf5ab-127">-SubscriptionId</span></span>
<span data-ttu-id="bf5ab-128">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bf5ab-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf5ab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5ab-130">CommonParameters</span></span>
<span data-ttu-id="bf5ab-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf5ab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5ab-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf5ab-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5ab-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf5ab-133">INPUTS</span></span>

## <span data-ttu-id="bf5ab-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf5ab-134">OUTPUTS</span></span>

### <span data-ttu-id="bf5ab-135">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.Api20200802.IMachine</span><span class="sxs-lookup"><span data-stu-id="bf5ab-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="bf5ab-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bf5ab-136">NOTES</span></span>

<span data-ttu-id="bf5ab-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="bf5ab-137">ALIASES</span></span>

## <span data-ttu-id="bf5ab-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf5ab-138">RELATED LINKS</span></span>

