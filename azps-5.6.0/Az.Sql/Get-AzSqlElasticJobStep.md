---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: d70a0b6abd31d4104301e877fb21bf1d0589a24f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999658"
---
# <span data-ttu-id="e1932-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="e1932-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="e1932-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1932-102">SYNOPSIS</span></span>
<span data-ttu-id="e1932-103">Otrzymuje co najmniej jeden krok w zadaniu</span><span class="sxs-lookup"><span data-stu-id="e1932-103">Gets one or more job steps</span></span>

## <span data-ttu-id="e1932-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1932-104">SYNTAX</span></span>

### <span data-ttu-id="e1932-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="e1932-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1932-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="e1932-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1932-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e1932-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1932-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="e1932-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1932-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e1932-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1932-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e1932-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1932-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1932-111">DESCRIPTION</span></span>
<span data-ttu-id="e1932-112">Polecenie Get-AzSqlElasticJobStep cmdlet pobiera jeden lub więcej kroków zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="e1932-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="e1932-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1932-113">EXAMPLES</span></span>

### <span data-ttu-id="e1932-114">Przykład 1. Pobiera z zadania etap zadania</span><span class="sxs-lookup"><span data-stu-id="e1932-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="e1932-115">Otrzymuje od zadania etap pracy</span><span class="sxs-lookup"><span data-stu-id="e1932-115">Gets a job step from a job</span></span>

## <span data-ttu-id="e1932-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1932-116">PARAMETERS</span></span>

### <span data-ttu-id="e1932-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e1932-117">-AgentName</span></span>
<span data-ttu-id="e1932-118">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="e1932-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1932-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1932-119">-DefaultProfile</span></span>
<span data-ttu-id="e1932-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1932-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1932-121">— JobName</span><span class="sxs-lookup"><span data-stu-id="e1932-121">-JobName</span></span>
<span data-ttu-id="e1932-122">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="e1932-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1932-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e1932-123">-Name</span></span>
<span data-ttu-id="e1932-124">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="e1932-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1932-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="e1932-125">-ParentObject</span></span>
<span data-ttu-id="e1932-126">Obiekt wprowadzania zadania</span><span class="sxs-lookup"><span data-stu-id="e1932-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1932-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e1932-127">-ParentResourceId</span></span>
<span data-ttu-id="e1932-128">Identyfikator zasobu zadań</span><span class="sxs-lookup"><span data-stu-id="e1932-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1932-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1932-129">-ResourceGroupName</span></span>
<span data-ttu-id="e1932-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e1932-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1932-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e1932-131">-ServerName</span></span>
<span data-ttu-id="e1932-132">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="e1932-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1932-133">— Wersja</span><span class="sxs-lookup"><span data-stu-id="e1932-133">-Version</span></span>
<span data-ttu-id="e1932-134">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="e1932-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1932-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1932-135">CommonParameters</span></span>
<span data-ttu-id="e1932-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1932-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1932-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1932-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1932-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1932-138">INPUTS</span></span>

### <span data-ttu-id="e1932-139">Microsoft.Azure.Commands.Sql.ElastycznaJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="e1932-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="e1932-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1932-140">OUTPUTS</span></span>

### <span data-ttu-id="e1932-141">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="e1932-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="e1932-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1932-142">NOTES</span></span>

## <span data-ttu-id="e1932-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1932-143">RELATED LINKS</span></span>
