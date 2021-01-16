---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 3a749f02854a915792a12271b2cf59b1091fef70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341221"
---
# <span data-ttu-id="4ae28-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="4ae28-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="4ae28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ae28-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae28-103">Pobiera co najmniej jeden krok zadania</span><span class="sxs-lookup"><span data-stu-id="4ae28-103">Gets one or more job steps</span></span>

## <span data-ttu-id="4ae28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ae28-104">SYNTAX</span></span>

### <span data-ttu-id="4ae28-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4ae28-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ae28-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="4ae28-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ae28-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="4ae28-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ae28-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="4ae28-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ae28-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ae28-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ae28-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4ae28-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ae28-111">Opis</span><span class="sxs-lookup"><span data-stu-id="4ae28-111">DESCRIPTION</span></span>
<span data-ttu-id="4ae28-112">Polecenie cmdlet Get-AzSqlElasticJobStep powoduje wykonanie jednego lub kilku kroków zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="4ae28-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="4ae28-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ae28-113">EXAMPLES</span></span>

### <span data-ttu-id="4ae28-114">Przykład 1: Pobiera etap zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="4ae28-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="4ae28-115">Pobiera etap zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="4ae28-115">Gets a job step from a job</span></span>

## <span data-ttu-id="4ae28-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ae28-116">PARAMETERS</span></span>

### <span data-ttu-id="4ae28-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4ae28-117">-AgentName</span></span>
<span data-ttu-id="4ae28-118">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="4ae28-118">The agent name</span></span>

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

### <span data-ttu-id="4ae28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae28-119">-DefaultProfile</span></span>
<span data-ttu-id="4ae28-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ae28-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ae28-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="4ae28-121">-JobName</span></span>
<span data-ttu-id="4ae28-122">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="4ae28-122">The job name</span></span>

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

### <span data-ttu-id="4ae28-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ae28-123">-Name</span></span>
<span data-ttu-id="4ae28-124">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="4ae28-124">The job step name</span></span>

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

### <span data-ttu-id="4ae28-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="4ae28-125">-ParentObject</span></span>
<span data-ttu-id="4ae28-126">Obiekt wejściowy zlecenia</span><span class="sxs-lookup"><span data-stu-id="4ae28-126">The job input object</span></span>

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

### <span data-ttu-id="4ae28-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4ae28-127">-ParentResourceId</span></span>
<span data-ttu-id="4ae28-128">Identyfikator zasobu zadania</span><span class="sxs-lookup"><span data-stu-id="4ae28-128">The job resource id</span></span>

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

### <span data-ttu-id="4ae28-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae28-129">-ResourceGroupName</span></span>
<span data-ttu-id="4ae28-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4ae28-130">The resource group name</span></span>

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

### <span data-ttu-id="4ae28-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4ae28-131">-ServerName</span></span>
<span data-ttu-id="4ae28-132">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="4ae28-132">The server name</span></span>

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

### <span data-ttu-id="4ae28-133">-Version</span><span class="sxs-lookup"><span data-stu-id="4ae28-133">-Version</span></span>
<span data-ttu-id="4ae28-134">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="4ae28-134">The job step name</span></span>

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

### <span data-ttu-id="4ae28-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae28-135">CommonParameters</span></span>
<span data-ttu-id="4ae28-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae28-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae28-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ae28-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae28-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ae28-138">INPUTS</span></span>

### <span data-ttu-id="4ae28-139">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="4ae28-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="4ae28-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ae28-140">OUTPUTS</span></span>

### <span data-ttu-id="4ae28-141">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="4ae28-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="4ae28-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ae28-142">NOTES</span></span>

## <span data-ttu-id="4ae28-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ae28-143">RELATED LINKS</span></span>
