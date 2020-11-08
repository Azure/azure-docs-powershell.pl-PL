---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 25c9845d0912374baa0e2219c234f63abe381cfc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050240"
---
# <span data-ttu-id="ad664-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="ad664-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="ad664-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad664-102">SYNOPSIS</span></span>
<span data-ttu-id="ad664-103">Dodanie kroku zadania do zadania</span><span class="sxs-lookup"><span data-stu-id="ad664-103">Adds a job step to a job</span></span>

## <span data-ttu-id="ad664-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad664-104">SYNTAX</span></span>

### <span data-ttu-id="ad664-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ad664-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad664-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="ad664-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad664-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="ad664-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad664-108">Obiekt</span><span class="sxs-lookup"><span data-stu-id="ad664-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad664-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ad664-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad664-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ad664-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad664-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ad664-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad664-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ad664-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad664-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ad664-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad664-114">Opis</span><span class="sxs-lookup"><span data-stu-id="ad664-114">DESCRIPTION</span></span>
<span data-ttu-id="ad664-115">Polecenie cmdlet Add-AzSqlElasticJobStep dodaje krok zadania do zadania</span><span class="sxs-lookup"><span data-stu-id="ad664-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="ad664-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad664-116">EXAMPLES</span></span>

### <span data-ttu-id="ad664-117">Przykład 1-dodanie kroku do zadania</span><span class="sxs-lookup"><span data-stu-id="ad664-117">Example 1 - Adds a step to a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="ad664-118">Dodanie kroku zadania do zadania</span><span class="sxs-lookup"><span data-stu-id="ad664-118">Adds a job step to a job</span></span>

## <span data-ttu-id="ad664-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad664-119">PARAMETERS</span></span>

### <span data-ttu-id="ad664-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ad664-120">-AgentName</span></span>
<span data-ttu-id="ad664-121">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="ad664-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="ad664-122">-CommandText</span></span>
<span data-ttu-id="ad664-123">Tekst polecenia</span><span class="sxs-lookup"><span data-stu-id="ad664-123">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ad664-124">-CredentialName</span></span>
<span data-ttu-id="ad664-125">Nazwa poświadczenia</span><span class="sxs-lookup"><span data-stu-id="ad664-125">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad664-126">-DefaultProfile</span></span>
<span data-ttu-id="ad664-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad664-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad664-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ad664-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="ad664-129">Początkowy interwał ponawiania prób w sekundach</span><span class="sxs-lookup"><span data-stu-id="ad664-129">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="ad664-130">-JobName</span></span>
<span data-ttu-id="ad664-131">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="ad664-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ad664-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="ad664-133">Maksymalny interwał ponawiania prób w sekundach</span><span class="sxs-lookup"><span data-stu-id="ad664-133">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad664-134">-Name</span></span>
<span data-ttu-id="ad664-135">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="ad664-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="ad664-136">-OutputCredentialName</span></span>
<span data-ttu-id="ad664-137">Nazwa poświadczenia danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="ad664-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ad664-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="ad664-139">Wyjściowy obiekt bazy danych</span><span class="sxs-lookup"><span data-stu-id="ad664-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="ad664-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="ad664-141">Identyfikator zasobu bazy danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="ad664-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="ad664-142">-OutputSchemaName</span></span>
<span data-ttu-id="ad664-143">Nazwa schematu wyjściowego</span><span class="sxs-lookup"><span data-stu-id="ad664-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="ad664-144">-OutputTableName</span></span>
<span data-ttu-id="ad664-145">Nazwa tabeli wyjściowej</span><span class="sxs-lookup"><span data-stu-id="ad664-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-146">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="ad664-146">-ParentObject</span></span>
<span data-ttu-id="ad664-147">Obiekt zadania</span><span class="sxs-lookup"><span data-stu-id="ad664-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ad664-148">-ParentResourceId</span></span>
<span data-ttu-id="ad664-149">Identyfikator zasobu zadania</span><span class="sxs-lookup"><span data-stu-id="ad664-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad664-150">-ResourceGroupName</span></span>
<span data-ttu-id="ad664-151">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ad664-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="ad664-152">-RetryAttempts</span></span>
<span data-ttu-id="ad664-153">Ponowna próba</span><span class="sxs-lookup"><span data-stu-id="ad664-153">The retry attempts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="ad664-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="ad664-155">Mnożnik cofania interwału ponawiania</span><span class="sxs-lookup"><span data-stu-id="ad664-155">The retry interval back off multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-156">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ad664-156">-ServerName</span></span>
<span data-ttu-id="ad664-157">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="ad664-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="ad664-158">-StepId</span></span>
<span data-ttu-id="ad664-159">Identyfikator kroku</span><span class="sxs-lookup"><span data-stu-id="ad664-159">The step id</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="ad664-160">-TargetGroupName</span></span>
<span data-ttu-id="ad664-161">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="ad664-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="ad664-162">-TimeoutSeconds</span></span>
<span data-ttu-id="ad664-163">Limit czasu w sekundach</span><span class="sxs-lookup"><span data-stu-id="ad664-163">The time out seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad664-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad664-164">-Confirm</span></span>
<span data-ttu-id="ad664-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad664-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad664-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad664-166">-WhatIf</span></span>
<span data-ttu-id="ad664-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad664-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad664-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad664-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad664-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad664-169">CommonParameters</span></span>
<span data-ttu-id="ad664-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad664-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad664-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad664-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad664-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad664-172">INPUTS</span></span>

### <span data-ttu-id="ad664-173">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="ad664-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="ad664-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad664-174">OUTPUTS</span></span>

### <span data-ttu-id="ad664-175">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="ad664-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="ad664-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad664-176">NOTES</span></span>

## <span data-ttu-id="ad664-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad664-177">RELATED LINKS</span></span>
