---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: ec2f9174cc0ca8781b56784836a4583b0568128e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981562"
---
# <span data-ttu-id="13976-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="13976-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="13976-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13976-102">SYNOPSIS</span></span>
<span data-ttu-id="13976-103">Aktualizacje kroku zadania</span><span class="sxs-lookup"><span data-stu-id="13976-103">Updates a job step</span></span>

## <span data-ttu-id="13976-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13976-104">SYNTAX</span></span>

### <span data-ttu-id="13976-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="13976-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13976-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="13976-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13976-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="13976-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13976-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="13976-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13976-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="13976-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13976-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="13976-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13976-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="13976-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13976-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="13976-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13976-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="13976-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13976-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="13976-114">DESCRIPTION</span></span>
<span data-ttu-id="13976-115">Polecenie Set-AzSqlElasticJobStep cmdlet aktualizuje krok zadania</span><span class="sxs-lookup"><span data-stu-id="13976-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="13976-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13976-116">EXAMPLES</span></span>

### <span data-ttu-id="13976-117">Przykład 1. Aktualizacja grupy docelowej etapu zadania</span><span class="sxs-lookup"><span data-stu-id="13976-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="13976-118">Przykład 2. Aktualizacja skryptu T-SQL kroku zadania dla zadania</span><span class="sxs-lookup"><span data-stu-id="13976-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="13976-119">Aktualizacje kroku zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="13976-119">Updates a job step from a job</span></span>

### <span data-ttu-id="13976-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="13976-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="13976-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13976-121">PARAMETERS</span></span>

### <span data-ttu-id="13976-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="13976-122">-AgentName</span></span>
<span data-ttu-id="13976-123">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="13976-123">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-124">- CommandText</span><span class="sxs-lookup"><span data-stu-id="13976-124">-CommandText</span></span>
<span data-ttu-id="13976-125">Tekst polecenia</span><span class="sxs-lookup"><span data-stu-id="13976-125">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="13976-126">-CredentialName</span></span>
<span data-ttu-id="13976-127">Nazwa poświadczeń</span><span class="sxs-lookup"><span data-stu-id="13976-127">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13976-128">-DefaultProfile</span></span>
<span data-ttu-id="13976-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13976-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13976-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="13976-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="13976-131">Początkowa ponowna próba interwału (sekundy)</span><span class="sxs-lookup"><span data-stu-id="13976-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="13976-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13976-132">-InputObject</span></span>
<span data-ttu-id="13976-133">Obiekt etapu zadania</span><span class="sxs-lookup"><span data-stu-id="13976-133">The job step object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet, WithRemoveOutputUsingParentObject, WithAddOutputUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13976-134">— JobName</span><span class="sxs-lookup"><span data-stu-id="13976-134">-JobName</span></span>
<span data-ttu-id="13976-135">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="13976-135">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="13976-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="13976-137">Maksymalna liczba ponownych prób w sekundach</span><span class="sxs-lookup"><span data-stu-id="13976-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="13976-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="13976-138">-Name</span></span>
<span data-ttu-id="13976-139">Nazwa kroku</span><span class="sxs-lookup"><span data-stu-id="13976-139">The step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="13976-140">-OutputCredentialName</span></span>
<span data-ttu-id="13976-141">Nazwa poświadczeń wyjściowych</span><span class="sxs-lookup"><span data-stu-id="13976-141">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="13976-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="13976-143">Obiekt wyjściowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="13976-143">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="13976-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="13976-145">Identyfikator zasobu wyjściowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="13976-145">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithAddOutput, WithAddOutputUsingParentObject, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="13976-146">-OutputSchemaName</span></span>
<span data-ttu-id="13976-147">Nazwa schematu wyjściowego</span><span class="sxs-lookup"><span data-stu-id="13976-147">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="13976-148">-OutputTableName</span></span>
<span data-ttu-id="13976-149">Nazwa tabeli wyjściowej</span><span class="sxs-lookup"><span data-stu-id="13976-149">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="13976-150">-RemoveOutput</span></span>
<span data-ttu-id="13976-151">Flaga wskazująca, czy usunąć dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="13976-151">The flag to indicate whether to remove output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WithRemoveOutput, WithRemoveOutputUsingParentObject, WithRemoveOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13976-152">-ResourceGroupName</span></span>
<span data-ttu-id="13976-153">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="13976-153">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13976-154">-ResourceId</span></span>
<span data-ttu-id="13976-155">Identyfikator zasobu kroku zadania</span><span class="sxs-lookup"><span data-stu-id="13976-155">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithRemoveOutputUsingParentResourceId, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13976-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="13976-156">-RetryAttempts</span></span>
<span data-ttu-id="13976-157">Ponów próbę przedtemp.</span><span class="sxs-lookup"><span data-stu-id="13976-157">The retry attemps</span></span>

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

### <span data-ttu-id="13976-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="13976-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="13976-159">Mnożenie ponownego odejmowania interwału</span><span class="sxs-lookup"><span data-stu-id="13976-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="13976-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="13976-160">-ServerName</span></span>
<span data-ttu-id="13976-161">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="13976-161">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="13976-162">-StepId</span></span>
<span data-ttu-id="13976-163">Tekst identyfikatora kroku</span><span class="sxs-lookup"><span data-stu-id="13976-163">The step id text</span></span>

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

### <span data-ttu-id="13976-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="13976-164">-TargetGroupName</span></span>
<span data-ttu-id="13976-165">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="13976-165">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13976-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="13976-166">-TimeoutSeconds</span></span>
<span data-ttu-id="13976-167">Limit czasu (sekundy)</span><span class="sxs-lookup"><span data-stu-id="13976-167">The timeout seconds</span></span>

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

### <span data-ttu-id="13976-168">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13976-168">-Confirm</span></span>
<span data-ttu-id="13976-169">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13976-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13976-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13976-170">-WhatIf</span></span>
<span data-ttu-id="13976-171">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13976-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13976-172">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="13976-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13976-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13976-173">CommonParameters</span></span>
<span data-ttu-id="13976-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13976-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13976-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13976-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13976-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13976-176">INPUTS</span></span>

### <span data-ttu-id="13976-177">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="13976-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="13976-178">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13976-178">OUTPUTS</span></span>

### <span data-ttu-id="13976-179">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="13976-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="13976-180">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13976-180">NOTES</span></span>

## <span data-ttu-id="13976-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13976-181">RELATED LINKS</span></span>
