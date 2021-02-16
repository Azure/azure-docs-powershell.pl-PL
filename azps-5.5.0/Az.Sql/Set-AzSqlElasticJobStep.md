---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176762"
---
# <span data-ttu-id="4ce29-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="4ce29-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="4ce29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ce29-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce29-103">Aktualizacje kroku zadania</span><span class="sxs-lookup"><span data-stu-id="4ce29-103">Updates a job step</span></span>

## <span data-ttu-id="4ce29-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ce29-104">SYNTAX</span></span>

### <span data-ttu-id="4ce29-105">DefaultSet (Default)</span><span class="sxs-lookup"><span data-stu-id="4ce29-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce29-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="4ce29-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ce29-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="4ce29-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ce29-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ce29-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce29-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4ce29-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce29-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4ce29-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce29-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ce29-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce29-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce29-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ce29-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce29-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ce29-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ce29-114">DESCRIPTION</span></span>
<span data-ttu-id="4ce29-115">Polecenie Set-AzSqlElasticJobStep cmdlet aktualizuje krok zadania</span><span class="sxs-lookup"><span data-stu-id="4ce29-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="4ce29-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ce29-116">EXAMPLES</span></span>

### <span data-ttu-id="4ce29-117">Przykład 1. Aktualizacja grupy docelowej etapu zadania</span><span class="sxs-lookup"><span data-stu-id="4ce29-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="4ce29-118">Przykład 2. Aktualizacja skryptu T-SQL kroku zadania dla zadania</span><span class="sxs-lookup"><span data-stu-id="4ce29-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="4ce29-119">Aktualizacje kroku zadania z zadania</span><span class="sxs-lookup"><span data-stu-id="4ce29-119">Updates a job step from a job</span></span>

### <span data-ttu-id="4ce29-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4ce29-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="4ce29-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ce29-121">PARAMETERS</span></span>

### <span data-ttu-id="4ce29-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4ce29-122">-AgentName</span></span>
<span data-ttu-id="4ce29-123">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="4ce29-123">The agent name</span></span>

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

### <span data-ttu-id="4ce29-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="4ce29-124">-CommandText</span></span>
<span data-ttu-id="4ce29-125">Tekst polecenia</span><span class="sxs-lookup"><span data-stu-id="4ce29-125">The command text</span></span>

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

### <span data-ttu-id="4ce29-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="4ce29-126">-CredentialName</span></span>
<span data-ttu-id="4ce29-127">Nazwa poświadczeń</span><span class="sxs-lookup"><span data-stu-id="4ce29-127">The credential name</span></span>

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

### <span data-ttu-id="4ce29-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce29-128">-DefaultProfile</span></span>
<span data-ttu-id="4ce29-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce29-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce29-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="4ce29-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="4ce29-131">Początkowa ponowna próba interwału (sekundy)</span><span class="sxs-lookup"><span data-stu-id="4ce29-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="4ce29-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ce29-132">-InputObject</span></span>
<span data-ttu-id="4ce29-133">Obiekt etapu zadania</span><span class="sxs-lookup"><span data-stu-id="4ce29-133">The job step object</span></span>

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

### <span data-ttu-id="4ce29-134">— JobName</span><span class="sxs-lookup"><span data-stu-id="4ce29-134">-JobName</span></span>
<span data-ttu-id="4ce29-135">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="4ce29-135">The job name</span></span>

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

### <span data-ttu-id="4ce29-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="4ce29-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="4ce29-137">Maksymalna liczba ponownych prób w sekundach</span><span class="sxs-lookup"><span data-stu-id="4ce29-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="4ce29-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4ce29-138">-Name</span></span>
<span data-ttu-id="4ce29-139">Nazwa etapu</span><span class="sxs-lookup"><span data-stu-id="4ce29-139">The step name</span></span>

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

### <span data-ttu-id="4ce29-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="4ce29-140">-OutputCredentialName</span></span>
<span data-ttu-id="4ce29-141">Nazwa poświadczeń wyjściowych</span><span class="sxs-lookup"><span data-stu-id="4ce29-141">The output credential name</span></span>

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

