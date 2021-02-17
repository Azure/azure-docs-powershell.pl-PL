---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 5846435df4921e425e12e908539849fda0bd2472
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399536"
---
# <span data-ttu-id="a4c79-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4c79-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="a4c79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4c79-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c79-103">Tworzy członka synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a4c79-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="a4c79-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4c79-104">SYNTAX</span></span>

### <span data-ttu-id="a4c79-105">AzureSqlDatabase (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a4c79-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4c79-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="a4c79-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4c79-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="a4c79-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4c79-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4c79-108">DESCRIPTION</span></span>
<span data-ttu-id="a4c79-109">Polecenie **cmdlet New-AzSqlSyncMember** tworzy członka synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a4c79-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="a4c79-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4c79-110">EXAMPLES</span></span>

### <span data-ttu-id="a4c79-111">Przykład 1. Tworzenie członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a4c79-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="a4c79-112">To polecenie tworzy członka synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a4c79-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="a4c79-113">Przykład 2. Tworzenie członka synchronizacji dla lokalnej bazy danych programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="a4c79-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="a4c79-114">To polecenie tworzy członka synchronizacji lokalnej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a4c79-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="a4c79-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4c79-115">PARAMETERS</span></span>

### <span data-ttu-id="a4c79-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4c79-116">-DatabaseName</span></span>
<span data-ttu-id="a4c79-117">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a4c79-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a4c79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c79-118">-DefaultProfile</span></span>
<span data-ttu-id="a4c79-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a4c79-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4c79-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="a4c79-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="a4c79-121">Poświadczenia (nazwa użytkownika i hasło) bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a4c79-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a4c79-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4c79-122">-MemberDatabaseName</span></span>
<span data-ttu-id="a4c79-123">Nazwa bazy danych Azure SQL Database członka bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a4c79-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="a4c79-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="a4c79-124">-MemberDatabaseType</span></span>
<span data-ttu-id="a4c79-125">Typ bazy danych członka bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a4c79-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="a4c79-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="a4c79-126">-MemberServerName</span></span>
<span data-ttu-id="a4c79-127">Nazwa programu Azure SQL Server bazy danych członków.</span><span class="sxs-lookup"><span data-stu-id="a4c79-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="a4c79-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a4c79-128">-Name</span></span>
<span data-ttu-id="a4c79-129">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a4c79-129">The sync member name.</span></span>

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

### <span data-ttu-id="a4c79-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c79-130">-ResourceGroupName</span></span>
<span data-ttu-id="a4c79-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4c79-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4c79-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4c79-132">-ServerName</span></span>
<span data-ttu-id="a4c79-133">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4c79-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a4c79-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="a4c79-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="a4c79-135">Identyfikator bazy danych programu SQL Server, która jest połączona przez agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a4c79-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="a4c79-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="a4c79-136">-SyncAgentName</span></span>
<span data-ttu-id="a4c79-137">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a4c79-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="a4c79-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c79-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="a4c79-139">Nazwa grupy zasobów, w której znajduje się agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a4c79-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="a4c79-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="a4c79-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="a4c79-141">Identyfikator zasobu agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a4c79-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="a4c79-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="a4c79-142">-SyncAgentServerName</span></span>
<span data-ttu-id="a4c79-143">Nazwa serwera Azure SQL Server, pod którym znajduje się agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a4c79-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="a4c79-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="a4c79-144">-SyncDirection</span></span>
<span data-ttu-id="a4c79-145">Kierunek synchronizacji tego członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a4c79-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="a4c79-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c79-146">-SyncGroupName</span></span>
<span data-ttu-id="a4c79-147">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a4c79-147">The sync group name.</span></span>

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

### <span data-ttu-id="a4c79-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4c79-148">-Confirm</span></span>
<span data-ttu-id="a4c79-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4c79-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4c79-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4c79-150">-WhatIf</span></span>
<span data-ttu-id="a4c79-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4c79-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4c79-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a4c79-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4c79-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c79-153">CommonParameters</span></span>
<span data-ttu-id="a4c79-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c79-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c79-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4c79-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c79-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4c79-156">INPUTS</span></span>

### <span data-ttu-id="a4c79-157">System.String</span><span class="sxs-lookup"><span data-stu-id="a4c79-157">System.String</span></span>

## <span data-ttu-id="a4c79-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4c79-158">OUTPUTS</span></span>

### <span data-ttu-id="a4c79-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="a4c79-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="a4c79-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4c79-160">NOTES</span></span>

## <span data-ttu-id="a4c79-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4c79-161">RELATED LINKS</span></span>

[<span data-ttu-id="a4c79-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4c79-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)


[<span data-ttu-id="a4c79-163">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4c79-163">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

