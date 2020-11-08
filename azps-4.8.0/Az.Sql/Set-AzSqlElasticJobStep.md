---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222844"
---
# <span data-ttu-id="fa710-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="fa710-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="fa710-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa710-102">SYNOPSIS</span></span>
<span data-ttu-id="fa710-103">Aktualizowanie kroku zadania</span><span class="sxs-lookup"><span data-stu-id="fa710-103">Updates a job step</span></span>

## <span data-ttu-id="fa710-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa710-104">SYNTAX</span></span>

### <span data-ttu-id="fa710-105">DefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fa710-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa710-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="fa710-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa710-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="fa710-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa710-108">Obiekt</span><span class="sxs-lookup"><span data-stu-id="fa710-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa710-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fa710-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa710-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fa710-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa710-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fa710-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa710-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fa710-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa710-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fa710-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa710-114">Opis</span><span class="sxs-lookup"><span data-stu-id="fa710-114">DESCRIPTION</span></span>
<span data-ttu-id="fa710-115">Polecenie cmdlet Set-AzSqlElasticJobStep aktualizuje krok zadania</span><span class="sxs-lookup"><span data-stu-id="fa710-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="fa710-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa710-116">EXAMPLES</span></span>

### <span data-ttu-id="fa710-117">Przykład 1: aktualizowanie grupy docelowej etapu zadania dla zadania</span><span class="sxs-lookup"><span data-stu-id="fa710-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="fa710-118">Przykład 2: aktualizowanie skryptu T-SQL kroku zadania dla zadania</span><span class="sxs-lookup"><span data-stu-id="fa710-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="fa710-119">Aktualizowanie kroku zadania na podstawie zadania</span><span class="sxs-lookup"><span data-stu-id="fa710-119">Updates a job step from a job</span></span>

### <span data-ttu-id="fa710-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fa710-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="fa710-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa710-121">PARAMETERS</span></span>

### <span data-ttu-id="fa710-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fa710-122">-AgentName</span></span>
<span data-ttu-id="fa710-123">Nazwa agenta</span><span class="sxs-lookup"><span data-stu-id="fa710-123">The agent name</span></span>

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

### <span data-ttu-id="fa710-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="fa710-124">-CommandText</span></span>
<span data-ttu-id="fa710-125">Tekst polecenia</span><span class="sxs-lookup"><span data-stu-id="fa710-125">The command text</span></span>

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

### <span data-ttu-id="fa710-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="fa710-126">-CredentialName</span></span>
<span data-ttu-id="fa710-127">Nazwa poświadczenia</span><span class="sxs-lookup"><span data-stu-id="fa710-127">The credential name</span></span>

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

### <span data-ttu-id="fa710-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa710-128">-DefaultProfile</span></span>
<span data-ttu-id="fa710-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa710-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa710-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="fa710-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="fa710-131">Początkowy interwał ponawiania prób w sekundach</span><span class="sxs-lookup"><span data-stu-id="fa710-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="fa710-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fa710-132">-InputObject</span></span>
<span data-ttu-id="fa710-133">Obiekt etap zadania</span><span class="sxs-lookup"><span data-stu-id="fa710-133">The job step object</span></span>

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

### <span data-ttu-id="fa710-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="fa710-134">-JobName</span></span>
<span data-ttu-id="fa710-135">Nazwa zadania</span><span class="sxs-lookup"><span data-stu-id="fa710-135">The job name</span></span>

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

### <span data-ttu-id="fa710-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="fa710-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="fa710-137">Maksymalny interwał ponawiania prób w sekundach</span><span class="sxs-lookup"><span data-stu-id="fa710-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="fa710-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa710-138">-Name</span></span>
<span data-ttu-id="fa710-139">Nazwa kroku</span><span class="sxs-lookup"><span data-stu-id="fa710-139">The step name</span></span>

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