### <span data-ttu-id="4ce29-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4ce29-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="4ce29-143">Obiekt wyjściowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="4ce29-143">The output database object</span></span>

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

### <span data-ttu-id="4ce29-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce29-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="4ce29-145">Identyfikator zasobu wyjściowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="4ce29-145">The output database resource id</span></span>

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

### <span data-ttu-id="4ce29-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="4ce29-146">-OutputSchemaName</span></span>
<span data-ttu-id="4ce29-147">Nazwa schematu wyjściowego</span><span class="sxs-lookup"><span data-stu-id="4ce29-147">The output schema name</span></span>

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

### <span data-ttu-id="4ce29-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="4ce29-148">-OutputTableName</span></span>
<span data-ttu-id="4ce29-149">Nazwa tabeli wyjściowej</span><span class="sxs-lookup"><span data-stu-id="4ce29-149">The output table name</span></span>

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

### <span data-ttu-id="4ce29-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="4ce29-150">-RemoveOutput</span></span>
<span data-ttu-id="4ce29-151">Flaga wskazująca, czy usunąć dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="4ce29-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="4ce29-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce29-152">-ResourceGroupName</span></span>
<span data-ttu-id="4ce29-153">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4ce29-153">The resource group name</span></span>

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

### <span data-ttu-id="4ce29-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce29-154">-ResourceId</span></span>
<span data-ttu-id="4ce29-155">Identyfikator zasobu kroku zadania</span><span class="sxs-lookup"><span data-stu-id="4ce29-155">The job step resource id</span></span>

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

### <span data-ttu-id="4ce29-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="4ce29-156">-RetryAttempts</span></span>
<span data-ttu-id="4ce29-157">Ponów próbę przedtemp.</span><span class="sxs-lookup"><span data-stu-id="4ce29-157">The retry attemps</span></span>

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

### <span data-ttu-id="4ce29-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="4ce29-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="4ce29-159">Mnożenie ponownego odejmowania interwału</span><span class="sxs-lookup"><span data-stu-id="4ce29-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="4ce29-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4ce29-160">-ServerName</span></span>
<span data-ttu-id="4ce29-161">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="4ce29-161">The server name</span></span>

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

### <span data-ttu-id="4ce29-162">- StepId</span><span class="sxs-lookup"><span data-stu-id="4ce29-162">-StepId</span></span>
<span data-ttu-id="4ce29-163">Tekst identyfikatora kroku</span><span class="sxs-lookup"><span data-stu-id="4ce29-163">The step id text</span></span>

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

### <span data-ttu-id="4ce29-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce29-164">-TargetGroupName</span></span>
<span data-ttu-id="4ce29-165">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="4ce29-165">The target group name</span></span>

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

### <span data-ttu-id="4ce29-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="4ce29-166">-TimeoutSeconds</span></span>
<span data-ttu-id="4ce29-167">Limit czasu (sekundy)</span><span class="sxs-lookup"><span data-stu-id="4ce29-167">The timeout seconds</span></span>

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

### <span data-ttu-id="4ce29-168">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ce29-168">-Confirm</span></span>
<span data-ttu-id="4ce29-169">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4ce29-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce29-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce29-170">-WhatIf</span></span>
<span data-ttu-id="4ce29-171">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce29-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ce29-172">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4ce29-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce29-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce29-173">CommonParameters</span></span>
<span data-ttu-id="4ce29-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce29-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce29-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ce29-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce29-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ce29-176">INPUTS</span></span>

### <span data-ttu-id="4ce29-177">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="4ce29-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="4ce29-178">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ce29-178">OUTPUTS</span></span>

### <span data-ttu-id="4ce29-179">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="4ce29-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="4ce29-180">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ce29-180">NOTES</span></span>

## <span data-ttu-id="4ce29-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ce29-181">RELATED LINKS</span></span>
