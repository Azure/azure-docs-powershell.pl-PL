---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 94ad9cb0c6c1db6ebc7233c63dcd26e8eebb4bef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051920"
---
# <span data-ttu-id="6ca87-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="6ca87-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="6ca87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ca87-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca87-103">Usuwa element docelowy z grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="6ca87-103">Removes the target from the target group</span></span>

## <span data-ttu-id="6ca87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ca87-104">SYNTAX</span></span>

### <span data-ttu-id="6ca87-105">SQLDatabase (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6ca87-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca87-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="6ca87-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca87-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="6ca87-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ca87-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6ca87-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca87-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6ca87-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca87-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6ca87-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca87-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca87-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca87-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca87-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ca87-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca87-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca87-114">Opis</span><span class="sxs-lookup"><span data-stu-id="6ca87-114">DESCRIPTION</span></span>
<span data-ttu-id="6ca87-115">Polecenie cmdlet Remove-AzSqlElasticJobTarget usuwa zasób docelowy do grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="6ca87-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="6ca87-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ca87-116">EXAMPLES</span></span>

### <span data-ttu-id="6ca87-117">Przykład 1-Usuwanie obiektu docelowego serwera</span><span class="sxs-lookup"><span data-stu-id="6ca87-117">Example 1 - Remove a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="6ca87-118">Przykład 2 — Usuwanie obiektu docelowego bazy danych</span><span class="sxs-lookup"><span data-stu-id="6ca87-118">Example 2 - Remove a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="6ca87-119">Przykład 3 — Usuwanie elementu docelowego puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="6ca87-119">Example 3 - Remove an elastic pool target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="6ca87-120">Przykład 4 — Usuwanie obiektu docelowego mapy Shard</span><span class="sxs-lookup"><span data-stu-id="6ca87-120">Example 4 - Remove a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="6ca87-121">Usuwa element docelowy (serwer, elastyczna Pula, baza danych i mapa Shard) z grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="6ca87-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="6ca87-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ca87-122">PARAMETERS</span></span>

### <span data-ttu-id="6ca87-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6ca87-123">-AgentName</span></span>
<span data-ttu-id="6ca87-124">Nazwa agenta bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6ca87-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="6ca87-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="6ca87-125">-AgentServerName</span></span>
<span data-ttu-id="6ca87-126">Nazwa serwera agenta bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6ca87-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="6ca87-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6ca87-127">-DatabaseName</span></span>
<span data-ttu-id="6ca87-128">Nazwa celu bazy danych</span><span class="sxs-lookup"><span data-stu-id="6ca87-128">Database Target Name</span></span>

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

### <span data-ttu-id="6ca87-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca87-129">-DefaultProfile</span></span>
<span data-ttu-id="6ca87-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca87-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca87-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6ca87-131">-ElasticPoolName</span></span>
<span data-ttu-id="6ca87-132">Nazwa docelowa puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="6ca87-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="6ca87-133">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="6ca87-133">-ParentObject</span></span>
<span data-ttu-id="6ca87-134">Obiekt grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="6ca87-134">The target group object.</span></span>

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

### <span data-ttu-id="6ca87-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca87-135">-ParentResourceId</span></span>
<span data-ttu-id="6ca87-136">Identyfikator zasobu grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="6ca87-136">The target group resource id.</span></span>

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

### <span data-ttu-id="6ca87-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="6ca87-137">-RefreshCredentialName</span></span>
<span data-ttu-id="6ca87-138">Odśwież nazwę poświadczenia</span><span class="sxs-lookup"><span data-stu-id="6ca87-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="6ca87-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca87-139">-ResourceGroupName</span></span>
<span data-ttu-id="6ca87-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6ca87-140">Resource Group Name</span></span>

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

### <span data-ttu-id="6ca87-141">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6ca87-141">-ServerName</span></span>
<span data-ttu-id="6ca87-142">Nazwa docelowa serwera</span><span class="sxs-lookup"><span data-stu-id="6ca87-142">Server Target Name</span></span>

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

### <span data-ttu-id="6ca87-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="6ca87-143">-ShardMapName</span></span>
<span data-ttu-id="6ca87-144">Nazwa docelowa mapy Shard</span><span class="sxs-lookup"><span data-stu-id="6ca87-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="6ca87-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca87-145">-TargetGroupName</span></span>
<span data-ttu-id="6ca87-146">Nazwa agenta bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6ca87-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="6ca87-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ca87-147">-Confirm</span></span>
<span data-ttu-id="6ca87-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca87-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca87-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca87-149">-WhatIf</span></span>
<span data-ttu-id="6ca87-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca87-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca87-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ca87-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca87-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca87-152">CommonParameters</span></span>
<span data-ttu-id="6ca87-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca87-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca87-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ca87-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca87-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ca87-155">INPUTS</span></span>

### <span data-ttu-id="6ca87-156">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="6ca87-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="6ca87-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ca87-157">OUTPUTS</span></span>

### <span data-ttu-id="6ca87-158">Microsoft. Azure. Management. SQL. MODELES. JobTarget</span><span class="sxs-lookup"><span data-stu-id="6ca87-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="6ca87-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ca87-159">NOTES</span></span>

## <span data-ttu-id="6ca87-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ca87-160">RELATED LINKS</span></span>
