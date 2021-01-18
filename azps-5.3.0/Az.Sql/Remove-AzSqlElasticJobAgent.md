---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498277"
---
# <span data-ttu-id="2b2c8-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="2b2c8-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="2b2c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b2c8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b2c8-103">Usuwa elastycznego agenta zadań.</span><span class="sxs-lookup"><span data-stu-id="2b2c8-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="2b2c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b2c8-104">SYNTAX</span></span>

### <span data-ttu-id="2b2c8-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2b2c8-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b2c8-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="2b2c8-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b2c8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2b2c8-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b2c8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2b2c8-108">DESCRIPTION</span></span>
<span data-ttu-id="2b2c8-109">Polecenie cmdlet Remove-AzSqlElasticJobAgent usuwa elastyczny Agent zadań</span><span class="sxs-lookup"><span data-stu-id="2b2c8-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="2b2c8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b2c8-110">EXAMPLES</span></span>

### <span data-ttu-id="2b2c8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2b2c8-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="2b2c8-112">Usuwa elastycznego agenta zadań.</span><span class="sxs-lookup"><span data-stu-id="2b2c8-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="2b2c8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b2c8-113">PARAMETERS</span></span>

### <span data-ttu-id="2b2c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b2c8-114">-DefaultProfile</span></span>
<span data-ttu-id="2b2c8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b2c8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b2c8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2b2c8-116">-Force</span></span>
<span data-ttu-id="2b2c8-117">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="2b2c8-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b2c8-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2b2c8-118">-InputObject</span></span>
<span data-ttu-id="2b2c8-119">Obiekt Agent</span><span class="sxs-lookup"><span data-stu-id="2b2c8-119">The agent object</span></span>

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

### <span data-ttu-id="2b2c8-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b2c8-120">-Name</span></span>
<span data-ttu-id="2b2c8-121">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="2b2c8-121">The agent name</span></span>

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

### <span data-ttu-id="2b2c8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b2c8-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b2c8-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2b2c8-123">The resource group name</span></span>

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

### <span data-ttu-id="2b2c8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b2c8-124">-ResourceId</span></span>
<span data-ttu-id="2b2c8-125">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="2b2c8-125">The agent resource id</span></span>

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

### <span data-ttu-id="2b2c8-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2b2c8-126">-ServerName</span></span>
<span data-ttu-id="2b2c8-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="2b2c8-127">The server name</span></span>

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

### <span data-ttu-id="2b2c8-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b2c8-128">-Confirm</span></span>
<span data-ttu-id="2b2c8-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b2c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b2c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b2c8-130">-WhatIf</span></span>
<span data-ttu-id="2b2c8-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b2c8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b2c8-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b2c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b2c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b2c8-133">CommonParameters</span></span>
<span data-ttu-id="2b2c8-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b2c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b2c8-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b2c8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b2c8-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b2c8-136">INPUTS</span></span>

### <span data-ttu-id="2b2c8-137">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2b2c8-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2b2c8-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b2c8-138">OUTPUTS</span></span>

### <span data-ttu-id="2b2c8-139">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2b2c8-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2b2c8-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b2c8-140">NOTES</span></span>

## <span data-ttu-id="2b2c8-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b2c8-141">RELATED LINKS</span></span>
