---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063090"
---
# <span data-ttu-id="81cfd-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="81cfd-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="81cfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="81cfd-103">Aktualizowanie elastycznego agenta zadań</span><span class="sxs-lookup"><span data-stu-id="81cfd-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="81cfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81cfd-104">SYNTAX</span></span>

### <span data-ttu-id="81cfd-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="81cfd-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cfd-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="81cfd-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cfd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="81cfd-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81cfd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="81cfd-108">DESCRIPTION</span></span>
<span data-ttu-id="81cfd-109">Polecenie cmdlet Set-AzSqlElasticJobAgent aktualizuje elastycznych agentów zadań</span><span class="sxs-lookup"><span data-stu-id="81cfd-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="81cfd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81cfd-110">EXAMPLES</span></span>

### <span data-ttu-id="81cfd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81cfd-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="81cfd-112">Aktualizowanie elastycznego agenta zadań</span><span class="sxs-lookup"><span data-stu-id="81cfd-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="81cfd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81cfd-113">PARAMETERS</span></span>

### <span data-ttu-id="81cfd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81cfd-114">-DefaultProfile</span></span>
<span data-ttu-id="81cfd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81cfd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81cfd-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81cfd-116">-InputObject</span></span>
<span data-ttu-id="81cfd-117">Obiekt wejściowy agenta</span><span class="sxs-lookup"><span data-stu-id="81cfd-117">The agent input object</span></span>

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

### <span data-ttu-id="81cfd-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81cfd-118">-Name</span></span>
<span data-ttu-id="81cfd-119">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="81cfd-119">The agent name</span></span>

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

### <span data-ttu-id="81cfd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81cfd-120">-ResourceGroupName</span></span>
<span data-ttu-id="81cfd-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="81cfd-121">The resource group name</span></span>

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

### <span data-ttu-id="81cfd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81cfd-122">-ResourceId</span></span>
<span data-ttu-id="81cfd-123">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="81cfd-123">The agent resource id</span></span>

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

### <span data-ttu-id="81cfd-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="81cfd-124">-ServerName</span></span>
<span data-ttu-id="81cfd-125">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="81cfd-125">The server name</span></span>

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

### <span data-ttu-id="81cfd-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="81cfd-126">-Tag</span></span>
<span data-ttu-id="81cfd-127">Tagi, które mają zostać skojarzone z agentem bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="81cfd-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="81cfd-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81cfd-128">-Confirm</span></span>
<span data-ttu-id="81cfd-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81cfd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81cfd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81cfd-130">-WhatIf</span></span>
<span data-ttu-id="81cfd-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81cfd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81cfd-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81cfd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81cfd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cfd-133">CommonParameters</span></span>
<span data-ttu-id="81cfd-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81cfd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cfd-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81cfd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cfd-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81cfd-136">INPUTS</span></span>

### <span data-ttu-id="81cfd-137">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="81cfd-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="81cfd-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81cfd-138">OUTPUTS</span></span>

### <span data-ttu-id="81cfd-139">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="81cfd-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="81cfd-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81cfd-140">NOTES</span></span>

## <span data-ttu-id="81cfd-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81cfd-141">RELATED LINKS</span></span>
