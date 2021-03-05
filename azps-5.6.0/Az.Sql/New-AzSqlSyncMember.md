---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: c26cb74f1d9f9c30e63bb39ec7668216a5f3a297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961425"
---
# <span data-ttu-id="c2c54-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c2c54-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="c2c54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2c54-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c54-103">Tworzy członka synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="c2c54-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="c2c54-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2c54-104">SYNTAX</span></span>

### <span data-ttu-id="c2c54-105">AzureSqlDatabase (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c2c54-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c54-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="c2c54-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c54-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="c2c54-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2c54-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2c54-108">DESCRIPTION</span></span>
<span data-ttu-id="c2c54-109">Polecenie **cmdlet New-AzSqlSyncMember** tworzy członka synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="c2c54-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="c2c54-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2c54-110">EXAMPLES</span></span>

### <span data-ttu-id="c2c54-111">Przykład 1. Tworzenie członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="c2c54-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "AzureSqlDatabase" -MemberServerName "memberServer01.full.dns.name" -MemberDatabaseName "memberDatabase01" -MemberDatabaseCredential $credential | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="c2c54-112">To polecenie tworzy członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="c2c54-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="c2c54-113">Przykład 2. Tworzenie członka synchronizacji dla lokalnej bazy danych programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="c2c54-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "SqlServerDatabase" -SqlServerDatabaseId "dbId" -syncAgentResourceGroupName "syncAgentResourceGroupName" -syncAgentServerName "syncAgentServerName" 
-syncAgentDatabaseName "syncAgentDatabaseName" -syncAgentName "agentName" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : /subscriptions/{subscriptionId}/resourceGroups/{syncAgentResourceGroupName}/servers/{syncAgentServerName}/syncAgents/{syncAgentId}
SqlServerDatabaseId         : dbId
MemberServerName            : 
MemberDatabaseName          : 
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="c2c54-114">To polecenie tworzy członka synchronizacji lokalnej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="c2c54-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="c2c54-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2c54-115">PARAMETERS</span></span>

### <span data-ttu-id="c2c54-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2c54-116">-DatabaseName</span></span>
<span data-ttu-id="c2c54-117">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="c2c54-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c54-118">-DefaultProfile</span></span>
<span data-ttu-id="c2c54-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c2c54-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2c54-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="c2c54-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="c2c54-121">Poświadczenia (nazwa użytkownika i hasło) bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="c2c54-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2c54-122">-MemberDatabaseName</span></span>
<span data-ttu-id="c2c54-123">Nazwa bazy danych Azure SQL Database członka bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c2c54-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="c2c54-124">-MemberDatabaseType</span></span>
<span data-ttu-id="c2c54-125">Typ bazy danych członka bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c2c54-125">The database type of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="c2c54-126">-MemberServerName</span></span>
<span data-ttu-id="c2c54-127">Nazwa programu Azure SQL Server bazy danych członków.</span><span class="sxs-lookup"><span data-stu-id="c2c54-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c2c54-128">-Name</span></span>
<span data-ttu-id="c2c54-129">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c2c54-129">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c54-130">-ResourceGroupName</span></span>
<span data-ttu-id="c2c54-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2c54-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c2c54-132">-ServerName</span></span>
<span data-ttu-id="c2c54-133">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c2c54-133">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="c2c54-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="c2c54-135">Identyfikator bazy danych programu SQL Server, która jest połączona przez agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c2c54-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="c2c54-136">-SyncAgentName</span></span>
<span data-ttu-id="c2c54-137">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c2c54-137">The name of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c54-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="c2c54-139">Nazwa grupy zasobów, w której znajduje się agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c2c54-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="c2c54-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="c2c54-141">Identyfikator zasobu agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c2c54-141">The resource ID of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="c2c54-142">-SyncAgentServerName</span></span>
<span data-ttu-id="c2c54-143">Nazwa serwera Azure SQL Server, w którym znajduje się agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c2c54-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="c2c54-144">-SyncDirection</span></span>
<span data-ttu-id="c2c54-145">Kierunek synchronizacji tego członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c2c54-145">The sync direction of this sync member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c54-146">-SyncGroupName</span></span>
<span data-ttu-id="c2c54-147">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c2c54-147">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="c2c54-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="c2c54-149">Identyfikator zasobu dla bazy danych członka synchronizacji, używany w przypadku ustawienia UsePrivateLinkConnection na wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="c2c54-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="c2c54-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c2c54-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="c2c54-151">Użyj prywatnego połączenia linku podczas nawiązywania połączenia z tym członkiem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c2c54-151">Use a private link connection when connecting to this sync member.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2c54-152">-Confirm</span></span>
<span data-ttu-id="c2c54-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2c54-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2c54-154">-WhatIf</span></span>
<span data-ttu-id="c2c54-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2c54-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2c54-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c2c54-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c54-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c54-157">CommonParameters</span></span>
<span data-ttu-id="c2c54-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c54-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c54-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2c54-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c54-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2c54-160">INPUTS</span></span>

### <span data-ttu-id="c2c54-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c2c54-161">System.String</span></span>

## <span data-ttu-id="c2c54-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2c54-162">OUTPUTS</span></span>

### <span data-ttu-id="c2c54-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="c2c54-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="c2c54-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2c54-164">NOTES</span></span>

## <span data-ttu-id="c2c54-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2c54-165">RELATED LINKS</span></span>

[<span data-ttu-id="c2c54-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c2c54-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="c2c54-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c2c54-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="c2c54-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c2c54-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

