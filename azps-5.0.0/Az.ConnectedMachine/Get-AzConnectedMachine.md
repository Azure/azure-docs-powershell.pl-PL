---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233211"
---
# <span data-ttu-id="72518-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="72518-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="72518-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72518-102">SYNOPSIS</span></span>
<span data-ttu-id="72518-103">Pobiera informacje o widoku modelu lub widoku wystąpienia maszyny hybrydowej.</span><span class="sxs-lookup"><span data-stu-id="72518-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="72518-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72518-104">SYNTAX</span></span>

### <span data-ttu-id="72518-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72518-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72518-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="72518-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72518-107">Lista</span><span class="sxs-lookup"><span data-stu-id="72518-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="72518-108">Opis</span><span class="sxs-lookup"><span data-stu-id="72518-108">DESCRIPTION</span></span>
<span data-ttu-id="72518-109">Pobiera informacje o widoku modelu lub widoku wystąpienia maszyny hybrydowej.</span><span class="sxs-lookup"><span data-stu-id="72518-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="72518-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72518-110">EXAMPLES</span></span>

### <span data-ttu-id="72518-111">Przykład 1: wyświetlanie wszystkich połączonych maszyn w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="72518-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="72518-112">Wyświetla listę wszystkich połączonych komputerów w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="72518-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="72518-113">Jeśli nie podano subskrypcji, zostanie ona wykorzystana z subskrypcji bieżącego kontekstu programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72518-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="72518-114">Przykład 2: Wyświetlanie listy wszystkich połączonych maszyn w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="72518-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="72518-115">Wyświetlanie listy wszystkich połączonych maszyn w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="72518-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="72518-116">Przykład 3: uzyskiwanie połączonego komputera w grupie zasób według nazwy</span><span class="sxs-lookup"><span data-stu-id="72518-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="72518-117">Uzyskaj połączony komputer w grupie zasób według nazwy.</span><span class="sxs-lookup"><span data-stu-id="72518-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="72518-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72518-118">PARAMETERS</span></span>

### <span data-ttu-id="72518-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72518-119">-DefaultProfile</span></span>
<span data-ttu-id="72518-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72518-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72518-121">-Expand</span><span class="sxs-lookup"><span data-stu-id="72518-121">-Expand</span></span>
<span data-ttu-id="72518-122">Wyrażenie rozwijania, które ma zostać zastosowane w operacji.</span><span class="sxs-lookup"><span data-stu-id="72518-122">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="72518-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72518-123">-Name</span></span>
<span data-ttu-id="72518-124">Nazwa maszyny hybrydowej.</span><span class="sxs-lookup"><span data-stu-id="72518-124">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="72518-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72518-125">-ResourceGroupName</span></span>
<span data-ttu-id="72518-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72518-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="72518-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="72518-127">-SubscriptionId</span></span>
<span data-ttu-id="72518-128">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="72518-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="72518-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="72518-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="72518-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72518-130">CommonParameters</span></span>
<span data-ttu-id="72518-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72518-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72518-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72518-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72518-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72518-133">INPUTS</span></span>

## <span data-ttu-id="72518-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72518-134">OUTPUTS</span></span>

### <span data-ttu-id="72518-135">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. Api20200802. IMachine</span><span class="sxs-lookup"><span data-stu-id="72518-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="72518-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72518-136">NOTES</span></span>

<span data-ttu-id="72518-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="72518-137">ALIASES</span></span>

## <span data-ttu-id="72518-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72518-138">RELATED LINKS</span></span>

