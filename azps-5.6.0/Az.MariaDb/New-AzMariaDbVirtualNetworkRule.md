---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cfbbfd9472d18d75dea3da68cb4d2e06cf54c9a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970570"
---
# <span data-ttu-id="d91e0-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d91e0-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="d91e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d91e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d91e0-103">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d91e0-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="d91e0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d91e0-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d91e0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d91e0-105">DESCRIPTION</span></span>
<span data-ttu-id="d91e0-106">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d91e0-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="d91e0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d91e0-107">EXAMPLES</span></span>

### <span data-ttu-id="d91e0-108">Przykład 1. Tworzenie reguły sieci wirtualnej dla bazy danych MariaDB</span><span class="sxs-lookup"><span data-stu-id="d91e0-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="d91e0-109">To polecenie tworzy regułę sieci wirtualnej dla bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d91e0-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="d91e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d91e0-110">PARAMETERS</span></span>

### <span data-ttu-id="d91e0-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d91e0-111">-AsJob</span></span>
<span data-ttu-id="d91e0-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d91e0-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d91e0-113">-DefaultProfile</span></span>
<span data-ttu-id="d91e0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d91e0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d91e0-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d91e0-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="d91e0-116">Utwórz regułę zapory, zanim sieć wirtualna będzie włączona dla punktu końcowego usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="d91e0-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91e0-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d91e0-117">-Name</span></span>
<span data-ttu-id="d91e0-118">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d91e0-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91e0-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d91e0-119">-NoWait</span></span>
<span data-ttu-id="d91e0-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d91e0-120">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91e0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d91e0-121">-PassThru</span></span>
<span data-ttu-id="d91e0-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d91e0-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d91e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="d91e0-124">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="d91e0-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d91e0-125">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d91e0-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d91e0-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d91e0-126">-ServerName</span></span>
<span data-ttu-id="d91e0-127">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="d91e0-127">The name of the server.</span></span>

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

### <span data-ttu-id="d91e0-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d91e0-128">-SubnetId</span></span>
<span data-ttu-id="d91e0-129">Identyfikator ARM sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d91e0-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="d91e0-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d91e0-130">-SubscriptionId</span></span>
<span data-ttu-id="d91e0-131">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d91e0-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91e0-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d91e0-132">-Confirm</span></span>
<span data-ttu-id="d91e0-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d91e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d91e0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d91e0-134">-WhatIf</span></span>
<span data-ttu-id="d91e0-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d91e0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d91e0-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d91e0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d91e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91e0-137">CommonParameters</span></span>
<span data-ttu-id="d91e0-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d91e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91e0-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d91e0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91e0-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d91e0-140">INPUTS</span></span>

## <span data-ttu-id="d91e0-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d91e0-141">OUTPUTS</span></span>

### <span data-ttu-id="d91e0-142">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d91e0-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="d91e0-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d91e0-143">NOTES</span></span>

<span data-ttu-id="d91e0-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d91e0-144">ALIASES</span></span>

## <span data-ttu-id="d91e0-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d91e0-145">RELATED LINKS</span></span>

