---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 05d01d776f03ec3bbfe4e9bf6bd438ba8f002afb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705058"
---
# <span data-ttu-id="42f32-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="42f32-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="42f32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42f32-102">SYNOPSIS</span></span>
<span data-ttu-id="42f32-103">Aktualizowanie istniejącej bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="42f32-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="42f32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42f32-104">SYNTAX</span></span>

### <span data-ttu-id="42f32-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="42f32-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42f32-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42f32-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42f32-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="42f32-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42f32-108">Opis</span><span class="sxs-lookup"><span data-stu-id="42f32-108">DESCRIPTION</span></span>
<span data-ttu-id="42f32-109">Aktualizowanie istniejącej bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="42f32-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="42f32-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42f32-110">EXAMPLES</span></span>

### <span data-ttu-id="42f32-111">Przykład 1 — Aktualizowanie istniejącej bazy danych według nazwy</span><span class="sxs-lookup"><span data-stu-id="42f32-111">Example 1 - Update an existing database by name</span></span>

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

<span data-ttu-id="42f32-112">Powyższe polecenie aktualizuje okres usuwania nietrwałego Kusto bazy danych "mykustodatabase" w klastrze "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="42f32-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="42f32-113">Przykład 2 — aktualizowanie istniejącej bazy danych za pomocą połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="42f32-113">Example 2 - Update an existing database by piping</span></span>

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

<span data-ttu-id="42f32-114">Powyższe polecenie pobiera bazę danych Kusto "mykustodatabase" w klastrze "mykustocluster" w grupie zasobów "testrg" przy użyciu `Get-AzKustoDatabase` polecenia cmdlet, a następnie przekazuje wynik w celu `Update-AzKustoDatabase` zaktualizowania okresu usuwania wstępnego bazy danych do pięciu dni.</span><span class="sxs-lookup"><span data-stu-id="42f32-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="42f32-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42f32-115">PARAMETERS</span></span>

### <span data-ttu-id="42f32-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="42f32-116">-ClusterName</span></span>
<span data-ttu-id="42f32-117">Nazwa klastra, w którym istnieje baza danych</span><span class="sxs-lookup"><span data-stu-id="42f32-117">Name of cluster under which the database exists</span></span>

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

### <span data-ttu-id="42f32-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f32-118">-DefaultProfile</span></span>
<span data-ttu-id="42f32-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42f32-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42f32-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="42f32-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="42f32-121">Liczba dni przechowywania danych w pamięci podręcznej w przypadku szybkich kwerend</span><span class="sxs-lookup"><span data-stu-id="42f32-121">The number of days that data should be kept in cache for fast queries</span></span>

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

### <span data-ttu-id="42f32-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42f32-122">-InputObject</span></span>
<span data-ttu-id="42f32-123">Obiekt bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="42f32-123">Kusto database object.</span></span>

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

### <span data-ttu-id="42f32-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42f32-124">-Name</span></span>
<span data-ttu-id="42f32-125">Nazwa bazy danych do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="42f32-125">Name of the database to update</span></span>

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

### <span data-ttu-id="42f32-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f32-126">-ResourceGroupName</span></span>
<span data-ttu-id="42f32-127">Nazwa grupy zasobów, pod którą klaster istnieje.</span><span class="sxs-lookup"><span data-stu-id="42f32-127">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="42f32-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42f32-128">-ResourceId</span></span>
<span data-ttu-id="42f32-129">Identyfikator zasobu bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="42f32-129">Kusto database ResourceID.</span></span>

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

### <span data-ttu-id="42f32-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="42f32-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="42f32-131">Liczba dni przechowywania danych przed uzyskaniem dostępu do zapytań</span><span class="sxs-lookup"><span data-stu-id="42f32-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

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

### <span data-ttu-id="42f32-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42f32-132">-Confirm</span></span>
<span data-ttu-id="42f32-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42f32-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42f32-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42f32-134">-WhatIf</span></span>
<span data-ttu-id="42f32-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42f32-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42f32-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42f32-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42f32-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f32-137">CommonParameters</span></span>
<span data-ttu-id="42f32-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f32-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f32-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f32-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f32-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42f32-140">INPUTS</span></span>

### <span data-ttu-id="42f32-141">System. String</span><span class="sxs-lookup"><span data-stu-id="42f32-141">System.String</span></span>

### <span data-ttu-id="42f32-142">Microsoft. Azure. Commands. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="42f32-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="42f32-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42f32-143">OUTPUTS</span></span>

### <span data-ttu-id="42f32-144">Microsoft. Azure. Commands. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="42f32-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="42f32-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42f32-145">NOTES</span></span>

## <span data-ttu-id="42f32-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42f32-146">RELATED LINKS</span></span>