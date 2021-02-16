---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196018"
---
# <span data-ttu-id="4eb16-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="4eb16-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="4eb16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb16-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb16-103">Usuwa element docelowy z grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="4eb16-103">Removes the target from the target group</span></span>

## <span data-ttu-id="4eb16-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4eb16-104">SYNTAX</span></span>

### <span data-ttu-id="4eb16-105">SqlDatabase (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4eb16-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb16-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="4eb16-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb16-107">SqlSmap</span><span class="sxs-lookup"><span data-stu-id="4eb16-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4eb16-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4eb16-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb16-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4eb16-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb16-110">SqlSmapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4eb16-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb16-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb16-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb16-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb16-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4eb16-113">SqlSmapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb16-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb16-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="4eb16-114">DESCRIPTION</span></span>
<span data-ttu-id="4eb16-115">Polecenie Remove-AzSqlElasticJobTarget cmdlet usuwa zasób docelowy do grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="4eb16-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="4eb16-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4eb16-116">EXAMPLES</span></span>

### <span data-ttu-id="4eb16-117">Przykład 1. Usuwanie obiektu docelowego serwera</span><span class="sxs-lookup"><span data-stu-id="4eb16-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="4eb16-118">Przykład 2. Usuwanie obiektu docelowego bazy danych</span><span class="sxs-lookup"><span data-stu-id="4eb16-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="4eb16-119">Przykład 3. Usuwanie elastycznego celu puli</span><span class="sxs-lookup"><span data-stu-id="4eb16-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="4eb16-120">Przykład 4. Usuwanie obiektu docelowego mapy sowa</span><span class="sxs-lookup"><span data-stu-id="4eb16-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="4eb16-121">Usuwa element docelowy (serwer, elastyczna pula, baza danych i mapa sieciowej) z grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="4eb16-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="4eb16-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eb16-122">PARAMETERS</span></span>

### <span data-ttu-id="4eb16-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4eb16-123">-AgentName</span></span>
<span data-ttu-id="4eb16-124">Nazwa agenta bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="4eb16-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="4eb16-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="4eb16-125">-AgentServerName</span></span>
<span data-ttu-id="4eb16-126">Nazwa serwera agenta bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="4eb16-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="4eb16-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4eb16-127">-DatabaseName</span></span>
<span data-ttu-id="4eb16-128">Nazwa docelowa bazy danych</span><span class="sxs-lookup"><span data-stu-id="4eb16-128">Database Target Name</span></span>

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

### <span data-ttu-id="4eb16-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb16-129">-DefaultProfile</span></span>
<span data-ttu-id="4eb16-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4eb16-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb16-131">-PochylićPoolName</span><span class="sxs-lookup"><span data-stu-id="4eb16-131">-ElasticPoolName</span></span>
<span data-ttu-id="4eb16-132">Elastyczna nazwa docelowa puli</span><span class="sxs-lookup"><span data-stu-id="4eb16-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="4eb16-133">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="4eb16-133">-ParentObject</span></span>
<span data-ttu-id="4eb16-134">Obiekt grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="4eb16-134">The target group object.</span></span>

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

### <span data-ttu-id="4eb16-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb16-135">-ParentResourceId</span></span>
<span data-ttu-id="4eb16-136">Identyfikator zasobu grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="4eb16-136">The target group resource id.</span></span>

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

### <span data-ttu-id="4eb16-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="4eb16-137">-RefreshCredentialName</span></span>
<span data-ttu-id="4eb16-138">Refresh Credential Name</span><span class="sxs-lookup"><span data-stu-id="4eb16-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="4eb16-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb16-139">-ResourceGroupName</span></span>
<span data-ttu-id="4eb16-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4eb16-140">Resource Group Name</span></span>

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

### <span data-ttu-id="4eb16-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4eb16-141">-ServerName</span></span>
<span data-ttu-id="4eb16-142">Nazwa docelowa serwera</span><span class="sxs-lookup"><span data-stu-id="4eb16-142">Server Target Name</span></span>

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

### <span data-ttu-id="4eb16-143">-SowaMapName</span><span class="sxs-lookup"><span data-stu-id="4eb16-143">-ShardMapName</span></span>
<span data-ttu-id="4eb16-144">Sowąd mapową nazwę docelową</span><span class="sxs-lookup"><span data-stu-id="4eb16-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="4eb16-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb16-145">-TargetGroupName</span></span>
<span data-ttu-id="4eb16-146">Nazwa agenta bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="4eb16-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="4eb16-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4eb16-147">-Confirm</span></span>
<span data-ttu-id="4eb16-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4eb16-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb16-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb16-149">-WhatIf</span></span>
<span data-ttu-id="4eb16-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eb16-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb16-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4eb16-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb16-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb16-152">CommonParameters</span></span>
<span data-ttu-id="4eb16-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb16-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb16-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4eb16-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb16-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4eb16-155">INPUTS</span></span>

### <span data-ttu-id="4eb16-156">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="4eb16-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="4eb16-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb16-157">OUTPUTS</span></span>

### <span data-ttu-id="4eb16-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="4eb16-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="4eb16-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4eb16-159">NOTES</span></span>

## <span data-ttu-id="4eb16-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4eb16-160">RELATED LINKS</span></span>
