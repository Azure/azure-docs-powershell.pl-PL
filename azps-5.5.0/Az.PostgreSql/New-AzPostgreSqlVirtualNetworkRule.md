---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193115"
---
# <span data-ttu-id="0e97e-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0e97e-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="0e97e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e97e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e97e-103">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0e97e-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="0e97e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e97e-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0e97e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e97e-105">DESCRIPTION</span></span>
<span data-ttu-id="0e97e-106">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0e97e-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="0e97e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e97e-107">EXAMPLES</span></span>

### <span data-ttu-id="0e97e-108">Przykład 1. Tworzenie nowej reguły sieci wirtualnej serwera PostgreSql</span><span class="sxs-lookup"><span data-stu-id="0e97e-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="0e97e-109">Te polecenia cmdlet tworzą regułę wirtualnej sieci na serwerze PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="0e97e-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="0e97e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e97e-110">PARAMETERS</span></span>

### <span data-ttu-id="0e97e-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0e97e-111">-AsJob</span></span>
<span data-ttu-id="0e97e-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0e97e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0e97e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e97e-113">-DefaultProfile</span></span>
<span data-ttu-id="0e97e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e97e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e97e-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e97e-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="0e97e-116">Utwórz regułę zapory, zanim sieć wirtualna będzie włączona dla punktu końcowego usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="0e97e-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="0e97e-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0e97e-117">-Name</span></span>
<span data-ttu-id="0e97e-118">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0e97e-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="0e97e-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0e97e-119">-NoWait</span></span>
<span data-ttu-id="0e97e-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0e97e-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0e97e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e97e-121">-PassThru</span></span>
<span data-ttu-id="0e97e-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="0e97e-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0e97e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e97e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0e97e-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e97e-124">The name of the resource group.</span></span>
<span data-ttu-id="0e97e-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="0e97e-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0e97e-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0e97e-126">-ServerName</span></span>
<span data-ttu-id="0e97e-127">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="0e97e-127">The name of the server.</span></span>

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

### <span data-ttu-id="0e97e-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0e97e-128">-SubnetId</span></span>
<span data-ttu-id="0e97e-129">Identyfikator ARM sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0e97e-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="0e97e-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e97e-130">-SubscriptionId</span></span>
<span data-ttu-id="0e97e-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0e97e-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0e97e-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e97e-132">-Confirm</span></span>
<span data-ttu-id="0e97e-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0e97e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e97e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e97e-134">-WhatIf</span></span>
<span data-ttu-id="0e97e-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e97e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e97e-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0e97e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e97e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e97e-137">CommonParameters</span></span>
<span data-ttu-id="0e97e-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e97e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e97e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e97e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e97e-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e97e-140">INPUTS</span></span>

## <span data-ttu-id="0e97e-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e97e-141">OUTPUTS</span></span>

### <span data-ttu-id="0e97e-142">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0e97e-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="0e97e-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e97e-143">NOTES</span></span>

<span data-ttu-id="0e97e-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0e97e-144">ALIASES</span></span>

## <span data-ttu-id="0e97e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e97e-145">RELATED LINKS</span></span>

