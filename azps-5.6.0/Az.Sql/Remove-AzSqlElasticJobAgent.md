---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 3c6a92a205aef19b1e4cef4842de4cf0414c2397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957889"
---
# <span data-ttu-id="3854e-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="3854e-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="3854e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3854e-102">SYNOPSIS</span></span>
<span data-ttu-id="3854e-103">Usuwa elastycznego agenta zadań</span><span class="sxs-lookup"><span data-stu-id="3854e-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="3854e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3854e-104">SYNTAX</span></span>

### <span data-ttu-id="3854e-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="3854e-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3854e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3854e-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3854e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3854e-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3854e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3854e-108">DESCRIPTION</span></span>
<span data-ttu-id="3854e-109">Polecenie Remove-AzSqlElasticJobAgent usuwa elastycznego agenta zadania</span><span class="sxs-lookup"><span data-stu-id="3854e-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="3854e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3854e-110">EXAMPLES</span></span>

### <span data-ttu-id="3854e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3854e-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="3854e-112">Usuwa elastycznego agenta zadań</span><span class="sxs-lookup"><span data-stu-id="3854e-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="3854e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3854e-113">PARAMETERS</span></span>

### <span data-ttu-id="3854e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3854e-114">-DefaultProfile</span></span>
<span data-ttu-id="3854e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3854e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3854e-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3854e-116">-Force</span></span>
<span data-ttu-id="3854e-117">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="3854e-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3854e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3854e-118">-InputObject</span></span>
<span data-ttu-id="3854e-119">Obiekt agenta</span><span class="sxs-lookup"><span data-stu-id="3854e-119">The agent object</span></span>

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

### <span data-ttu-id="3854e-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3854e-120">-Name</span></span>
<span data-ttu-id="3854e-121">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="3854e-121">The agent name</span></span>

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

### <span data-ttu-id="3854e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3854e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3854e-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3854e-123">The resource group name</span></span>

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

### <span data-ttu-id="3854e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3854e-124">-ResourceId</span></span>
<span data-ttu-id="3854e-125">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="3854e-125">The agent resource id</span></span>

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

### <span data-ttu-id="3854e-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3854e-126">-ServerName</span></span>
<span data-ttu-id="3854e-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="3854e-127">The server name</span></span>

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

### <span data-ttu-id="3854e-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3854e-128">-Confirm</span></span>
<span data-ttu-id="3854e-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3854e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3854e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3854e-130">-WhatIf</span></span>
<span data-ttu-id="3854e-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3854e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3854e-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3854e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3854e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3854e-133">CommonParameters</span></span>
<span data-ttu-id="3854e-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3854e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3854e-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3854e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3854e-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3854e-136">INPUTS</span></span>

### <span data-ttu-id="3854e-137">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="3854e-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3854e-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3854e-138">OUTPUTS</span></span>

### <span data-ttu-id="3854e-139">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="3854e-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3854e-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3854e-140">NOTES</span></span>

## <span data-ttu-id="3854e-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3854e-141">RELATED LINKS</span></span>
