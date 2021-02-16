---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180051"
---
# <span data-ttu-id="c3168-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c3168-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="c3168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3168-102">SYNOPSIS</span></span>
<span data-ttu-id="c3168-103">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c3168-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="c3168-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3168-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3168-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3168-105">DESCRIPTION</span></span>
<span data-ttu-id="c3168-106">Tworzy lub aktualizuje istniejącą regułę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c3168-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="c3168-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3168-107">EXAMPLES</span></span>

### <span data-ttu-id="c3168-108">Przykład 1. Tworzenie nowej reguły sieci wirtualnej serwera MySql</span><span class="sxs-lookup"><span data-stu-id="c3168-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="c3168-109">Te polecenia cmdlet tworzą regułę wirtualnej sieci na serwerze MySql.</span><span class="sxs-lookup"><span data-stu-id="c3168-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="c3168-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3168-110">PARAMETERS</span></span>

### <span data-ttu-id="c3168-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c3168-111">-AsJob</span></span>
<span data-ttu-id="c3168-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="c3168-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c3168-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3168-113">-DefaultProfile</span></span>
<span data-ttu-id="c3168-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3168-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3168-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3168-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="c3168-116">Utwórz regułę zapory, zanim sieć wirtualna będzie włączona dla punktu końcowego usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="c3168-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="c3168-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c3168-117">-Name</span></span>
<span data-ttu-id="c3168-118">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c3168-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c3168-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c3168-119">-NoWait</span></span>
<span data-ttu-id="c3168-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="c3168-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c3168-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3168-121">-PassThru</span></span>
<span data-ttu-id="c3168-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="c3168-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c3168-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3168-123">-ResourceGroupName</span></span>
<span data-ttu-id="c3168-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3168-124">The name of the resource group.</span></span>
<span data-ttu-id="c3168-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="c3168-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c3168-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c3168-126">-ServerName</span></span>
<span data-ttu-id="c3168-127">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="c3168-127">The name of the server.</span></span>

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

### <span data-ttu-id="c3168-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c3168-128">-SubnetId</span></span>
<span data-ttu-id="c3168-129">Identyfikator ARM sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c3168-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="c3168-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3168-130">-SubscriptionId</span></span>
<span data-ttu-id="c3168-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c3168-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c3168-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3168-132">-Confirm</span></span>
<span data-ttu-id="c3168-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c3168-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3168-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3168-134">-WhatIf</span></span>
<span data-ttu-id="c3168-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3168-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3168-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c3168-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3168-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3168-137">CommonParameters</span></span>
<span data-ttu-id="c3168-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3168-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3168-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3168-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3168-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3168-140">INPUTS</span></span>

## <span data-ttu-id="c3168-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c3168-141">OUTPUTS</span></span>

### <span data-ttu-id="c3168-142">Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c3168-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="c3168-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3168-143">NOTES</span></span>

<span data-ttu-id="c3168-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c3168-144">ALIASES</span></span>

## <span data-ttu-id="c3168-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3168-145">RELATED LINKS</span></span>

