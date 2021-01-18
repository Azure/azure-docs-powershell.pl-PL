---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: f7fc860711c5037e6ce6390f9fb7d79ddfa7d6ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498302"
---
# <span data-ttu-id="9ec2e-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="9ec2e-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="9ec2e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ec2e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec2e-103">Tworzy członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="9ec2e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ec2e-104">SYNTAX</span></span>

### <span data-ttu-id="9ec2e-105">AzureSqlDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ec2e-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec2e-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="9ec2e-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec2e-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="9ec2e-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ec2e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9ec2e-108">DESCRIPTION</span></span>
<span data-ttu-id="9ec2e-109">Polecenie cmdlet **New-AzSqlSyncMember** umożliwia utworzenie członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="9ec2e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ec2e-110">EXAMPLES</span></span>

### <span data-ttu-id="9ec2e-111">Przykład 1. Utwórz element synchronizacji dla bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="9ec2e-112">To polecenie tworzy element synchronizacji dla bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="9ec2e-113">Przykład 2: Tworzenie członka synchronizacji dla lokalnej bazy danych programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="9ec2e-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="9ec2e-114">To polecenie tworzy element synchronizacji dla lokalnej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="9ec2e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ec2e-115">PARAMETERS</span></span>

### <span data-ttu-id="9ec2e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9ec2e-116">-DatabaseName</span></span>
<span data-ttu-id="9ec2e-117">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9ec2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec2e-118">-DefaultProfile</span></span>
<span data-ttu-id="9ec2e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9ec2e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ec2e-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="9ec2e-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="9ec2e-121">Poświadczenia (nazwa użytkownika i hasło) bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9ec2e-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="9ec2e-122">-MemberDatabaseName</span></span>
<span data-ttu-id="9ec2e-123">Nazwa bazy danych usługi Azure SQL Database bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="9ec2e-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="9ec2e-124">-MemberDatabaseType</span></span>
<span data-ttu-id="9ec2e-125">Typ bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="9ec2e-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="9ec2e-126">-MemberServerName</span></span>
<span data-ttu-id="9ec2e-127">Nazwa programu Azure SQL Server bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="9ec2e-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ec2e-128">-Name</span></span>
<span data-ttu-id="9ec2e-129">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-129">The sync member name.</span></span>

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

### <span data-ttu-id="9ec2e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec2e-130">-ResourceGroupName</span></span>
<span data-ttu-id="9ec2e-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="9ec2e-132">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="9ec2e-132">-ServerName</span></span>
<span data-ttu-id="9ec2e-133">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9ec2e-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="9ec2e-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="9ec2e-135">Identyfikator bazy danych programu SQL Server połączonej z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="9ec2e-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="9ec2e-136">-SyncAgentName</span></span>
<span data-ttu-id="9ec2e-137">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="9ec2e-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec2e-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="9ec2e-139">Nazwa grupy zasobów, w której znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="9ec2e-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="9ec2e-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="9ec2e-141">Identyfikator zasobu agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="9ec2e-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="9ec2e-142">-SyncAgentServerName</span></span>
<span data-ttu-id="9ec2e-143">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="9ec2e-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="9ec2e-144">-SyncDirection</span></span>
<span data-ttu-id="9ec2e-145">Kierunek synchronizacji tego członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="9ec2e-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec2e-146">-SyncGroupName</span></span>
<span data-ttu-id="9ec2e-147">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-147">The sync group name.</span></span>

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

### <span data-ttu-id="9ec2e-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="9ec2e-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="9ec2e-149">Identyfikator zasobu dla bazy danych elementu członkowskiego synchronizacji, używana, jeśli UsePrivateLinkConnection ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="9ec2e-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="9ec2e-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="9ec2e-151">Połącz się z tym członkiem synchronizacji przy użyciu połączenia prywatnego.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-151">Use a private link connection when connecting to this sync member.</span></span>

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

### <span data-ttu-id="9ec2e-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ec2e-152">-Confirm</span></span>
<span data-ttu-id="9ec2e-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ec2e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ec2e-154">-WhatIf</span></span>
<span data-ttu-id="9ec2e-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ec2e-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ec2e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec2e-157">CommonParameters</span></span>
<span data-ttu-id="9ec2e-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec2e-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec2e-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ec2e-160">INPUTS</span></span>

### <span data-ttu-id="9ec2e-161">System. String</span><span class="sxs-lookup"><span data-stu-id="9ec2e-161">System.String</span></span>

## <span data-ttu-id="9ec2e-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ec2e-162">OUTPUTS</span></span>

### <span data-ttu-id="9ec2e-163">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="9ec2e-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="9ec2e-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ec2e-164">NOTES</span></span>

## <span data-ttu-id="9ec2e-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ec2e-165">RELATED LINKS</span></span>

[<span data-ttu-id="9ec2e-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="9ec2e-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="9ec2e-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="9ec2e-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="9ec2e-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="9ec2e-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

