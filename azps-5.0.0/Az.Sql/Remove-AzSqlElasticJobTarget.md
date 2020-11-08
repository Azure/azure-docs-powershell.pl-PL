---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232942"
---
# <span data-ttu-id="55fef-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="55fef-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="55fef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55fef-102">SYNOPSIS</span></span>
<span data-ttu-id="55fef-103">Usuwa element docelowy z grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="55fef-103">Removes the target from the target group</span></span>

## <span data-ttu-id="55fef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55fef-104">SYNTAX</span></span>

### <span data-ttu-id="55fef-105">SQLDatabase (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="55fef-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55fef-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="55fef-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55fef-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="55fef-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55fef-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="55fef-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55fef-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="55fef-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55fef-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="55fef-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55fef-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="55fef-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55fef-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="55fef-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55fef-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="55fef-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55fef-114">Opis</span><span class="sxs-lookup"><span data-stu-id="55fef-114">DESCRIPTION</span></span>
<span data-ttu-id="55fef-115">Polecenie cmdlet Remove-AzSqlElasticJobTarget usuwa zasób docelowy do grupy docelowej</span><span class="sxs-lookup"><span data-stu-id="55fef-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="55fef-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55fef-116">EXAMPLES</span></span>

### <span data-ttu-id="55fef-117">Przykład 1: usuwanie obiektu docelowego serwera</span><span class="sxs-lookup"><span data-stu-id="55fef-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="55fef-118">Przykład 2: usuwanie obiektu docelowego bazy danych</span><span class="sxs-lookup"><span data-stu-id="55fef-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="55fef-119">Przykład 3: usuwanie elementu docelowego puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="55fef-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="55fef-120">Przykład 4: usuwanie obiektu docelowego mapy Shard</span><span class="sxs-lookup"><span data-stu-id="55fef-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="55fef-121">Usuwa element docelowy (serwer, elastyczna Pula, baza danych i mapa Shard) z grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="55fef-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="55fef-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55fef-122">PARAMETERS</span></span>

### <span data-ttu-id="55fef-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="55fef-123">-AgentName</span></span>
<span data-ttu-id="55fef-124">Nazwa agenta bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="55fef-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="55fef-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="55fef-125">-AgentServerName</span></span>
<span data-ttu-id="55fef-126">Nazwa serwera agenta bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="55fef-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="55fef-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="55fef-127">-DatabaseName</span></span>
<span data-ttu-id="55fef-128">Nazwa celu bazy danych</span><span class="sxs-lookup"><span data-stu-id="55fef-128">Database Target Name</span></span>

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

### <span data-ttu-id="55fef-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fef-129">-DefaultProfile</span></span>
<span data-ttu-id="55fef-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55fef-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55fef-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="55fef-131">-ElasticPoolName</span></span>
<span data-ttu-id="55fef-132">Nazwa docelowa puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="55fef-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="55fef-133">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="55fef-133">-ParentObject</span></span>
<span data-ttu-id="55fef-134">Obiekt grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="55fef-134">The target group object.</span></span>

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

### <span data-ttu-id="55fef-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="55fef-135">-ParentResourceId</span></span>
<span data-ttu-id="55fef-136">Identyfikator zasobu grupy docelowej.</span><span class="sxs-lookup"><span data-stu-id="55fef-136">The target group resource id.</span></span>

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

### <span data-ttu-id="55fef-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="55fef-137">-RefreshCredentialName</span></span>
<span data-ttu-id="55fef-138">Odśwież nazwę poświadczenia</span><span class="sxs-lookup"><span data-stu-id="55fef-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="55fef-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55fef-139">-ResourceGroupName</span></span>
<span data-ttu-id="55fef-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="55fef-140">Resource Group Name</span></span>

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

### <span data-ttu-id="55fef-141">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="55fef-141">-ServerName</span></span>
<span data-ttu-id="55fef-142">Nazwa docelowa serwera</span><span class="sxs-lookup"><span data-stu-id="55fef-142">Server Target Name</span></span>

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

### <span data-ttu-id="55fef-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="55fef-143">-ShardMapName</span></span>
<span data-ttu-id="55fef-144">Nazwa docelowa mapy Shard</span><span class="sxs-lookup"><span data-stu-id="55fef-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="55fef-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="55fef-145">-TargetGroupName</span></span>
<span data-ttu-id="55fef-146">Nazwa agenta bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="55fef-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="55fef-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55fef-147">-Confirm</span></span>
<span data-ttu-id="55fef-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55fef-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55fef-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55fef-149">-WhatIf</span></span>
<span data-ttu-id="55fef-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55fef-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55fef-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="55fef-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55fef-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fef-152">CommonParameters</span></span>
<span data-ttu-id="55fef-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55fef-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fef-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55fef-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fef-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55fef-155">INPUTS</span></span>

### <span data-ttu-id="55fef-156">Microsoft. Azure. Commands. SQL. ElasticJobs. model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="55fef-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="55fef-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55fef-157">OUTPUTS</span></span>

### <span data-ttu-id="55fef-158">Microsoft. Azure. Management. SQL. MODELES. JobTarget</span><span class="sxs-lookup"><span data-stu-id="55fef-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="55fef-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55fef-159">NOTES</span></span>

## <span data-ttu-id="55fef-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55fef-160">RELATED LINKS</span></span>
