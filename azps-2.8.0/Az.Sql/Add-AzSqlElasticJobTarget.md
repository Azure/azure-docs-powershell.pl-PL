---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: d1788abc6ac0546732fe2476cf2822210a1fa8da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871468"
---
# <span data-ttu-id="06ede-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="06ede-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="06ede-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06ede-102">SYNOPSIS</span></span>
<span data-ttu-id="06ede-103">Dodawanie elementu docelowego do grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="06ede-103">Adds a target to a target group</span></span>

## <span data-ttu-id="06ede-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06ede-104">SYNTAX</span></span>

### <span data-ttu-id="06ede-105">SQLDatabase (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="06ede-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06ede-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="06ede-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06ede-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="06ede-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06ede-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="06ede-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06ede-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="06ede-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06ede-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="06ede-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06ede-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="06ede-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06ede-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="06ede-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06ede-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="06ede-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06ede-114">Opis</span><span class="sxs-lookup"><span data-stu-id="06ede-114">DESCRIPTION</span></span>
<span data-ttu-id="06ede-115">Polecenie cmdlet Add-AzSqlElasticJobTarget Dodawanie zasobu docelowego do grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="06ede-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="06ede-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06ede-116">EXAMPLES</span></span>

### <span data-ttu-id="06ede-117">Przykład 1-Dodawanie obiektu docelowego serwera</span><span class="sxs-lookup"><span data-stu-id="06ede-117">Example 1 - Add a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="06ede-118">Przykład 2 — Dodawanie obiektu docelowego bazy danych</span><span class="sxs-lookup"><span data-stu-id="06ede-118">Example 2 - Add a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="06ede-119">Przykład 3 — Dodawanie elementu docelowego puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="06ede-119">Example 3 - Add an elastic pool target</span></span>
```
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="06ede-120">Przykład 4-Dodawanie obiektu docelowego mapy Shard</span><span class="sxs-lookup"><span data-stu-id="06ede-120">Example 4 - Add a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="06ede-121">Dodaje docelową (serwerową, elastyczną pulę, bazę danych i mapę Shard) do grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="06ede-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="06ede-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06ede-122">PARAMETERS</span></span>

### <span data-ttu-id="06ede-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="06ede-123">-AgentName</span></span>
<span data-ttu-id="06ede-124">Nazwa agenta.</span><span class="sxs-lookup"><span data-stu-id="06ede-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="06ede-125">-AgentServerName</span></span>
<span data-ttu-id="06ede-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="06ede-126">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06ede-127">-DatabaseName</span></span>
<span data-ttu-id="06ede-128">Nazwa celu bazy danych</span><span class="sxs-lookup"><span data-stu-id="06ede-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ede-129">-DefaultProfile</span></span>
<span data-ttu-id="06ede-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06ede-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06ede-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="06ede-131">-ElasticPoolName</span></span>
<span data-ttu-id="06ede-132">Nazwa docelowa puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="06ede-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-133">-Wyklucz</span><span class="sxs-lookup"><span data-stu-id="06ede-133">-Exclude</span></span>
<span data-ttu-id="06ede-134">Wyklucza element docelowy.</span><span class="sxs-lookup"><span data-stu-id="06ede-134">Excludes a target.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-135">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="06ede-135">-ParentObject</span></span>
<span data-ttu-id="06ede-136">Obiekt grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="06ede-136">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="06ede-137">-ParentResourceId</span></span>
<span data-ttu-id="06ede-138">Identyfikator zasobu grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="06ede-138">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="06ede-139">-RefreshCredentialName</span></span>
<span data-ttu-id="06ede-140">Odśwież nazwę poświadczenia</span><span class="sxs-lookup"><span data-stu-id="06ede-140">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06ede-141">-ResourceGroupName</span></span>
<span data-ttu-id="06ede-142">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="06ede-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-143">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="06ede-143">-ServerName</span></span>
<span data-ttu-id="06ede-144">Nazwa docelowa serwera</span><span class="sxs-lookup"><span data-stu-id="06ede-144">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="06ede-145">-ShardMapName</span></span>
<span data-ttu-id="06ede-146">Nazwa docelowa mapy Shard</span><span class="sxs-lookup"><span data-stu-id="06ede-146">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="06ede-147">-TargetGroupName</span></span>
<span data-ttu-id="06ede-148">Nazwa grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="06ede-148">The target group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ede-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06ede-149">-Confirm</span></span>
<span data-ttu-id="06ede-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06ede-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06ede-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06ede-151">-WhatIf</span></span>
<span data-ttu-id="06ede-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06ede-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06ede-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06ede-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06ede-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ede-154">CommonParameters</span></span>
<span data-ttu-id="06ede-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ede-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ede-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06ede-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ede-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06ede-157">INPUTS</span></span>

### <span data-ttu-id="06ede-158">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="06ede-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="06ede-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06ede-159">OUTPUTS</span></span>

### <span data-ttu-id="06ede-160">Microsoft. Azure. Management. SQL. MODELES. JobTarget</span><span class="sxs-lookup"><span data-stu-id="06ede-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="06ede-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06ede-161">NOTES</span></span>

## <span data-ttu-id="06ede-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06ede-162">RELATED LINKS</span></span>
