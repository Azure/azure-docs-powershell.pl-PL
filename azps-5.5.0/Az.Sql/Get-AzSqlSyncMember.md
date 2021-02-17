---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178435"
---
# <span data-ttu-id="35732-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="35732-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="35732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35732-102">SYNOPSIS</span></span>
<span data-ttu-id="35732-103">Zwraca informacje o członkach synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="35732-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="35732-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35732-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35732-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="35732-105">DESCRIPTION</span></span>
<span data-ttu-id="35732-106">Polecenie **cmdlet Get-AzSqlSyncMember** zwraca informacje dotyczące co najmniej jednego członka synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="35732-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="35732-107">Określ nazwę członka synchronizacji, aby wyświetlić informacje tylko dla tego członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="35732-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="35732-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35732-108">EXAMPLES</span></span>

### <span data-ttu-id="35732-109">Przykład 1. Uzyskiwanie wszystkich wystąpień programu Azure SQL Sync Member przypisanego do grupy synchronizacji</span><span class="sxs-lookup"><span data-stu-id="35732-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
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

<span data-ttu-id="35732-110">To polecenie pobiera informacje o wszystkich członkach synchronizacji usługi Azure SQL Database przypisanych do grupy synchronizacji SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="35732-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="35732-111">Przykład 2. Uzyskiwanie informacji na temat członka synchronizacji bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="35732-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
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

<span data-ttu-id="35732-112">To polecenie pobiera informacje o członce synchronizacji bazy danych Azure SQL o nazwie "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="35732-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="35732-113">Przykład 3. Uzyskiwanie wszystkich wystąpień programu Azure SQL Sync Member przypisanego do grupy synchronizacji przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="35732-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
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

<span data-ttu-id="35732-114">To polecenie pobiera informacje o wszystkich członkach synchronizacji usługi Azure SQL Database przypisanych do grupy synchronizacji SyncGroup01, których nazwa rozpoczyna się od "SyncMember".</span><span class="sxs-lookup"><span data-stu-id="35732-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="35732-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35732-115">PARAMETERS</span></span>

### <span data-ttu-id="35732-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="35732-116">-DatabaseName</span></span>
<span data-ttu-id="35732-117">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="35732-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="35732-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35732-118">-DefaultProfile</span></span>
<span data-ttu-id="35732-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="35732-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35732-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="35732-120">-Name</span></span>
<span data-ttu-id="35732-121">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="35732-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35732-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35732-122">-ResourceGroupName</span></span>
<span data-ttu-id="35732-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35732-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="35732-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="35732-124">-ServerName</span></span>
<span data-ttu-id="35732-125">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35732-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="35732-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="35732-126">-SyncGroupName</span></span>
<span data-ttu-id="35732-127">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="35732-127">The sync group name.</span></span>

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

### <span data-ttu-id="35732-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35732-128">CommonParameters</span></span>
<span data-ttu-id="35732-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35732-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35732-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35732-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35732-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35732-131">INPUTS</span></span>

### <span data-ttu-id="35732-132">System.String</span><span class="sxs-lookup"><span data-stu-id="35732-132">System.String</span></span>

## <span data-ttu-id="35732-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35732-133">OUTPUTS</span></span>

### <span data-ttu-id="35732-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="35732-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="35732-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35732-135">NOTES</span></span>

## <span data-ttu-id="35732-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35732-136">RELATED LINKS</span></span>

[<span data-ttu-id="35732-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="35732-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="35732-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="35732-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="35732-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="35732-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

