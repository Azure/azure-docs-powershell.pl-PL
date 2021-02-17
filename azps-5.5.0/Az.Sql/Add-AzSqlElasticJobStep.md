---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: dbc27ec87be3de4c320ad60b7dc204d704fe8f2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198587"
---
# <span data-ttu-id="04b7d-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="04b7d-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="04b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="04b7d-103">Dodaje krok zadania do zadania</span><span class="sxs-lookup"><span data-stu-id="04b7d-103">Adds a job step to a job</span></span>

## <span data-ttu-id="04b7d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04b7d-104">SYNTAX</span></span>

### <span data-ttu-id="04b7d-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="04b7d-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b7d-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="04b7d-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04b7d-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="04b7d-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04b7d-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="04b7d-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04b7d-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="04b7d-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b7d-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="04b7d-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b7d-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="04b7d-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04b7d-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="04b7d-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04b7d-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="04b7d-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04b7d-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="04b7d-114">DESCRIPTION</span></span>
<span data-ttu-id="04b7d-115">Polecenie Add-AzSqlElasticJobStep cmdlet dodaje krok zadania do zadania</span><span class="sxs-lookup"><span data-stu-id="04b7d-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="04b7d-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04b7d-116">EXAMPLES</span></span>

### <span data-ttu-id="04b7d-117">Przykład 1. Dodanie kroku do zadania</span><span class="sxs-lookup"><span data-stu-id="04b7d-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="04b7d-118">Dodaje krok zadania do zadania</span><span class="sxs-lookup"><span data-stu-id="04b7d-118">Adds a job step to a job</span></span>

## <span data-ttu-id="04b7d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04b7d-119">PARAMETERS</span></span>

### <span data-ttu-id="04b7d-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="04b7d-120">-AgentName</span></span>
<span data-ttu-id="04b7d-121">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="04b7d-121">The agent name</span></span>

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

### <span data-ttu-id="04b7d-122">- CommandText</span><span class="sxs-lookup"><span data-stu-id="04b7d-122">-CommandText</span></span>
<span data-ttu-id="04b7d-123">Tekst polecenia</span><span class="sxs-lookup"><span data-stu-id="04b7d-123">The command text</span></span>

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

### <span data-ttu-id="04b7d-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="04b7d-124">-CredentialName</span></span>
<span data-ttu-id="04b7d-125">Nazwa poświadczeń</span><span class="sxs-lookup"><span data-stu-id="04b7d-125">The credential name</span></span>

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

### <span data-ttu-id="04b7d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b7d-126">-DefaultProfile</span></span>
<span data-ttu-id="04b7d-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="04b7d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04b7d-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="04b7d-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="04b7d-129">Początkowa ponowna próba interwału (sekundy)</span><span class="sxs-lookup"><span data-stu-id="04b7d-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="04b7d-130">— JobName</span><span class="sxs-lookup"><span data-stu-id="04b7d-130">-JobName</span></span>
<span data-ttu-id="04b7d-131">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="04b7d-131">The job name</span></span>

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

### <span data-ttu-id="04b7d-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="04b7d-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="04b7d-133">Maksymalna liczba ponownych prób w sekundach</span><span class="sxs-lookup"><span data-stu-id="04b7d-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="04b7d-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="04b7d-134">-Name</span></span>
<span data-ttu-id="04b7d-135">Nazwa etapu zadania</span><span class="sxs-lookup"><span data-stu-id="04b7d-135">The job step name</span></span>

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

### <span data-ttu-id="04b7d-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="04b7d-136">-OutputCredentialName</span></span>
<span data-ttu-id="04b7d-137">Nazwa poświadczeń wyjściowych</span><span class="sxs-lookup"><span data-stu-id="04b7d-137">The output credential name</span></span>

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

### <span data-ttu-id="04b7d-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="04b7d-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="04b7d-139">Obiekt wyjściowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="04b7d-139">The output database object</span></span>

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

