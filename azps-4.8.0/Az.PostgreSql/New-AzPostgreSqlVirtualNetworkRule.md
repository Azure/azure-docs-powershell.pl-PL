---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219317"
---
# <span data-ttu-id="e848a-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e848a-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="e848a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e848a-102">SYNOPSIS</span></span>
<span data-ttu-id="e848a-103">Umożliwia utworzenie lub zaktualizowanie istniejącej reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e848a-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e848a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e848a-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e848a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e848a-105">DESCRIPTION</span></span>
<span data-ttu-id="e848a-106">Umożliwia utworzenie lub zaktualizowanie istniejącej reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e848a-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e848a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e848a-107">EXAMPLES</span></span>

### <span data-ttu-id="e848a-108">Przykład 1. Utwórz nową regułę sieci wirtualnej serwera PostgreSql</span><span class="sxs-lookup"><span data-stu-id="e848a-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="e848a-109">Te polecenia cmdlet tworzą regułę sieci wirtualnej serwera PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="e848a-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="e848a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e848a-110">PARAMETERS</span></span>

### <span data-ttu-id="e848a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e848a-111">-AsJob</span></span>
<span data-ttu-id="e848a-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e848a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e848a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e848a-113">-DefaultProfile</span></span>
<span data-ttu-id="e848a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e848a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e848a-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e848a-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e848a-116">Tworzenie reguły zapory przed włączeniem punktu końcowego usługi VNET w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e848a-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="e848a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e848a-117">-Name</span></span>
<span data-ttu-id="e848a-118">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e848a-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e848a-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e848a-119">-NoWait</span></span>
<span data-ttu-id="e848a-120">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e848a-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e848a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e848a-121">-PassThru</span></span>
<span data-ttu-id="e848a-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="e848a-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e848a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e848a-123">-ResourceGroupName</span></span>
<span data-ttu-id="e848a-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e848a-124">The name of the resource group.</span></span>
<span data-ttu-id="e848a-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="e848a-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e848a-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e848a-126">-ServerName</span></span>
<span data-ttu-id="e848a-127">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="e848a-127">The name of the server.</span></span>

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

### <span data-ttu-id="e848a-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e848a-128">-SubnetId</span></span>
<span data-ttu-id="e848a-129">Identyfikator zasobu ARM podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e848a-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="e848a-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e848a-130">-SubscriptionId</span></span>
<span data-ttu-id="e848a-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e848a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e848a-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e848a-132">-Confirm</span></span>
<span data-ttu-id="e848a-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e848a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e848a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e848a-134">-WhatIf</span></span>
<span data-ttu-id="e848a-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e848a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e848a-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e848a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e848a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e848a-137">CommonParameters</span></span>
<span data-ttu-id="e848a-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e848a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e848a-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e848a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e848a-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e848a-140">INPUTS</span></span>

## <span data-ttu-id="e848a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e848a-141">OUTPUTS</span></span>

### <span data-ttu-id="e848a-142">Microsoft. Azure. PowerShell. polecenia. PostgreSql. models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e848a-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="e848a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e848a-143">NOTES</span></span>

<span data-ttu-id="e848a-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e848a-144">ALIASES</span></span>

## <span data-ttu-id="e848a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e848a-145">RELATED LINKS</span></span>

