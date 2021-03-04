---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: ca23ba63e2f92fa14c97957a2b21b38d91e453ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982017"
---
# <span data-ttu-id="7033b-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="7033b-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="7033b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7033b-102">SYNOPSIS</span></span>
<span data-ttu-id="7033b-103">Tworzy nowego elastycznego agenta stanowisk</span><span class="sxs-lookup"><span data-stu-id="7033b-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="7033b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7033b-104">SYNTAX</span></span>

### <span data-ttu-id="7033b-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="7033b-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7033b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7033b-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7033b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7033b-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7033b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7033b-108">DESCRIPTION</span></span>
<span data-ttu-id="7033b-109">Polecenie New-AzSqlElasticJobAgent cmdlet tworzy nowego elastycznego agenta zadania</span><span class="sxs-lookup"><span data-stu-id="7033b-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="7033b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7033b-110">EXAMPLES</span></span>

### <span data-ttu-id="7033b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7033b-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="7033b-112">Tworzy nowego elastycznego agenta zadań</span><span class="sxs-lookup"><span data-stu-id="7033b-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="7033b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7033b-113">PARAMETERS</span></span>

### <span data-ttu-id="7033b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7033b-114">-DatabaseName</span></span>
<span data-ttu-id="7033b-115">Nazwa bazy danych</span><span class="sxs-lookup"><span data-stu-id="7033b-115">The database name</span></span>

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

### <span data-ttu-id="7033b-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7033b-116">-DatabaseObject</span></span>
<span data-ttu-id="7033b-117">Obiekt bazy danych kontrolki agenta</span><span class="sxs-lookup"><span data-stu-id="7033b-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="7033b-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="7033b-118">-DatabaseResourceId</span></span>
<span data-ttu-id="7033b-119">Identyfikator zasobu bazy danych kontrolki agenta</span><span class="sxs-lookup"><span data-stu-id="7033b-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="7033b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7033b-120">-DefaultProfile</span></span>
<span data-ttu-id="7033b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7033b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7033b-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7033b-122">-Name</span></span>
<span data-ttu-id="7033b-123">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="7033b-123">The Agent Name</span></span>

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

### <span data-ttu-id="7033b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7033b-124">-ResourceGroupName</span></span>
<span data-ttu-id="7033b-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7033b-125">The resource group name</span></span>

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

### <span data-ttu-id="7033b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7033b-126">-ServerName</span></span>
<span data-ttu-id="7033b-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="7033b-127">The server name</span></span>

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

### <span data-ttu-id="7033b-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="7033b-128">-Tag</span></span>
<span data-ttu-id="7033b-129">Tagi agenta</span><span class="sxs-lookup"><span data-stu-id="7033b-129">The Agent Tags</span></span>

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

### <span data-ttu-id="7033b-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7033b-130">-Confirm</span></span>
<span data-ttu-id="7033b-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7033b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7033b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7033b-132">-WhatIf</span></span>
<span data-ttu-id="7033b-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7033b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7033b-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7033b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7033b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7033b-135">CommonParameters</span></span>
<span data-ttu-id="7033b-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7033b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7033b-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7033b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7033b-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7033b-138">INPUTS</span></span>

### <span data-ttu-id="7033b-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7033b-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="7033b-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7033b-140">OUTPUTS</span></span>

### <span data-ttu-id="7033b-141">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="7033b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="7033b-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7033b-142">NOTES</span></span>

## <span data-ttu-id="7033b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7033b-143">RELATED LINKS</span></span>
