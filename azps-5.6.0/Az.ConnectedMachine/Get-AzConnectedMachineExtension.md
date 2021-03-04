---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: 423834d0dc7a324743795e0d54324a51f1cd04ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012401"
---
# <span data-ttu-id="64aaa-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="64aaa-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="64aaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="64aaa-103">Operacja uzyskania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="64aaa-103">The operation to get the extension.</span></span>

## <span data-ttu-id="64aaa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64aaa-104">SYNTAX</span></span>

### <span data-ttu-id="64aaa-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="64aaa-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64aaa-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="64aaa-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="64aaa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="64aaa-107">DESCRIPTION</span></span>
<span data-ttu-id="64aaa-108">Operacja uzyskania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="64aaa-108">The operation to get the extension.</span></span>

## <span data-ttu-id="64aaa-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64aaa-109">EXAMPLES</span></span>

### <span data-ttu-id="64aaa-110">Przykład 1. Lista wszystkich rozszerzeń dla komputera</span><span class="sxs-lookup"><span data-stu-id="64aaa-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="64aaa-111">Lista wszystkich rozszerzeń dla określonego komputera.</span><span class="sxs-lookup"><span data-stu-id="64aaa-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="64aaa-112">Przykład 2. Uzyskiwanie określonego rozszerzenia na komputerze</span><span class="sxs-lookup"><span data-stu-id="64aaa-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="64aaa-113">Pobiera określone rozszerzenie na komputerze.</span><span class="sxs-lookup"><span data-stu-id="64aaa-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="64aaa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64aaa-114">PARAMETERS</span></span>

### <span data-ttu-id="64aaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64aaa-115">-DefaultProfile</span></span>
<span data-ttu-id="64aaa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="64aaa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64aaa-117">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="64aaa-117">-Expand</span></span>
<span data-ttu-id="64aaa-118">Wyrażenie rozwijania, które ma być stosowane do operacji.</span><span class="sxs-lookup"><span data-stu-id="64aaa-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64aaa-119">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="64aaa-119">-MachineName</span></span>
<span data-ttu-id="64aaa-120">Nazwa komputera zawierającego rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="64aaa-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="64aaa-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="64aaa-121">-Name</span></span>
<span data-ttu-id="64aaa-122">Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="64aaa-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="64aaa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64aaa-123">-ResourceGroupName</span></span>
<span data-ttu-id="64aaa-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64aaa-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="64aaa-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64aaa-125">-SubscriptionId</span></span>
<span data-ttu-id="64aaa-126">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64aaa-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="64aaa-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="64aaa-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="64aaa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64aaa-128">CommonParameters</span></span>
<span data-ttu-id="64aaa-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64aaa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64aaa-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64aaa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64aaa-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64aaa-131">INPUTS</span></span>

## <span data-ttu-id="64aaa-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64aaa-132">OUTPUTS</span></span>

### <span data-ttu-id="64aaa-133">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="64aaa-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="64aaa-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64aaa-134">NOTES</span></span>

<span data-ttu-id="64aaa-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="64aaa-135">ALIASES</span></span>

## <span data-ttu-id="64aaa-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64aaa-136">RELATED LINKS</span></span>

