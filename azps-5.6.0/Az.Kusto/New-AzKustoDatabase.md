---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: b3e6319de721d63071c730bb43e1ef7db5a46e25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956129"
---
# <span data-ttu-id="aff83-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="aff83-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="aff83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aff83-102">SYNOPSIS</span></span>
<span data-ttu-id="aff83-103">Tworzy lub aktualizuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="aff83-103">Creates or updates a database.</span></span>

## <span data-ttu-id="aff83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aff83-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aff83-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="aff83-105">DESCRIPTION</span></span>
<span data-ttu-id="aff83-106">Tworzy lub aktualizuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="aff83-106">Creates or updates a database.</span></span>

## <span data-ttu-id="aff83-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aff83-107">EXAMPLES</span></span>

### <span data-ttu-id="aff83-108">Przykład 1. Tworzenie nowej bazy danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="aff83-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="aff83-109">Powyższe polecenie tworzy nową bazę danych Kusto o nazwie "mykustodatabase" w istniejącym klastrze "testnewkustocluster" znalezionym w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="aff83-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="aff83-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aff83-110">PARAMETERS</span></span>

### <span data-ttu-id="aff83-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="aff83-111">-AsJob</span></span>
<span data-ttu-id="aff83-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="aff83-112">Run the command as a job</span></span>

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

### <span data-ttu-id="aff83-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="aff83-113">-ClusterName</span></span>
<span data-ttu-id="aff83-114">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="aff83-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="aff83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff83-115">-DefaultProfile</span></span>
<span data-ttu-id="aff83-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aff83-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aff83-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="aff83-117">-HotCachePeriod</span></span>
<span data-ttu-id="aff83-118">Czas przechowywania danych w pamięci podręcznej szybkich zapytań w programie TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="aff83-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff83-119">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="aff83-119">-Kind</span></span>
<span data-ttu-id="aff83-120">Typ bazy danych</span><span class="sxs-lookup"><span data-stu-id="aff83-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff83-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="aff83-121">-Location</span></span>
<span data-ttu-id="aff83-122">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="aff83-122">Resource location.</span></span>

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

### <span data-ttu-id="aff83-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="aff83-123">-Name</span></span>
<span data-ttu-id="aff83-124">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="aff83-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff83-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aff83-125">-NoWait</span></span>
<span data-ttu-id="aff83-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="aff83-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aff83-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff83-127">-ResourceGroupName</span></span>
<span data-ttu-id="aff83-128">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="aff83-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="aff83-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="aff83-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="aff83-130">Czas przechowywania danych, zanim przestanie być dostępny dla zapytań w programie TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="aff83-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff83-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aff83-131">-SubscriptionId</span></span>
<span data-ttu-id="aff83-132">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aff83-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aff83-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="aff83-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aff83-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aff83-134">-Confirm</span></span>
<span data-ttu-id="aff83-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aff83-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aff83-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aff83-136">-WhatIf</span></span>
<span data-ttu-id="aff83-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aff83-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aff83-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aff83-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aff83-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff83-139">CommonParameters</span></span>
<span data-ttu-id="aff83-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aff83-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff83-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aff83-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff83-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aff83-142">INPUTS</span></span>

## <span data-ttu-id="aff83-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aff83-143">OUTPUTS</span></span>

### <span data-ttu-id="aff83-144">Microsoft.Azure.PowerShell.cmdlet.kusto.models.api20200918.iDatabase</span><span class="sxs-lookup"><span data-stu-id="aff83-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="aff83-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aff83-145">NOTES</span></span>

<span data-ttu-id="aff83-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="aff83-146">ALIASES</span></span>

## <span data-ttu-id="aff83-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aff83-147">RELATED LINKS</span></span>

