---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: a779217b67cc73f25223661ae8671b4588a8cd2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547343"
---
# <span data-ttu-id="26c83-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="26c83-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="26c83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26c83-102">SYNOPSIS</span></span>
<span data-ttu-id="26c83-103">Tworzy członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="26c83-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26c83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26c83-104">SYNTAX</span></span>

### <span data-ttu-id="26c83-105">AzureSqlDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26c83-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c83-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="26c83-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c83-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="26c83-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26c83-108">Opis</span><span class="sxs-lookup"><span data-stu-id="26c83-108">DESCRIPTION</span></span>
<span data-ttu-id="26c83-109">Polecenie cmdlet **New-AzureRmSqlSyncMember** umożliwia utworzenie członka synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="26c83-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="26c83-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26c83-110">EXAMPLES</span></span>

### <span data-ttu-id="26c83-111">Przykład 1. Utwórz element synchronizacji dla bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="26c83-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="26c83-112">To polecenie tworzy element synchronizacji dla bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="26c83-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="26c83-113">Przykład 2: Tworzenie członka synchronizacji dla lokalnej bazy danych programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="26c83-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="26c83-114">To polecenie tworzy element synchronizacji dla lokalnej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="26c83-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="26c83-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26c83-115">PARAMETERS</span></span>

### <span data-ttu-id="26c83-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26c83-116">-DatabaseName</span></span>
<span data-ttu-id="26c83-117">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="26c83-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="26c83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c83-118">-DefaultProfile</span></span>
<span data-ttu-id="26c83-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="26c83-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26c83-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="26c83-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="26c83-121">Poświadczenia (nazwa użytkownika i hasło) bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="26c83-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="26c83-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="26c83-122">-MemberDatabaseName</span></span>
<span data-ttu-id="26c83-123">Nazwa bazy danych usługi Azure SQL Database bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="26c83-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="26c83-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="26c83-124">-MemberDatabaseType</span></span>
<span data-ttu-id="26c83-125">Typ bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="26c83-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="26c83-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="26c83-126">-MemberServerName</span></span>
<span data-ttu-id="26c83-127">Nazwa programu Azure SQL Server bazy danych członka.</span><span class="sxs-lookup"><span data-stu-id="26c83-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="26c83-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26c83-128">-Name</span></span>
<span data-ttu-id="26c83-129">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="26c83-129">The sync member name.</span></span>

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

### <span data-ttu-id="26c83-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26c83-130">-ResourceGroupName</span></span>
<span data-ttu-id="26c83-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26c83-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="26c83-132">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="26c83-132">-ServerName</span></span>
<span data-ttu-id="26c83-133">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="26c83-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="26c83-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="26c83-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="26c83-135">Identyfikator bazy danych programu SQL Server połączonej z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="26c83-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="26c83-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="26c83-136">-SyncAgentName</span></span>
<span data-ttu-id="26c83-137">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="26c83-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="26c83-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26c83-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="26c83-139">Nazwa grupy zasobów, w której znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="26c83-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="26c83-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="26c83-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="26c83-141">Identyfikator zasobu agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="26c83-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="26c83-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="26c83-142">-SyncAgentServerName</span></span>
<span data-ttu-id="26c83-143">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="26c83-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="26c83-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="26c83-144">-SyncDirection</span></span>
<span data-ttu-id="26c83-145">Kierunek synchronizacji tego członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="26c83-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="26c83-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="26c83-146">-SyncGroupName</span></span>
<span data-ttu-id="26c83-147">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="26c83-147">The sync group name.</span></span>

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

### <span data-ttu-id="26c83-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26c83-148">-Confirm</span></span>
<span data-ttu-id="26c83-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26c83-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26c83-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26c83-150">-WhatIf</span></span>
<span data-ttu-id="26c83-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26c83-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26c83-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26c83-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26c83-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c83-153">CommonParameters</span></span>
<span data-ttu-id="26c83-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26c83-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c83-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26c83-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c83-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26c83-156">INPUTS</span></span>

### <span data-ttu-id="26c83-157">System. String</span><span class="sxs-lookup"><span data-stu-id="26c83-157">System.String</span></span>

## <span data-ttu-id="26c83-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26c83-158">OUTPUTS</span></span>

### <span data-ttu-id="26c83-159">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="26c83-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="26c83-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26c83-160">NOTES</span></span>

## <span data-ttu-id="26c83-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26c83-161">RELATED LINKS</span></span>

[<span data-ttu-id="26c83-162">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="26c83-162">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="26c83-163">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="26c83-163">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="26c83-164">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="26c83-164">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

