---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183338"
---
# <span data-ttu-id="47550-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="47550-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="47550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47550-102">SYNOPSIS</span></span>
<span data-ttu-id="47550-103">Pobiera jedną lub więcej grup docelowych zadań</span><span class="sxs-lookup"><span data-stu-id="47550-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="47550-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="47550-104">SYNTAX</span></span>

### <span data-ttu-id="47550-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="47550-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47550-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="47550-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47550-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="47550-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47550-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="47550-108">DESCRIPTION</span></span>
<span data-ttu-id="47550-109">Polecenie Get-AzSqlElasticJobTargetGroup cmdlet pobiera grupę docelową i jest to wartość docelowa</span><span class="sxs-lookup"><span data-stu-id="47550-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="47550-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="47550-110">EXAMPLES</span></span>

### <span data-ttu-id="47550-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47550-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="47550-112">Pobiera grupę docelową i jest to wartość docelowa</span><span class="sxs-lookup"><span data-stu-id="47550-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="47550-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47550-113">PARAMETERS</span></span>

### <span data-ttu-id="47550-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="47550-114">-AgentName</span></span>
<span data-ttu-id="47550-115">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="47550-115">The agent name</span></span>

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

### <span data-ttu-id="47550-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47550-116">-DefaultProfile</span></span>
<span data-ttu-id="47550-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="47550-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47550-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="47550-118">-Name</span></span>
<span data-ttu-id="47550-119">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="47550-119">The target group name</span></span>

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

### <span data-ttu-id="47550-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="47550-120">-ParentObject</span></span>
<span data-ttu-id="47550-121">Obiekt agenta</span><span class="sxs-lookup"><span data-stu-id="47550-121">The agent object</span></span>

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

### <span data-ttu-id="47550-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="47550-122">-ParentResourceId</span></span>
<span data-ttu-id="47550-123">Identyfikator zasobu agenta</span><span class="sxs-lookup"><span data-stu-id="47550-123">The agent resource id</span></span>

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

### <span data-ttu-id="47550-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47550-124">-ResourceGroupName</span></span>
<span data-ttu-id="47550-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="47550-125">The resource group name</span></span>

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

### <span data-ttu-id="47550-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47550-126">-ServerName</span></span>
<span data-ttu-id="47550-127">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="47550-127">The server name</span></span>

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

### <span data-ttu-id="47550-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47550-128">CommonParameters</span></span>
<span data-ttu-id="47550-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47550-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47550-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47550-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47550-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47550-131">INPUTS</span></span>

### <span data-ttu-id="47550-132">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="47550-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="47550-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47550-133">OUTPUTS</span></span>

### <span data-ttu-id="47550-134">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="47550-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="47550-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="47550-135">NOTES</span></span>

## <span data-ttu-id="47550-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47550-136">RELATED LINKS</span></span>