### <span data-ttu-id="fa710-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="fa710-140">-OutputCredentialName</span></span>
<span data-ttu-id="fa710-141">Nazwa poświadczenia danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="fa710-141">The output credential name</span></span>

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

### <span data-ttu-id="fa710-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fa710-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="fa710-143">Wyjściowy obiekt bazy danych</span><span class="sxs-lookup"><span data-stu-id="fa710-143">The output database object</span></span>

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

### <span data-ttu-id="fa710-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="fa710-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="fa710-145">Identyfikator zasobu bazy danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="fa710-145">The output database resource id</span></span>

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

### <span data-ttu-id="fa710-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="fa710-146">-OutputSchemaName</span></span>
<span data-ttu-id="fa710-147">Nazwa schematu wyjściowego</span><span class="sxs-lookup"><span data-stu-id="fa710-147">The output schema name</span></span>

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

### <span data-ttu-id="fa710-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="fa710-148">-OutputTableName</span></span>
<span data-ttu-id="fa710-149">Nazwa tabeli wyjściowej</span><span class="sxs-lookup"><span data-stu-id="fa710-149">The output table name</span></span>

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

### <span data-ttu-id="fa710-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="fa710-150">-RemoveOutput</span></span>
<span data-ttu-id="fa710-151">Flaga wskazująca, czy usunąć dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="fa710-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="fa710-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa710-152">-ResourceGroupName</span></span>
<span data-ttu-id="fa710-153">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fa710-153">The resource group name</span></span>

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

### <span data-ttu-id="fa710-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa710-154">-ResourceId</span></span>
<span data-ttu-id="fa710-155">Identyfikator zasobu krok zadania</span><span class="sxs-lookup"><span data-stu-id="fa710-155">The job step resource id</span></span>

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

### <span data-ttu-id="fa710-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="fa710-156">-RetryAttempts</span></span>
<span data-ttu-id="fa710-157">Ponowna próba attemps</span><span class="sxs-lookup"><span data-stu-id="fa710-157">The retry attemps</span></span>

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

### <span data-ttu-id="fa710-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="fa710-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="fa710-159">Mnożnik Backoff interwał ponawiania</span><span class="sxs-lookup"><span data-stu-id="fa710-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="fa710-160">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fa710-160">-ServerName</span></span>
<span data-ttu-id="fa710-161">Nazwa serwera</span><span class="sxs-lookup"><span data-stu-id="fa710-161">The server name</span></span>

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

### <span data-ttu-id="fa710-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="fa710-162">-StepId</span></span>
<span data-ttu-id="fa710-163">Tekst identyfikatora kroku</span><span class="sxs-lookup"><span data-stu-id="fa710-163">The step id text</span></span>

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

### <span data-ttu-id="fa710-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="fa710-164">-TargetGroupName</span></span>
<span data-ttu-id="fa710-165">Nazwa grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="fa710-165">The target group name</span></span>

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

### <span data-ttu-id="fa710-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="fa710-166">-TimeoutSeconds</span></span>
<span data-ttu-id="fa710-167">Limit czasu w sekundach</span><span class="sxs-lookup"><span data-stu-id="fa710-167">The timeout seconds</span></span>

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

### <span data-ttu-id="fa710-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa710-168">-Confirm</span></span>
<span data-ttu-id="fa710-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa710-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa710-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa710-170">-WhatIf</span></span>
<span data-ttu-id="fa710-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa710-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa710-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa710-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa710-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa710-173">CommonParameters</span></span>
<span data-ttu-id="fa710-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa710-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa710-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa710-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa710-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa710-176">INPUTS</span></span>

### <span data-ttu-id="fa710-177">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="fa710-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="fa710-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa710-178">OUTPUTS</span></span>

### <span data-ttu-id="fa710-179">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="fa710-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="fa710-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa710-180">NOTES</span></span>

## <span data-ttu-id="fa710-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa710-181">RELATED LINKS</span></span>
