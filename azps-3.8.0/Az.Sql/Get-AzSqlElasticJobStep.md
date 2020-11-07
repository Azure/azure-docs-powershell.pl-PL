---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 2b202fd2cff8ae12425c1e41807126798eb9944e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896590"
---
# <span data-ttu-id="de73d-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="de73d-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="de73d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de73d-102">SYNOPSIS</span></span>
<span data-ttu-id="de73d-103">Pobiera co najmniej jeden krok zadania</span><span class="sxs-lookup"><span data-stu-id="de73d-103">Gets one or more job steps</span></span>

## <span data-ttu-id="de73d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de73d-104">SYNTAX</span></span>

### <span data-ttu-id="de73d-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de73d-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de73d-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="de73d-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de73d-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="de73d-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de73d-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="de73d-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de73d-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="de73d-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de73d-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="de73d-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de73d-111">Opis</span><span class="sxs-lookup"><span data-stu-id="de73d-111">DESCRIPTION</span></span>
<span data-ttu-id="de73d-112">Polecenie cmdlet Get-AzSqlElasticJobStep powoduje wykonanie jednego lub kilku kroków zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="de73d-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="de73d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de73d-113">EXAMPLES</span></span>

### <span data-ttu-id="de73d-114">Przykład 1 — pobiera etap zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="de73d-114">Example 1 - Gets a job step from a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="de73d-115">Pobiera etap zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="de73d-115">Gets a job step from a job</span></span>

## <span data-ttu-id="de73d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de73d-116">PARAMETERS</span></span>

### <span data-ttu-id="de73d-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="de73d-117">-AgentName</span></span>
<span data-ttu-id="de73d-118">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="de73d-118">The agent name</span></span>

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

### <span data-ttu-id="de73d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de73d-119">-DefaultProfile</span></span>
<span data-ttu-id="de73d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de73d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de73d-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="de73d-121">-JobName</span></span>
<span data-ttu-id="de73d-122">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="de73d-122">The job name</span></span>

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

### <span data-ttu-id="de73d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de73d-123">-Name</span></span>
<span data-ttu-id="de73d-124">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="de73d-124">The job step name</span></span>

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

### <span data-ttu-id="de73d-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="de73d-125">-ParentObject</span></span>
<span data-ttu-id="de73d-126">Obiekt wejściowy zlecenia</span><span class="sxs-lookup"><span data-stu-id="de73d-126">The job input object</span></span>

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

### <span data-ttu-id="de73d-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="de73d-127">-ParentResourceId</span></span>
<span data-ttu-id="de73d-128">Identyfikator zasobu zadania</span><span class="sxs-lookup"><span data-stu-id="de73d-128">The job resource id</span></span>

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

### <span data-ttu-id="de73d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de73d-129">-ResourceGroupName</span></span>
<span data-ttu-id="de73d-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="de73d-130">The resource group name</span></span>

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

### <span data-ttu-id="de73d-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="de73d-131">-ServerName</span></span>
<span data-ttu-id="de73d-132">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="de73d-132">The server name</span></span>

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

### <span data-ttu-id="de73d-133">-Version</span><span class="sxs-lookup"><span data-stu-id="de73d-133">-Version</span></span>
<span data-ttu-id="de73d-134">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="de73d-134">The job step name</span></span>

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

### <span data-ttu-id="de73d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de73d-135">CommonParameters</span></span>
<span data-ttu-id="de73d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de73d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de73d-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de73d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de73d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de73d-138">INPUTS</span></span>

### <span data-ttu-id="de73d-139">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="de73d-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="de73d-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de73d-140">OUTPUTS</span></span>

### <span data-ttu-id="de73d-141">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="de73d-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="de73d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de73d-142">NOTES</span></span>

## <span data-ttu-id="de73d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de73d-143">RELATED LINKS</span></span>
