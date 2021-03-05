---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: c65c7a74d4b2edfcddf8b4e08ee3e538c32d31df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986350"
---
# <span data-ttu-id="b3e85-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="b3e85-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="b3e85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e85-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e85-103">Aktualizuje elastycznego agenta zadań</span><span class="sxs-lookup"><span data-stu-id="b3e85-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="b3e85-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b3e85-104">SYNTAX</span></span>

### <span data-ttu-id="b3e85-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="b3e85-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e85-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b3e85-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e85-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b3e85-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e85-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b3e85-108">DESCRIPTION</span></span>
<span data-ttu-id="b3e85-109">Polecenie Set-AzSqlElasticJobAgent cmdlet aktualizuje elastyczną agentów zadań</span><span class="sxs-lookup"><span data-stu-id="b3e85-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="b3e85-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b3e85-110">EXAMPLES</span></span>

### <span data-ttu-id="b3e85-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3e85-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="b3e85-112">Aktualizuje elastycznego agenta zadań</span><span class="sxs-lookup"><span data-stu-id="b3e85-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="b3e85-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3e85-113">PARAMETERS</span></span>

### <span data-ttu-id="b3e85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e85-114">-DefaultProfile</span></span>
<span data-ttu-id="b3e85-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e85-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3e85-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3e85-116">-InputObject</span></span>
<span data-ttu-id="b3e85-117">Obiekt wejściowy agenta</span><span class="sxs-lookup"><span data-stu-id="b3e85-117">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e85-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b3e85-118">-Name</span></span>
<span data-ttu-id="b3e85-119">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="b3e85-119">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e85-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e85-120">-ResourceGroupName</span></span>
<span data-ttu-id="b3e85-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b3e85-121">The resource group name</span></span>

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

### <span data-ttu-id="b3e85-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3e85-122">-ResourceId</span></span>
<span data-ttu-id="b3e85-123">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="b3e85-123">The agent resource id</span></span>

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

### <span data-ttu-id="b3e85-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3e85-124">-ServerName</span></span>
<span data-ttu-id="b3e85-125">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="b3e85-125">The server name</span></span>

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

### <span data-ttu-id="b3e85-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="b3e85-126">-Tag</span></span>
<span data-ttu-id="b3e85-127">Tagi do skojarzenia z agentem bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="b3e85-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="b3e85-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3e85-128">-Confirm</span></span>
<span data-ttu-id="b3e85-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b3e85-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e85-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e85-130">-WhatIf</span></span>
<span data-ttu-id="b3e85-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3e85-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e85-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b3e85-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e85-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e85-133">CommonParameters</span></span>
<span data-ttu-id="b3e85-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e85-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e85-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3e85-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e85-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3e85-136">INPUTS</span></span>

### <span data-ttu-id="b3e85-137">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="b3e85-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b3e85-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3e85-138">OUTPUTS</span></span>

### <span data-ttu-id="b3e85-139">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="b3e85-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b3e85-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b3e85-140">NOTES</span></span>

## <span data-ttu-id="b3e85-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3e85-141">RELATED LINKS</span></span>
