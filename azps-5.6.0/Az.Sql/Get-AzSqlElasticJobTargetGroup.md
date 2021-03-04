---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 022ef6979ddac4fa31c0a1dae42ae04c044498dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999617"
---
# <span data-ttu-id="e59ae-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="e59ae-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="e59ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e59ae-102">SYNOPSIS</span></span>
<span data-ttu-id="e59ae-103">Pobiera jedną lub więcej grup docelowych zadań</span><span class="sxs-lookup"><span data-stu-id="e59ae-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="e59ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e59ae-104">SYNTAX</span></span>

### <span data-ttu-id="e59ae-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="e59ae-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e59ae-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e59ae-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e59ae-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e59ae-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e59ae-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e59ae-108">DESCRIPTION</span></span>
<span data-ttu-id="e59ae-109">Polecenie Get-AzSqlElasticJobTargetGroup cmdlet pobiera grupę docelową i jest to wartość docelowa</span><span class="sxs-lookup"><span data-stu-id="e59ae-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="e59ae-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e59ae-110">EXAMPLES</span></span>

### <span data-ttu-id="e59ae-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e59ae-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="e59ae-112">Pobiera grupę docelową i jest to wartość docelowa</span><span class="sxs-lookup"><span data-stu-id="e59ae-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="e59ae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e59ae-113">PARAMETERS</span></span>

### <span data-ttu-id="e59ae-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e59ae-114">-AgentName</span></span>
<span data-ttu-id="e59ae-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="e59ae-115">The agent name</span></span>

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

### <span data-ttu-id="e59ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59ae-116">-DefaultProfile</span></span>
<span data-ttu-id="e59ae-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e59ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e59ae-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e59ae-118">-Name</span></span>
<span data-ttu-id="e59ae-119">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="e59ae-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e59ae-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="e59ae-120">-ParentObject</span></span>
<span data-ttu-id="e59ae-121">Obiekt agenta</span><span class="sxs-lookup"><span data-stu-id="e59ae-121">The agent object</span></span>

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

### <span data-ttu-id="e59ae-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e59ae-122">-ParentResourceId</span></span>
<span data-ttu-id="e59ae-123">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="e59ae-123">The agent resource id</span></span>

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

### <span data-ttu-id="e59ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e59ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="e59ae-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e59ae-125">The resource group name</span></span>

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

### <span data-ttu-id="e59ae-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e59ae-126">-ServerName</span></span>
<span data-ttu-id="e59ae-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="e59ae-127">The server name</span></span>

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

### <span data-ttu-id="e59ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59ae-128">CommonParameters</span></span>
<span data-ttu-id="e59ae-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e59ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59ae-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e59ae-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59ae-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e59ae-131">INPUTS</span></span>

### <span data-ttu-id="e59ae-132">Microsoft.Azure.Commands.sql.Jego elastycznaobs.model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="e59ae-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e59ae-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e59ae-133">OUTPUTS</span></span>

### <span data-ttu-id="e59ae-134">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="e59ae-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="e59ae-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e59ae-135">NOTES</span></span>

## <span data-ttu-id="e59ae-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e59ae-136">RELATED LINKS</span></span>
