---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 26da7e8b0bf3ca24edd9f4abd52f0c27aabf49e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356909"
---
# <span data-ttu-id="32c10-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="32c10-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="32c10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32c10-102">SYNOPSIS</span></span>
<span data-ttu-id="32c10-103">Umożliwia utworzenie lub zaktualizowanie dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="32c10-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="32c10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32c10-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="32c10-105">Opis</span><span class="sxs-lookup"><span data-stu-id="32c10-105">DESCRIPTION</span></span>
<span data-ttu-id="32c10-106">Umożliwia utworzenie lub zaktualizowanie dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="32c10-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="32c10-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32c10-107">EXAMPLES</span></span>

### <span data-ttu-id="32c10-108">Przykład 1. Utwórz nowy AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="32c10-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="32c10-109">Powyższe polecenie tworzy bazę danych tylko do odczytu "mykustodatabase" w klastrze "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="32c10-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="32c10-110">Jest on zgodny z bazą danych "mykustodatabase" z poziomu klastra "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="32c10-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="32c10-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32c10-111">PARAMETERS</span></span>

### <span data-ttu-id="32c10-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32c10-112">-AsJob</span></span>
<span data-ttu-id="32c10-113">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="32c10-113">Run the command as a job</span></span>

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

### <span data-ttu-id="32c10-114">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="32c10-114">-ClusterName</span></span>
<span data-ttu-id="32c10-115">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="32c10-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="32c10-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="32c10-116">-ClusterResourceId</span></span>
<span data-ttu-id="32c10-117">Identyfikator zasobu klastra, w którym znajdują się bazy danych, które chcesz dołączyć.</span><span class="sxs-lookup"><span data-stu-id="32c10-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="32c10-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32c10-118">-DatabaseName</span></span>
<span data-ttu-id="32c10-119">Nazwa bazy danych, którą chcesz dołączyć, użyj \*, jeśli chcesz śledzić wszystkie bieżące i przyszłe bazy danych.</span><span class="sxs-lookup"><span data-stu-id="32c10-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="32c10-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="32c10-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="32c10-121">Rodzajowe modyfikacje podmiotów domyślnych</span><span class="sxs-lookup"><span data-stu-id="32c10-121">The default principals modification kind</span></span>

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

### <span data-ttu-id="32c10-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32c10-122">-DefaultProfile</span></span>
<span data-ttu-id="32c10-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32c10-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32c10-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="32c10-124">-Location</span></span>
<span data-ttu-id="32c10-125">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="32c10-125">Resource location.</span></span>

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

### <span data-ttu-id="32c10-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="32c10-126">-Name</span></span>
<span data-ttu-id="32c10-127">Nazwa dołączonej konfiguracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="32c10-127">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="32c10-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="32c10-128">-NoWait</span></span>
<span data-ttu-id="32c10-129">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="32c10-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="32c10-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32c10-130">-ResourceGroupName</span></span>
<span data-ttu-id="32c10-131">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="32c10-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="32c10-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="32c10-132">-SubscriptionId</span></span>
<span data-ttu-id="32c10-133">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="32c10-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="32c10-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="32c10-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="32c10-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="32c10-135">-Confirm</span></span>
<span data-ttu-id="32c10-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32c10-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32c10-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32c10-137">-WhatIf</span></span>
<span data-ttu-id="32c10-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32c10-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32c10-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="32c10-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32c10-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32c10-140">CommonParameters</span></span>
<span data-ttu-id="32c10-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32c10-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32c10-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32c10-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32c10-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32c10-143">INPUTS</span></span>

## <span data-ttu-id="32c10-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32c10-144">OUTPUTS</span></span>

### <span data-ttu-id="32c10-145">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="32c10-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="32c10-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32c10-146">NOTES</span></span>

<span data-ttu-id="32c10-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="32c10-147">ALIASES</span></span>

## <span data-ttu-id="32c10-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32c10-148">RELATED LINKS</span></span>

