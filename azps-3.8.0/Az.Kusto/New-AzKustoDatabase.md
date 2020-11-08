---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: ed039eefe46a1527948e7fffc3030f209a91b0c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050097"
---
# <span data-ttu-id="19909-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="19909-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="19909-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19909-102">SYNOPSIS</span></span>
<span data-ttu-id="19909-103">Tworzy nową bazę danych Kusto w istniejącym klastrze.</span><span class="sxs-lookup"><span data-stu-id="19909-103">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="19909-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19909-104">SYNTAX</span></span>

### <span data-ttu-id="19909-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="19909-105">ByNameAndResourceGroup (Default)</span></span>
```
New-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19909-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="19909-106">ByResourceId</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19909-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="19909-107">ByInputObject</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-InputObject] <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19909-108">Opis</span><span class="sxs-lookup"><span data-stu-id="19909-108">DESCRIPTION</span></span>
<span data-ttu-id="19909-109">Tworzy nową bazę danych Kusto w istniejącym klastrze.</span><span class="sxs-lookup"><span data-stu-id="19909-109">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="19909-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19909-110">EXAMPLES</span></span>

### <span data-ttu-id="19909-111">Przykład 1 — Tworzenie nowej bazy danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="19909-111">Example 1 - Create a new Kusto database by name</span></span>

```
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 4 -HotCachePeriodInDays 2

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 4
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="19909-112">Powyższe polecenie tworzy nową Kusto bazę danych o nazwie "mykustodatabase" w istniejącym klastrze "mykustocluster" odnalezionym w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="19909-112">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="19909-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19909-113">PARAMETERS</span></span>

### <span data-ttu-id="19909-114">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="19909-114">-ClusterName</span></span>
<span data-ttu-id="19909-115">Nazwa klastra, w którym chcesz utworzyć bazę danych.</span><span class="sxs-lookup"><span data-stu-id="19909-115">Name of cluster under which you want to create the database.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19909-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19909-116">-DefaultProfile</span></span>
<span data-ttu-id="19909-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19909-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19909-118">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="19909-118">-HotCachePeriodInDays</span></span>
<span data-ttu-id="19909-119">Liczba dni danych, które powinny być przechowywane w pamięci podręcznej dla szybkich kwerend.</span><span class="sxs-lookup"><span data-stu-id="19909-119">The number of days of data that should be kept in cache for fast queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19909-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="19909-120">-InputObject</span></span>
<span data-ttu-id="19909-121">Obiekt klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="19909-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19909-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="19909-122">-Name</span></span>
<span data-ttu-id="19909-123">Nazwa bazy danych, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="19909-123">Name of the database to be created.</span></span>

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

### <span data-ttu-id="19909-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19909-124">-ResourceGroupName</span></span>
<span data-ttu-id="19909-125">Nazwa grupy zasobów, pod którą klaster istnieje.</span><span class="sxs-lookup"><span data-stu-id="19909-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19909-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19909-126">-ResourceId</span></span>
<span data-ttu-id="19909-127">Kusto identyfikator zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="19909-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19909-128">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="19909-128">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="19909-129">Liczba dni przechowywania danych, zanim nie będzie można jej uzyskać dostęp do zapytań.</span><span class="sxs-lookup"><span data-stu-id="19909-129">The number of days data should be kept before it stops being accessible to queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19909-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19909-130">-Confirm</span></span>
<span data-ttu-id="19909-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19909-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19909-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19909-132">-WhatIf</span></span>
<span data-ttu-id="19909-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19909-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19909-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19909-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19909-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19909-135">CommonParameters</span></span>
<span data-ttu-id="19909-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19909-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19909-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19909-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19909-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19909-138">INPUTS</span></span>

### <span data-ttu-id="19909-139">System. String</span><span class="sxs-lookup"><span data-stu-id="19909-139">System.String</span></span>

### <span data-ttu-id="19909-140">Microsoft. Azure. Commands. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="19909-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="19909-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19909-141">OUTPUTS</span></span>

### <span data-ttu-id="19909-142">Microsoft. Azure. Commands. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="19909-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="19909-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19909-143">NOTES</span></span>

## <span data-ttu-id="19909-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19909-144">RELATED LINKS</span></span>
