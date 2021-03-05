---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: 1705b053939d8c5b67666d550c6c8340e892ae45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987673"
---
# <span data-ttu-id="9de55-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9de55-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="9de55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9de55-102">SYNOPSIS</span></span>
<span data-ttu-id="9de55-103">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9de55-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="9de55-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9de55-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9de55-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9de55-105">DESCRIPTION</span></span>
<span data-ttu-id="9de55-106">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9de55-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="9de55-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9de55-107">EXAMPLES</span></span>

### <span data-ttu-id="9de55-108">Przykład 1. Tworzenie nowej reguły sieci wirtualnej serwera PostgreSql</span><span class="sxs-lookup"><span data-stu-id="9de55-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="9de55-109">Te polecenia cmdlet tworzą regułę wirtualnej sieci na serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="9de55-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="9de55-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9de55-110">PARAMETERS</span></span>

### <span data-ttu-id="9de55-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9de55-111">-AsJob</span></span>
<span data-ttu-id="9de55-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9de55-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9de55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de55-113">-DefaultProfile</span></span>
<span data-ttu-id="9de55-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9de55-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de55-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9de55-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="9de55-116">Utwórz regułę zapory, zanim sieć wirtualna będzie włączona dla punktu końcowego usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="9de55-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="9de55-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9de55-117">-Name</span></span>
<span data-ttu-id="9de55-118">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9de55-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="9de55-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9de55-119">-NoWait</span></span>
<span data-ttu-id="9de55-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9de55-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9de55-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9de55-121">-PassThru</span></span>
<span data-ttu-id="9de55-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9de55-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9de55-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de55-123">-ResourceGroupName</span></span>
<span data-ttu-id="9de55-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9de55-124">The name of the resource group.</span></span>
<span data-ttu-id="9de55-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9de55-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9de55-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9de55-126">-ServerName</span></span>
<span data-ttu-id="9de55-127">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9de55-127">The name of the server.</span></span>

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

### <span data-ttu-id="9de55-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9de55-128">-SubnetId</span></span>
<span data-ttu-id="9de55-129">Identyfikator ARM sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9de55-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="9de55-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9de55-130">-SubscriptionId</span></span>
<span data-ttu-id="9de55-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9de55-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9de55-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9de55-132">-Confirm</span></span>
<span data-ttu-id="9de55-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9de55-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de55-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de55-134">-WhatIf</span></span>
<span data-ttu-id="9de55-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9de55-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9de55-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9de55-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de55-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de55-137">CommonParameters</span></span>
<span data-ttu-id="9de55-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de55-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de55-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9de55-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de55-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9de55-140">INPUTS</span></span>

## <span data-ttu-id="9de55-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9de55-141">OUTPUTS</span></span>

### <span data-ttu-id="9de55-142">Microsoft.Azure.PowerShell.cmdlet.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9de55-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="9de55-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9de55-143">NOTES</span></span>

<span data-ttu-id="9de55-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9de55-144">ALIASES</span></span>

## <span data-ttu-id="9de55-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9de55-145">RELATED LINKS</span></span>

