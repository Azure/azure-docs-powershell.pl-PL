---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 858578d36f2f913f903f86b9c556a93d30e2e3b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050080"
---
# <span data-ttu-id="a97fd-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="a97fd-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="a97fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a97fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a97fd-103">Aktualizowanie istniejącej bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="a97fd-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="a97fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a97fd-104">SYNTAX</span></span>

### <span data-ttu-id="a97fd-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a97fd-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a97fd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a97fd-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a97fd-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a97fd-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a97fd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a97fd-108">DESCRIPTION</span></span>
<span data-ttu-id="a97fd-109">Aktualizowanie istniejącej bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="a97fd-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="a97fd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a97fd-110">EXAMPLES</span></span>

### <span data-ttu-id="a97fd-111">Przykład 1 — Aktualizowanie istniejącej bazy danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="a97fd-111">Example 1 - Update an existing database by name</span></span>

```
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="a97fd-112">Powyższe polecenie aktualizuje okres usuwania nietrwałego Kusto bazy danych "mykustodatabase" w klastrze "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="a97fd-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="a97fd-113">Przykład 2 — aktualizowanie istniejącej bazy danych za pomocą połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="a97fd-113">Example 2 - Update an existing database by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Update-AzKustoDatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="a97fd-114">Powyższe polecenie pobiera bazę danych Kusto "mykustodatabase" w klastrze "mykustocluster" w grupie zasobów "testrg" przy użyciu `Get-AzKustoDatabase` polecenia cmdlet, a następnie przekazuje wynik w celu `Update-AzKustoDatabase` zaktualizowania okresu usuwania wstępnego bazy danych do pięciu dni.</span><span class="sxs-lookup"><span data-stu-id="a97fd-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="a97fd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a97fd-115">PARAMETERS</span></span>

### <span data-ttu-id="a97fd-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="a97fd-116">-ClusterName</span></span>
<span data-ttu-id="a97fd-117">Nazwa klastra, w którym istnieje baza danych</span><span class="sxs-lookup"><span data-stu-id="a97fd-117">Name of cluster under which the database exists</span></span>

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

### <span data-ttu-id="a97fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a97fd-118">-DefaultProfile</span></span>
<span data-ttu-id="a97fd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a97fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a97fd-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a97fd-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="a97fd-121">Liczba dni przechowywania danych w pamięci podręcznej w przypadku szybkich kwerend</span><span class="sxs-lookup"><span data-stu-id="a97fd-121">The number of days that data should be kept in cache for fast queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a97fd-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a97fd-122">-InputObject</span></span>
<span data-ttu-id="a97fd-123">Obiekt bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="a97fd-123">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a97fd-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a97fd-124">-Name</span></span>
<span data-ttu-id="a97fd-125">Nazwa bazy danych do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="a97fd-125">Name of the database to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a97fd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a97fd-126">-ResourceGroupName</span></span>
<span data-ttu-id="a97fd-127">Nazwa grupy zasobów, pod którą klaster istnieje.</span><span class="sxs-lookup"><span data-stu-id="a97fd-127">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="a97fd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a97fd-128">-ResourceId</span></span>
<span data-ttu-id="a97fd-129">Identyfikator zasobu bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="a97fd-129">Kusto database ResourceID.</span></span>

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

### <span data-ttu-id="a97fd-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a97fd-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="a97fd-131">Liczba dni przechowywania danych przed uzyskaniem dostępu do zapytań</span><span class="sxs-lookup"><span data-stu-id="a97fd-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a97fd-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a97fd-132">-Confirm</span></span>
<span data-ttu-id="a97fd-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a97fd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a97fd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a97fd-134">-WhatIf</span></span>
<span data-ttu-id="a97fd-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a97fd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a97fd-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a97fd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a97fd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a97fd-137">CommonParameters</span></span>
<span data-ttu-id="a97fd-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a97fd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a97fd-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a97fd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a97fd-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a97fd-140">INPUTS</span></span>

### <span data-ttu-id="a97fd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a97fd-141">System.String</span></span>

### <span data-ttu-id="a97fd-142">Microsoft. Azure. Commands. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="a97fd-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="a97fd-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a97fd-143">OUTPUTS</span></span>

### <span data-ttu-id="a97fd-144">Microsoft. Azure. Commands. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="a97fd-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="a97fd-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a97fd-145">NOTES</span></span>

## <span data-ttu-id="a97fd-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a97fd-146">RELATED LINKS</span></span>
