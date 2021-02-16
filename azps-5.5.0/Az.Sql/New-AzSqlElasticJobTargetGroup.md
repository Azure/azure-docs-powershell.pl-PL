---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183282"
---
# <span data-ttu-id="349b1-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="349b1-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="349b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="349b1-102">SYNOPSIS</span></span>
<span data-ttu-id="349b1-103">Tworzy nową grupę docelową</span><span class="sxs-lookup"><span data-stu-id="349b1-103">Creates a new target group</span></span>

## <span data-ttu-id="349b1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="349b1-104">SYNTAX</span></span>

### <span data-ttu-id="349b1-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="349b1-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349b1-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="349b1-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349b1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="349b1-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="349b1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="349b1-108">DESCRIPTION</span></span>
<span data-ttu-id="349b1-109">Polecenie New-AzSqlElasticJobTargetGroup cmdlet tworzy nową grupę docelową</span><span class="sxs-lookup"><span data-stu-id="349b1-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="349b1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="349b1-110">EXAMPLES</span></span>

### <span data-ttu-id="349b1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="349b1-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="349b1-112">Tworzy pustą grupę docelową</span><span class="sxs-lookup"><span data-stu-id="349b1-112">Creates an empty target group</span></span>

## <span data-ttu-id="349b1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="349b1-113">PARAMETERS</span></span>

### <span data-ttu-id="349b1-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="349b1-114">-AgentName</span></span>
<span data-ttu-id="349b1-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="349b1-115">The agent name</span></span>

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

### <span data-ttu-id="349b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349b1-116">-DefaultProfile</span></span>
<span data-ttu-id="349b1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="349b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="349b1-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="349b1-118">-Name</span></span>
<span data-ttu-id="349b1-119">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="349b1-119">The target group name</span></span>

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

### <span data-ttu-id="349b1-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="349b1-120">-ParentObject</span></span>
<span data-ttu-id="349b1-121">Obiekt wejściowy agenta</span><span class="sxs-lookup"><span data-stu-id="349b1-121">The agent input object</span></span>

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

### <span data-ttu-id="349b1-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="349b1-122">-ParentResourceId</span></span>
<span data-ttu-id="349b1-123">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="349b1-123">The agent resource id</span></span>

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

### <span data-ttu-id="349b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="349b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="349b1-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="349b1-125">The resource group name</span></span>

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

### <span data-ttu-id="349b1-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="349b1-126">-ServerName</span></span>
<span data-ttu-id="349b1-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="349b1-127">The server name</span></span>

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

### <span data-ttu-id="349b1-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="349b1-128">-Confirm</span></span>
<span data-ttu-id="349b1-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="349b1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="349b1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="349b1-130">-WhatIf</span></span>
<span data-ttu-id="349b1-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="349b1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="349b1-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="349b1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="349b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349b1-133">CommonParameters</span></span>
<span data-ttu-id="349b1-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="349b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349b1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="349b1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349b1-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="349b1-136">INPUTS</span></span>

### <span data-ttu-id="349b1-137">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="349b1-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="349b1-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="349b1-138">OUTPUTS</span></span>

### <span data-ttu-id="349b1-139">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="349b1-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="349b1-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="349b1-140">NOTES</span></span>

## <span data-ttu-id="349b1-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="349b1-141">RELATED LINKS</span></span>