### <span data-ttu-id="04b7d-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="04b7d-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="04b7d-141">Identyfikator zasobu wyjściowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="04b7d-141">The output database resource id</span></span>

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

### <span data-ttu-id="04b7d-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="04b7d-142">-OutputSchemaName</span></span>
<span data-ttu-id="04b7d-143">Nazwa schematu wyjściowego</span><span class="sxs-lookup"><span data-stu-id="04b7d-143">The output schema name</span></span>

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

### <span data-ttu-id="04b7d-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="04b7d-144">-OutputTableName</span></span>
<span data-ttu-id="04b7d-145">Nazwa tabeli wyjściowej</span><span class="sxs-lookup"><span data-stu-id="04b7d-145">The output table name</span></span>

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

### <span data-ttu-id="04b7d-146">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="04b7d-146">-ParentObject</span></span>
<span data-ttu-id="04b7d-147">Obiekt zadania</span><span class="sxs-lookup"><span data-stu-id="04b7d-147">The job object</span></span>

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

### <span data-ttu-id="04b7d-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="04b7d-148">-ParentResourceId</span></span>
<span data-ttu-id="04b7d-149">Identyfikator zasobu zadań</span><span class="sxs-lookup"><span data-stu-id="04b7d-149">The job resource id</span></span>

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

### <span data-ttu-id="04b7d-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04b7d-150">-ResourceGroupName</span></span>
<span data-ttu-id="04b7d-151">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="04b7d-151">The resource group name</span></span>

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

### <span data-ttu-id="04b7d-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="04b7d-152">-RetryAttempts</span></span>
<span data-ttu-id="04b7d-153">Ponów próbę</span><span class="sxs-lookup"><span data-stu-id="04b7d-153">The retry attempts</span></span>

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

### <span data-ttu-id="04b7d-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="04b7d-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="04b7d-155">Interwał ponownego ponawiania próby po odjęniu mnożenia</span><span class="sxs-lookup"><span data-stu-id="04b7d-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="04b7d-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="04b7d-156">-ServerName</span></span>
<span data-ttu-id="04b7d-157">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="04b7d-157">The server name</span></span>

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

### <span data-ttu-id="04b7d-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="04b7d-158">-StepId</span></span>
<span data-ttu-id="04b7d-159">Identyfikator kroku</span><span class="sxs-lookup"><span data-stu-id="04b7d-159">The step id</span></span>

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

### <span data-ttu-id="04b7d-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="04b7d-160">-TargetGroupName</span></span>
<span data-ttu-id="04b7d-161">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="04b7d-161">The target group name</span></span>

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

### <span data-ttu-id="04b7d-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="04b7d-162">-TimeoutSeconds</span></span>
<span data-ttu-id="04b7d-163">Przeo jej czasu w sekundach</span><span class="sxs-lookup"><span data-stu-id="04b7d-163">The time out seconds</span></span>

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

### <span data-ttu-id="04b7d-164">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04b7d-164">-Confirm</span></span>
<span data-ttu-id="04b7d-165">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="04b7d-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04b7d-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04b7d-166">-WhatIf</span></span>
<span data-ttu-id="04b7d-167">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04b7d-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04b7d-168">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="04b7d-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04b7d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b7d-169">CommonParameters</span></span>
<span data-ttu-id="04b7d-170">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b7d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b7d-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04b7d-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b7d-172">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04b7d-172">INPUTS</span></span>

### <span data-ttu-id="04b7d-173">Microsoft.Azure.Commands.Sql.ElastycznaJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="04b7d-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="04b7d-174">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04b7d-174">OUTPUTS</span></span>

### <span data-ttu-id="04b7d-175">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="04b7d-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="04b7d-176">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04b7d-176">NOTES</span></span>

## <span data-ttu-id="04b7d-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04b7d-177">RELATED LINKS</span></span>
