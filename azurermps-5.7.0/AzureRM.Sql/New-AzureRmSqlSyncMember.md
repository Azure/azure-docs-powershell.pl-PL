---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: d2df78cc4cbf7bea7918653e310193bf013d7495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547863"
---
# <span data-ttu-id="7a211-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7a211-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="7a211-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a211-102">SYNOPSIS</span></span>
<span data-ttu-id="7a211-103">Tworzy członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="7a211-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a211-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a211-104">SYNTAX</span></span>

### <span data-ttu-id="7a211-105">AzureSqlDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7a211-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a211-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="7a211-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a211-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="7a211-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a211-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7a211-108">DESCRIPTION</span></span>
<span data-ttu-id="7a211-109">Polecenie cmdlet **New-AzureRmSqlSyncMember** umożliwia utworzenie członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="7a211-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="7a211-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a211-110">EXAMPLES</span></span>

### <span data-ttu-id="7a211-111">Przykład 1. Utwórz element synchronizacji dla bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="7a211-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="7a211-112">To polecenie tworzy element synchronizacji dla bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="7a211-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="7a211-113">Przykład 2: Tworzenie członka synchronizacji dla lokalnej bazy danych programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="7a211-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="7a211-114">To polecenie tworzy element synchronizacji dla lokalnej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="7a211-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="7a211-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a211-115">PARAMETERS</span></span>

### <span data-ttu-id="7a211-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a211-116">-DatabaseName</span></span>
<span data-ttu-id="7a211-117">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="7a211-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a211-118">-DefaultProfile</span></span>
<span data-ttu-id="7a211-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7a211-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="7a211-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="7a211-121">Poświadczenia (nazwa użytkownika i hasło) bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7a211-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a211-122">-MemberDatabaseName</span></span>
<span data-ttu-id="7a211-123">Nazwa bazy danych usługi Azure SQL Database bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="7a211-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="7a211-124">-MemberDatabaseType</span></span>
<span data-ttu-id="7a211-125">Typ bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="7a211-125">The database type of the member database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="7a211-126">-MemberServerName</span></span>
<span data-ttu-id="7a211-127">Nazwa programu Azure SQL Server bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="7a211-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a211-128">-Name</span></span>
<span data-ttu-id="7a211-129">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7a211-129">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a211-130">-ResourceGroupName</span></span>
<span data-ttu-id="7a211-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a211-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-132">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7a211-132">-ServerName</span></span>
<span data-ttu-id="7a211-133">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7a211-133">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="7a211-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="7a211-135">Identyfikator bazy danych programu SQL Server połączonej z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7a211-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="7a211-136">-SyncAgentName</span></span>
<span data-ttu-id="7a211-137">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7a211-137">The name of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a211-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="7a211-139">Nazwa grupy zasobów, w której znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7a211-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="7a211-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="7a211-141">Identyfikator zasobu agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7a211-141">The resource ID of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="7a211-142">-SyncAgentServerName</span></span>
<span data-ttu-id="7a211-143">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7a211-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="7a211-144">-SyncDirection</span></span>
<span data-ttu-id="7a211-145">Kierunek synchronizacji tego członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7a211-145">The sync direction of this sync member.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7a211-146">-SyncGroupName</span></span>
<span data-ttu-id="7a211-147">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7a211-147">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a211-148">-Confirm</span></span>
<span data-ttu-id="7a211-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a211-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a211-150">-WhatIf</span></span>
<span data-ttu-id="7a211-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a211-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a211-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a211-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a211-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a211-153">CommonParameters</span></span>
<span data-ttu-id="7a211-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a211-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a211-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a211-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a211-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a211-156">INPUTS</span></span>

### <span data-ttu-id="7a211-157">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7a211-157">None</span></span>
<span data-ttu-id="7a211-158">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7a211-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a211-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a211-159">OUTPUTS</span></span>

### <span data-ttu-id="7a211-160">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="7a211-160">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="7a211-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a211-161">NOTES</span></span>

## <span data-ttu-id="7a211-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a211-162">RELATED LINKS</span></span>

[<span data-ttu-id="7a211-163">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7a211-163">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="7a211-164">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7a211-164">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="7a211-165">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7a211-165">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

