---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b540b82ed07e42a6789a2603299508c21c7c3aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983482"
---
# <span data-ttu-id="8c35b-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c35b-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="8c35b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c35b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c35b-103">Tworzy lub aktualizuje załączoną konfigurację bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8c35b-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="8c35b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c35b-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8c35b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c35b-105">DESCRIPTION</span></span>
<span data-ttu-id="8c35b-106">Tworzy lub aktualizuje załączoną konfigurację bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8c35b-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="8c35b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c35b-107">EXAMPLES</span></span>

### <span data-ttu-id="8c35b-108">Przykład 1. Tworzenie nowej konfiguracji AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c35b-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="8c35b-109">Powyższe polecenie tworzy bazę danych ReadOnly "mykustodatabase" w klastrze "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="8c35b-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="8c35b-110">Następuje on po bazie danych "mykustodatabase" z grupy "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="8c35b-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="8c35b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c35b-111">PARAMETERS</span></span>

### <span data-ttu-id="8c35b-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8c35b-112">-AsJob</span></span>
<span data-ttu-id="8c35b-113">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8c35b-113">Run the command as a job</span></span>

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

### <span data-ttu-id="8c35b-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8c35b-114">-ClusterName</span></span>
<span data-ttu-id="8c35b-115">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="8c35b-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8c35b-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="8c35b-116">-ClusterResourceId</span></span>
<span data-ttu-id="8c35b-117">Identyfikator zasobu klasteru, w którym chcesz dołączyć bazy danych, znajduje się.</span><span class="sxs-lookup"><span data-stu-id="8c35b-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="8c35b-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8c35b-118">-DatabaseName</span></span>
<span data-ttu-id="8c35b-119">Nazwa bazy danych, którą chcesz dołączyć, użyj \*, jeśli chcesz obserwować wszystkie bieżące i przyszłe bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8c35b-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="8c35b-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="8c35b-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="8c35b-121">Domyślny rodzaj modyfikacji głównych</span><span class="sxs-lookup"><span data-stu-id="8c35b-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c35b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c35b-122">-DefaultProfile</span></span>
<span data-ttu-id="8c35b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c35b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c35b-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8c35b-124">-Location</span></span>
<span data-ttu-id="8c35b-125">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="8c35b-125">Resource location.</span></span>

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

### <span data-ttu-id="8c35b-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c35b-126">-Name</span></span>
<span data-ttu-id="8c35b-127">Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8c35b-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c35b-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8c35b-128">-NoWait</span></span>
<span data-ttu-id="8c35b-129">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8c35b-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8c35b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c35b-130">-ResourceGroupName</span></span>
<span data-ttu-id="8c35b-131">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="8c35b-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8c35b-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c35b-132">-SubscriptionId</span></span>
<span data-ttu-id="8c35b-133">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8c35b-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8c35b-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="8c35b-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8c35b-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c35b-135">-Confirm</span></span>
<span data-ttu-id="8c35b-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c35b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c35b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c35b-137">-WhatIf</span></span>
<span data-ttu-id="8c35b-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c35b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c35b-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c35b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c35b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c35b-140">CommonParameters</span></span>
<span data-ttu-id="8c35b-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c35b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c35b-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c35b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c35b-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c35b-143">INPUTS</span></span>

## <span data-ttu-id="8c35b-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c35b-144">OUTPUTS</span></span>

### <span data-ttu-id="8c35b-145">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c35b-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="8c35b-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c35b-146">NOTES</span></span>

<span data-ttu-id="8c35b-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8c35b-147">ALIASES</span></span>

## <span data-ttu-id="8c35b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c35b-148">RELATED LINKS</span></span>

