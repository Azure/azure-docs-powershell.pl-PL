---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: cdf50079a08a4ac021e78e210ae574aa978674fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191131"
---
# <span data-ttu-id="9f4f2-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="9f4f2-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="9f4f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9f4f2-103">Dodaje element docelowy do grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="9f4f2-103">Adds a target to a target group</span></span>

## <span data-ttu-id="9f4f2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9f4f2-104">SYNTAX</span></span>

### <span data-ttu-id="9f4f2-105">SqlDatabase (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9f4f2-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="9f4f2-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-107">SqlSmap</span><span class="sxs-lookup"><span data-stu-id="9f4f2-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="9f4f2-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="9f4f2-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-110">SqlSmapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="9f4f2-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9f4f2-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9f4f2-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f4f2-113">SqlSmapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9f4f2-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f4f2-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="9f4f2-114">DESCRIPTION</span></span>
<span data-ttu-id="9f4f2-115">Polecenie Add-AzSqlElasticJobTarget cmdlet dodaje zasób docelowy do grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="9f4f2-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="9f4f2-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9f4f2-116">EXAMPLES</span></span>

### <span data-ttu-id="9f4f2-117">Przykład 1. Dodawanie obiektu docelowego serwera</span><span class="sxs-lookup"><span data-stu-id="9f4f2-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="9f4f2-118">Przykład 2. Dodawanie obiektu docelowego bazy danych</span><span class="sxs-lookup"><span data-stu-id="9f4f2-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="9f4f2-119">Przykład 3. Dodawanie elastycznego celu puli</span><span class="sxs-lookup"><span data-stu-id="9f4f2-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="9f4f2-120">Przykład 4. Dodawanie celu mapy sowa</span><span class="sxs-lookup"><span data-stu-id="9f4f2-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="9f4f2-121">Dodaje element docelowy (serwer, elastyczna pula, baza danych i mapa mapy mapy docelowej) do grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="9f4f2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f4f2-122">PARAMETERS</span></span>

### <span data-ttu-id="9f4f2-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-123">-AgentName</span></span>
<span data-ttu-id="9f4f2-124">Nazwa agenta.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-124">The agent name.</span></span>

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

### <span data-ttu-id="9f4f2-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-125">-AgentServerName</span></span>
<span data-ttu-id="9f4f2-126">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-126">The server name.</span></span>

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

### <span data-ttu-id="9f4f2-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-127">-DatabaseName</span></span>
<span data-ttu-id="9f4f2-128">Nazwa docelowa bazy danych</span><span class="sxs-lookup"><span data-stu-id="9f4f2-128">Database Target Name</span></span>

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

### <span data-ttu-id="9f4f2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f4f2-129">-DefaultProfile</span></span>
<span data-ttu-id="9f4f2-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f4f2-131">-PochylićPoolName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-131">-ElasticPoolName</span></span>
<span data-ttu-id="9f4f2-132">Elastyczna nazwa docelowa puli</span><span class="sxs-lookup"><span data-stu-id="9f4f2-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="9f4f2-133">— Wyklucz</span><span class="sxs-lookup"><span data-stu-id="9f4f2-133">-Exclude</span></span>
<span data-ttu-id="9f4f2-134">Wyklucza wartość docelową.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-134">Excludes a target.</span></span>

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

### <span data-ttu-id="9f4f2-135">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="9f4f2-135">-ParentObject</span></span>
<span data-ttu-id="9f4f2-136">Obiekt grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-136">The target group object.</span></span>

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

### <span data-ttu-id="9f4f2-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9f4f2-137">-ParentResourceId</span></span>
<span data-ttu-id="9f4f2-138">Identyfikator zasobu grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-138">The target group resource id.</span></span>

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

### <span data-ttu-id="9f4f2-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-139">-RefreshCredentialName</span></span>
<span data-ttu-id="9f4f2-140">Refresh Credential Name</span><span class="sxs-lookup"><span data-stu-id="9f4f2-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="9f4f2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-141">-ResourceGroupName</span></span>
<span data-ttu-id="9f4f2-142">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9f4f2-142">Resource Group Name</span></span>

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

### <span data-ttu-id="9f4f2-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-143">-ServerName</span></span>
<span data-ttu-id="9f4f2-144">Nazwa docelowa serwera</span><span class="sxs-lookup"><span data-stu-id="9f4f2-144">Server Target Name</span></span>

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

### <span data-ttu-id="9f4f2-145">-SowaMapName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-145">-ShardMapName</span></span>
<span data-ttu-id="9f4f2-146">Sowąd mapową nazwę docelową</span><span class="sxs-lookup"><span data-stu-id="9f4f2-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="9f4f2-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="9f4f2-147">-TargetGroupName</span></span>
<span data-ttu-id="9f4f2-148">Nazwa grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-148">The target group name.</span></span>

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

### <span data-ttu-id="9f4f2-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f4f2-149">-Confirm</span></span>
<span data-ttu-id="9f4f2-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f4f2-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f4f2-151">-WhatIf</span></span>
<span data-ttu-id="9f4f2-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f4f2-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f4f2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f4f2-154">CommonParameters</span></span>
<span data-ttu-id="9f4f2-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f4f2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f4f2-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f4f2-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f4f2-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f4f2-157">INPUTS</span></span>

### <span data-ttu-id="9f4f2-158">Microsoft.Azure.Commands.Sql.NajbłędszaJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="9f4f2-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="9f4f2-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f4f2-159">OUTPUTS</span></span>

### <span data-ttu-id="9f4f2-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="9f4f2-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="9f4f2-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9f4f2-161">NOTES</span></span>

## <span data-ttu-id="9f4f2-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f4f2-162">RELATED LINKS</span></span>
