---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 7e1c03b176974c85802451980df24f5a7fdf9b1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887245"
---
# <span data-ttu-id="8d63b-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="8d63b-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="8d63b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d63b-102">SYNOPSIS</span></span>
<span data-ttu-id="8d63b-103">Aktualizowanie kroku zadania</span><span class="sxs-lookup"><span data-stu-id="8d63b-103">Updates a job step</span></span>

## <span data-ttu-id="8d63b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d63b-104">SYNTAX</span></span>

### <span data-ttu-id="8d63b-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8d63b-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d63b-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="8d63b-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d63b-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="8d63b-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d63b-108">Obiekt</span><span class="sxs-lookup"><span data-stu-id="8d63b-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d63b-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8d63b-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d63b-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8d63b-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d63b-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8d63b-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d63b-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8d63b-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d63b-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8d63b-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d63b-114">Opis</span><span class="sxs-lookup"><span data-stu-id="8d63b-114">DESCRIPTION</span></span>
<span data-ttu-id="8d63b-115">Polecenie cmdlet Set-AzSqlElasticJobStep aktualizuje krok zadania</span><span class="sxs-lookup"><span data-stu-id="8d63b-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="8d63b-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d63b-116">EXAMPLES</span></span>

### <span data-ttu-id="8d63b-117">Przykład 1-Aktualizowanie grupy docelowej krok zadania dla zadania</span><span class="sxs-lookup"><span data-stu-id="8d63b-117">Example 1 - Updates a job step's target group for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="8d63b-118">Przykład 2 — aktualizuje skrypt T-SQL kroku zadania dla zadania</span><span class="sxs-lookup"><span data-stu-id="8d63b-118">Example 2 - Updates a job step's T-SQL script for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="8d63b-119">Aktualizowanie kroku zadania na podstawie zadania</span><span class="sxs-lookup"><span data-stu-id="8d63b-119">Updates a job step from a job</span></span>

## <span data-ttu-id="8d63b-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d63b-120">PARAMETERS</span></span>

### <span data-ttu-id="8d63b-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8d63b-121">-AgentName</span></span>
<span data-ttu-id="8d63b-122">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="8d63b-122">The agent name</span></span>

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

### <span data-ttu-id="8d63b-123">-CommandText</span><span class="sxs-lookup"><span data-stu-id="8d63b-123">-CommandText</span></span>
<span data-ttu-id="8d63b-124">Tekst polecenia</span><span class="sxs-lookup"><span data-stu-id="8d63b-124">The command text</span></span>

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

### <span data-ttu-id="8d63b-125">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="8d63b-125">-CredentialName</span></span>
<span data-ttu-id="8d63b-126">Nazwa poświadczenia</span><span class="sxs-lookup"><span data-stu-id="8d63b-126">The credential name</span></span>

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

### <span data-ttu-id="8d63b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d63b-127">-DefaultProfile</span></span>
<span data-ttu-id="8d63b-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d63b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d63b-129">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="8d63b-129">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="8d63b-130">Początkowy interwał ponawiania prób w sekundach</span><span class="sxs-lookup"><span data-stu-id="8d63b-130">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="8d63b-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8d63b-131">-InputObject</span></span>
<span data-ttu-id="8d63b-132">Obiekt etap zadania</span><span class="sxs-lookup"><span data-stu-id="8d63b-132">The job step object</span></span>

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

### <span data-ttu-id="8d63b-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="8d63b-133">-JobName</span></span>
<span data-ttu-id="8d63b-134">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="8d63b-134">The job name</span></span>

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

### <span data-ttu-id="8d63b-135">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="8d63b-135">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="8d63b-136">Maksymalny interwał ponawiania prób w sekundach</span><span class="sxs-lookup"><span data-stu-id="8d63b-136">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="8d63b-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8d63b-137">-Name</span></span>
<span data-ttu-id="8d63b-138">Nazwa kroku</span><span class="sxs-lookup"><span data-stu-id="8d63b-138">The step name</span></span>

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

### <span data-ttu-id="8d63b-139">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="8d63b-139">-OutputCredentialName</span></span>
<span data-ttu-id="8d63b-140">Nazwa poświadczenia danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="8d63b-140">The output credential name</span></span>

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

