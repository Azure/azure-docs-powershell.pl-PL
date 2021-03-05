---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 9a80504f1b3aff814d50b5b4aba98b488d1e55b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970218"
---
# <span data-ttu-id="4c02a-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="4c02a-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="4c02a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c02a-102">SYNOPSIS</span></span>
<span data-ttu-id="4c02a-103">Tworzy nową grupę docelową</span><span class="sxs-lookup"><span data-stu-id="4c02a-103">Creates a new target group</span></span>

## <span data-ttu-id="4c02a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4c02a-104">SYNTAX</span></span>

### <span data-ttu-id="4c02a-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="4c02a-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c02a-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4c02a-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c02a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4c02a-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c02a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4c02a-108">DESCRIPTION</span></span>
<span data-ttu-id="4c02a-109">Polecenie New-AzSqlElasticJobTargetGroup cmdlet tworzy nową grupę docelową</span><span class="sxs-lookup"><span data-stu-id="4c02a-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="4c02a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4c02a-110">EXAMPLES</span></span>

### <span data-ttu-id="4c02a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4c02a-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="4c02a-112">Tworzy pustą grupę docelową</span><span class="sxs-lookup"><span data-stu-id="4c02a-112">Creates an empty target group</span></span>

## <span data-ttu-id="4c02a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c02a-113">PARAMETERS</span></span>

### <span data-ttu-id="4c02a-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4c02a-114">-AgentName</span></span>
<span data-ttu-id="4c02a-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="4c02a-115">The agent name</span></span>

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

### <span data-ttu-id="4c02a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c02a-116">-DefaultProfile</span></span>
<span data-ttu-id="4c02a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c02a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c02a-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4c02a-118">-Name</span></span>
<span data-ttu-id="4c02a-119">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="4c02a-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c02a-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="4c02a-120">-ParentObject</span></span>
<span data-ttu-id="4c02a-121">Obiekt wejściowy agenta</span><span class="sxs-lookup"><span data-stu-id="4c02a-121">The agent input object</span></span>

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

### <span data-ttu-id="4c02a-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4c02a-122">-ParentResourceId</span></span>
<span data-ttu-id="4c02a-123">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="4c02a-123">The agent resource id</span></span>

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

### <span data-ttu-id="4c02a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c02a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c02a-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4c02a-125">The resource group name</span></span>

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

### <span data-ttu-id="4c02a-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4c02a-126">-ServerName</span></span>
<span data-ttu-id="4c02a-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="4c02a-127">The server name</span></span>

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

### <span data-ttu-id="4c02a-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c02a-128">-Confirm</span></span>
<span data-ttu-id="4c02a-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4c02a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c02a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c02a-130">-WhatIf</span></span>
<span data-ttu-id="4c02a-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c02a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c02a-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4c02a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c02a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c02a-133">CommonParameters</span></span>
<span data-ttu-id="4c02a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c02a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c02a-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c02a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c02a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c02a-136">INPUTS</span></span>

### <span data-ttu-id="4c02a-137">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="4c02a-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="4c02a-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c02a-138">OUTPUTS</span></span>

### <span data-ttu-id="4c02a-139">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="4c02a-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="4c02a-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4c02a-140">NOTES</span></span>

## <span data-ttu-id="4c02a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c02a-141">RELATED LINKS</span></span>
