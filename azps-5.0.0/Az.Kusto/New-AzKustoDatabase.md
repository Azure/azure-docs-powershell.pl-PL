---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: dc0b4ea1616c916edacaf4d5a4a2b431e7f7d113
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233462"
---
# <span data-ttu-id="46422-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="46422-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="46422-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46422-102">SYNOPSIS</span></span>
<span data-ttu-id="46422-103">Tworzenie lub aktualizowanie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="46422-103">Creates or updates a database.</span></span>

## <span data-ttu-id="46422-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46422-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46422-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46422-105">DESCRIPTION</span></span>
<span data-ttu-id="46422-106">Tworzenie lub aktualizowanie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="46422-106">Creates or updates a database.</span></span>

## <span data-ttu-id="46422-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46422-107">EXAMPLES</span></span>

### <span data-ttu-id="46422-108">Przykład 1. Tworzenie nowej bazy danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="46422-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="46422-109">Powyższe polecenie tworzy nową Kusto bazę danych o nazwie "mykustodatabase" w istniejącym klastrze "testnewkustocluster" odnalezionym w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="46422-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="46422-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46422-110">PARAMETERS</span></span>

### <span data-ttu-id="46422-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46422-111">-AsJob</span></span>
<span data-ttu-id="46422-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="46422-112">Run the command as a job</span></span>

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

### <span data-ttu-id="46422-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="46422-113">-ClusterName</span></span>
<span data-ttu-id="46422-114">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="46422-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="46422-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46422-115">-DefaultProfile</span></span>
<span data-ttu-id="46422-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46422-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46422-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="46422-117">-HotCachePeriod</span></span>
<span data-ttu-id="46422-118">Czas przechowywania danych w pamięci podręcznej w przypadku szybkiego wykonywania kwerend w polu TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="46422-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="46422-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="46422-119">-Kind</span></span>
<span data-ttu-id="46422-120">Rodzaj bazy danych</span><span class="sxs-lookup"><span data-stu-id="46422-120">Kind of the database</span></span>

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

### <span data-ttu-id="46422-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="46422-121">-Location</span></span>
<span data-ttu-id="46422-122">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="46422-122">Resource location.</span></span>

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

### <span data-ttu-id="46422-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46422-123">-Name</span></span>
<span data-ttu-id="46422-124">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="46422-124">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="46422-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="46422-125">-NoWait</span></span>
<span data-ttu-id="46422-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="46422-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="46422-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46422-127">-ResourceGroupName</span></span>
<span data-ttu-id="46422-128">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="46422-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="46422-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="46422-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="46422-130">Czas przechowywania danych przed zakończeniem dostępu do zapytań w polu TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="46422-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="46422-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="46422-131">-SubscriptionId</span></span>
<span data-ttu-id="46422-132">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46422-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="46422-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="46422-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="46422-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46422-134">-Confirm</span></span>
<span data-ttu-id="46422-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46422-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46422-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46422-136">-WhatIf</span></span>
<span data-ttu-id="46422-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46422-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46422-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46422-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46422-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46422-139">CommonParameters</span></span>
<span data-ttu-id="46422-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46422-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46422-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46422-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46422-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46422-142">INPUTS</span></span>

## <span data-ttu-id="46422-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46422-143">OUTPUTS</span></span>

### <span data-ttu-id="46422-144">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="46422-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="46422-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46422-145">NOTES</span></span>

<span data-ttu-id="46422-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="46422-146">ALIASES</span></span>

## <span data-ttu-id="46422-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46422-147">RELATED LINKS</span></span>

