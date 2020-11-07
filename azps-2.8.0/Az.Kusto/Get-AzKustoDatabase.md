---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 98936051ba3faa06d611fc8509faaa2b26998d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705075"
---
# <span data-ttu-id="d2c8d-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="d2c8d-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="d2c8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c8d-103">Wyświetlanie wszystkich Kustoych baz danych w klastrze lub uzyskiwanie określonej bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="d2c8d-103">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="d2c8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2c8d-104">SYNTAX</span></span>

### <span data-ttu-id="d2c8d-105">ByClusterOrResourceGroupOrSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d2c8d-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c8d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2c8d-106">ByResourceId</span></span>
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2c8d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d2c8d-107">ByInputObject</span></span>
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2c8d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d2c8d-108">DESCRIPTION</span></span>
<span data-ttu-id="d2c8d-109">Wyświetlanie wszystkich Kustoych baz danych w klastrze lub uzyskiwanie określonej bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="d2c8d-109">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="d2c8d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2c8d-110">EXAMPLES</span></span>

### <span data-ttu-id="d2c8d-111">Przykład 1-Wyświetlanie wszystkich Kusto baz danych w klastrze według nazwy</span><span class="sxs-lookup"><span data-stu-id="d2c8d-111">Example 1 - List all Kusto databases in a cluster by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="d2c8d-112">Powyższe polecenie zwraca wszystkie bazy danych Kusto w klastrze "mykustocluster", które znajdują się w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="d2c8d-112">The above command returns all Kusto databases in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="d2c8d-113">Przykład 2 — Wyświetlanie wszystkich baz danych Kusto w klastrze za pomocą połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="d2c8d-113">Example 2 - List all Kusto databases in a cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="d2c8d-114">Powyższe polecenie otrzyma klaster Kusto o nazwie "mykustocluster" znajdujący się w grupie zasobów "testrg" przy użyciu `Get-AzKustoCluster` polecenia cmdlet, a następnie przełączenie wyniku do `Get-AzKustoDatabase` polecenia cmdlet na listę wszystkich baz danych w tym klastrze.</span><span class="sxs-lookup"><span data-stu-id="d2c8d-114">The above command will get the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and pipe the result to the `Get-AzKustoDatabase` cmdlet to list all databases in that cluster.</span></span>

### <span data-ttu-id="d2c8d-115">Przykład 3 — Uzyskaj określoną bazę danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="d2c8d-115">Example 3 - Get a specific Kusto database by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="d2c8d-116">Powyższe polecenie zwraca bazę danych Kusto o nazwie "mykustodatabase" w klastrze "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="d2c8d-116">The above command returns the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="d2c8d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2c8d-117">PARAMETERS</span></span>

### <span data-ttu-id="d2c8d-118">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d2c8d-118">-ClusterName</span></span>
<span data-ttu-id="d2c8d-119">Nazwa klastra, pod którym istnieje baza danych.</span><span class="sxs-lookup"><span data-stu-id="d2c8d-119">Name of cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2c8d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c8d-120">-DefaultProfile</span></span>
<span data-ttu-id="d2c8d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c8d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2c8d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d2c8d-122">-InputObject</span></span>
<span data-ttu-id="d2c8d-123">Obiekt klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="d2c8d-123">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c8d-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2c8d-124">-Name</span></span>
<span data-ttu-id="d2c8d-125">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d2c8d-125">the name of the database.</span></span>

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

### <span data-ttu-id="d2c8d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c8d-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2c8d-127">Nazwa grupy zasobów, pod którą użytkownik chce pobrać klaster.</span><span class="sxs-lookup"><span data-stu-id="d2c8d-127">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2c8d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2c8d-128">-ResourceId</span></span>
<span data-ttu-id="d2c8d-129">Kusto identyfikator zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="d2c8d-129">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c8d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c8d-130">CommonParameters</span></span>
<span data-ttu-id="d2c8d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c8d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c8d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c8d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c8d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2c8d-133">INPUTS</span></span>

### <span data-ttu-id="d2c8d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d2c8d-134">System.String</span></span>

### <span data-ttu-id="d2c8d-135">Microsoft. Azure. Commands. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d2c8d-135">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="d2c8d-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2c8d-136">OUTPUTS</span></span>

### <span data-ttu-id="d2c8d-137">Microsoft. Azure. Commands. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="d2c8d-137">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="d2c8d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2c8d-138">NOTES</span></span>

## <span data-ttu-id="d2c8d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2c8d-139">RELATED LINKS</span></span>