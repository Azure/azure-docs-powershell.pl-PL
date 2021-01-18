---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498357"
---
# <span data-ttu-id="8dd19-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="8dd19-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="8dd19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8dd19-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd19-103">Tworzy nowego elastycznego agenta zadań.</span><span class="sxs-lookup"><span data-stu-id="8dd19-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="8dd19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8dd19-104">SYNTAX</span></span>

### <span data-ttu-id="8dd19-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8dd19-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dd19-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="8dd19-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dd19-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8dd19-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd19-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8dd19-108">DESCRIPTION</span></span>
<span data-ttu-id="8dd19-109">Polecenie cmdlet New-AzSqlElasticJobAgent tworzy nowego elastycznego agenta zadań</span><span class="sxs-lookup"><span data-stu-id="8dd19-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="8dd19-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8dd19-110">EXAMPLES</span></span>

### <span data-ttu-id="8dd19-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8dd19-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="8dd19-112">Tworzy nowego elastycznego agenta zadań.</span><span class="sxs-lookup"><span data-stu-id="8dd19-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="8dd19-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8dd19-113">PARAMETERS</span></span>

### <span data-ttu-id="8dd19-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8dd19-114">-DatabaseName</span></span>
<span data-ttu-id="8dd19-115">Nazwa bazy danych</span><span class="sxs-lookup"><span data-stu-id="8dd19-115">The database name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd19-116">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="8dd19-116">-DatabaseObject</span></span>
<span data-ttu-id="8dd19-117">Obiekt bazy danych kontroli agenta</span><span class="sxs-lookup"><span data-stu-id="8dd19-117">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd19-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="8dd19-118">-DatabaseResourceId</span></span>
<span data-ttu-id="8dd19-119">Identyfikator zasobu bazy danych kontroli agenta</span><span class="sxs-lookup"><span data-stu-id="8dd19-119">The Agent Control Database Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd19-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd19-120">-DefaultProfile</span></span>
<span data-ttu-id="8dd19-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd19-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dd19-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8dd19-122">-Name</span></span>
<span data-ttu-id="8dd19-123">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="8dd19-123">The Agent Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd19-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd19-124">-ResourceGroupName</span></span>
<span data-ttu-id="8dd19-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8dd19-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd19-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8dd19-126">-ServerName</span></span>
<span data-ttu-id="8dd19-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="8dd19-127">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd19-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="8dd19-128">-Tag</span></span>
<span data-ttu-id="8dd19-129">Tagi agenta</span><span class="sxs-lookup"><span data-stu-id="8dd19-129">The Agent Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd19-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8dd19-130">-Confirm</span></span>
<span data-ttu-id="8dd19-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dd19-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd19-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd19-132">-WhatIf</span></span>
<span data-ttu-id="8dd19-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dd19-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dd19-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8dd19-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd19-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd19-135">CommonParameters</span></span>
<span data-ttu-id="8dd19-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd19-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd19-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dd19-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd19-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dd19-138">INPUTS</span></span>

### <span data-ttu-id="8dd19-139">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8dd19-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8dd19-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8dd19-140">OUTPUTS</span></span>

### <span data-ttu-id="8dd19-141">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="8dd19-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="8dd19-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8dd19-142">NOTES</span></span>

## <span data-ttu-id="8dd19-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8dd19-143">RELATED LINKS</span></span>
