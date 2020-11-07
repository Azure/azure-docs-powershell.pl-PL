---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: 8b0f67aa8e85ce9123b515f12c2e3a7da84f860d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886881"
---
# <span data-ttu-id="979e6-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="979e6-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="979e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="979e6-102">SYNOPSIS</span></span>
<span data-ttu-id="979e6-103">Zwraca informacje o elementach członkowskich synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="979e6-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="979e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="979e6-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="979e6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="979e6-105">DESCRIPTION</span></span>
<span data-ttu-id="979e6-106">Polecenie cmdlet **Get-AzSqlSyncMember** zwraca informacje o co najmniej jednym członku synchronizacji bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="979e6-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="979e6-107">Określ nazwę członka synchronizacji, aby wyświetlić informacje dotyczące tylko tego członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="979e6-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="979e6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="979e6-108">EXAMPLES</span></span>

### <span data-ttu-id="979e6-109">Przykład 1: Pobierz wszystkie wystąpienia elementu członkowskiego synchronizacji platformy Azure SQL przypisanego do grupy synchronizacji</span><span class="sxs-lookup"><span data-stu-id="979e6-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="979e6-110">To polecenie pobiera informacje o składniku synchronizacji bazy danych SQL Azure przypisanym do grupy synchronizacji SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="979e6-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="979e6-111">Przykład 2: uzyskiwanie informacji o członku synchronizacji bazy danych SQL Azure Database</span><span class="sxs-lookup"><span data-stu-id="979e6-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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
SyncState                   : Good
```

<span data-ttu-id="979e6-112">To polecenie pobiera informacje o członku synchronizacji bazy danych Azure SQL Database o nazwie "SyncMember01".</span><span class="sxs-lookup"><span data-stu-id="979e6-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="979e6-113">Przykład 3: Pobierz wszystkie wystąpienia elementu członkowskiego synchronizacji platformy Azure SQL przypisanego do grupy synchronizacji przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="979e6-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember*" | Format-List
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
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="979e6-114">To polecenie pobiera informacje o członku synchronizacji bazy danych SQL Azure przypisanym do grupy synchronizacji SyncGroup01, która rozpoczyna się od "SyncMember".</span><span class="sxs-lookup"><span data-stu-id="979e6-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="979e6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="979e6-115">PARAMETERS</span></span>

### <span data-ttu-id="979e6-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="979e6-116">-DatabaseName</span></span>
<span data-ttu-id="979e6-117">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="979e6-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="979e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="979e6-118">-DefaultProfile</span></span>
<span data-ttu-id="979e6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="979e6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="979e6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="979e6-120">-Name</span></span>
<span data-ttu-id="979e6-121">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="979e6-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="979e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="979e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="979e6-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="979e6-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="979e6-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="979e6-124">-ServerName</span></span>
<span data-ttu-id="979e6-125">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="979e6-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="979e6-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="979e6-126">-SyncGroupName</span></span>
<span data-ttu-id="979e6-127">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="979e6-127">The sync group name.</span></span>

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

### <span data-ttu-id="979e6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="979e6-128">CommonParameters</span></span>
<span data-ttu-id="979e6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="979e6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="979e6-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="979e6-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="979e6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="979e6-131">INPUTS</span></span>

### <span data-ttu-id="979e6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="979e6-132">System.String</span></span>

## <span data-ttu-id="979e6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="979e6-133">OUTPUTS</span></span>

### <span data-ttu-id="979e6-134">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="979e6-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="979e6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="979e6-135">NOTES</span></span>

## <span data-ttu-id="979e6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="979e6-136">RELATED LINKS</span></span>

[<span data-ttu-id="979e6-137">Nowe — AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="979e6-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="979e6-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="979e6-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="979e6-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="979e6-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