### <span data-ttu-id="8d63b-141">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8d63b-141">-OutputDatabaseObject</span></span>
<span data-ttu-id="8d63b-142">Wyjściowy obiekt bazy danych</span><span class="sxs-lookup"><span data-stu-id="8d63b-142">The output database object</span></span>

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

### <span data-ttu-id="8d63b-143">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="8d63b-143">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="8d63b-144">Identyfikator zasobu bazy danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="8d63b-144">The output database resource id</span></span>

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

### <span data-ttu-id="8d63b-145">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="8d63b-145">-OutputSchemaName</span></span>
<span data-ttu-id="8d63b-146">Nazwa schematu wyjściowego</span><span class="sxs-lookup"><span data-stu-id="8d63b-146">The output schema name</span></span>

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

### <span data-ttu-id="8d63b-147">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="8d63b-147">-OutputTableName</span></span>
<span data-ttu-id="8d63b-148">Nazwa tabeli wyjściowej</span><span class="sxs-lookup"><span data-stu-id="8d63b-148">The output table name</span></span>

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

### <span data-ttu-id="8d63b-149">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="8d63b-149">-RemoveOutput</span></span>
<span data-ttu-id="8d63b-150">Flaga wskazująca, czy usunąć dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="8d63b-150">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="8d63b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d63b-151">-ResourceGroupName</span></span>
<span data-ttu-id="8d63b-152">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8d63b-152">The resource group name</span></span>

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

### <span data-ttu-id="8d63b-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d63b-153">-ResourceId</span></span>
<span data-ttu-id="8d63b-154">Identyfikator zasobu krok zadania</span><span class="sxs-lookup"><span data-stu-id="8d63b-154">The job step resource id</span></span>

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

### <span data-ttu-id="8d63b-155">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="8d63b-155">-RetryAttempts</span></span>
<span data-ttu-id="8d63b-156">Ponowna próba attemps</span><span class="sxs-lookup"><span data-stu-id="8d63b-156">The retry attemps</span></span>

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

### <span data-ttu-id="8d63b-157">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="8d63b-157">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="8d63b-158">Mnożnik Backoff interwał ponawiania</span><span class="sxs-lookup"><span data-stu-id="8d63b-158">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="8d63b-159">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8d63b-159">-ServerName</span></span>
<span data-ttu-id="8d63b-160">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="8d63b-160">The server name</span></span>

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

### <span data-ttu-id="8d63b-161">-StepId</span><span class="sxs-lookup"><span data-stu-id="8d63b-161">-StepId</span></span>
<span data-ttu-id="8d63b-162">Tekst identyfikatora kroku</span><span class="sxs-lookup"><span data-stu-id="8d63b-162">The step id text</span></span>

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

### <span data-ttu-id="8d63b-163">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="8d63b-163">-TargetGroupName</span></span>
<span data-ttu-id="8d63b-164">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="8d63b-164">The target group name</span></span>

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

### <span data-ttu-id="8d63b-165">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="8d63b-165">-TimeoutSeconds</span></span>
<span data-ttu-id="8d63b-166">Limit czasu w sekundach</span><span class="sxs-lookup"><span data-stu-id="8d63b-166">The timeout seconds</span></span>

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

### <span data-ttu-id="8d63b-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d63b-167">-Confirm</span></span>
<span data-ttu-id="8d63b-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d63b-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d63b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d63b-169">-WhatIf</span></span>
<span data-ttu-id="8d63b-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d63b-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d63b-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8d63b-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d63b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d63b-172">CommonParameters</span></span>
<span data-ttu-id="8d63b-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d63b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d63b-174">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d63b-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d63b-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d63b-175">INPUTS</span></span>

### <span data-ttu-id="8d63b-176">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="8d63b-176">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="8d63b-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d63b-177">OUTPUTS</span></span>

### <span data-ttu-id="8d63b-178">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="8d63b-178">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="8d63b-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d63b-179">NOTES</span></span>

## <span data-ttu-id="8d63b-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d63b-180">RELATED LINKS</span></span>
