---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: bd828a88b870174b870d3acb963cdcb3b3c58ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527226"
---
# <span data-ttu-id="12327-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="12327-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="12327-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12327-102">SYNOPSIS</span></span>
<span data-ttu-id="12327-103">Zwraca informacje o elementach członkowskich synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="12327-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12327-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12327-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12327-105">Opis</span><span class="sxs-lookup"><span data-stu-id="12327-105">DESCRIPTION</span></span>
<span data-ttu-id="12327-106">Polecenie cmdlet **Get-AzureRmSqlSyncMember** zwraca informacje o co najmniej jednym członku synchronizacji bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="12327-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="12327-107">Określ nazwę członka synchronizacji, aby wyświetlić informacje dotyczące tylko tego członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="12327-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="12327-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12327-108">EXAMPLES</span></span>

### <span data-ttu-id="12327-109">Przykład 1: Pobierz wszystkie wystąpienia elementu członkowskiego synchronizacji platformy Azure SQL przypisanego do grupy synchronizacji</span><span class="sxs-lookup"><span data-stu-id="12327-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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

<span data-ttu-id="12327-110">To polecenie pobiera informacje o składniku synchronizacji bazy danych SQL Azure przypisanym do grupy synchronizacji SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="12327-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="12327-111">Przykład 2: uzyskiwanie informacji o członku synchronizacji bazy danych SQL Azure Database</span><span class="sxs-lookup"><span data-stu-id="12327-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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

<span data-ttu-id="12327-112">To polecenie pobiera informacje o członku synchronizacji bazy danych Azure SQL Database o nazwie "SyncMember01".</span><span class="sxs-lookup"><span data-stu-id="12327-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="12327-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12327-113">PARAMETERS</span></span>

### <span data-ttu-id="12327-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="12327-114">-DatabaseName</span></span>
<span data-ttu-id="12327-115">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="12327-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="12327-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12327-116">-Name</span></span>
<span data-ttu-id="12327-117">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="12327-117">The sync member name.</span></span>

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

### <span data-ttu-id="12327-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12327-118">-ResourceGroupName</span></span>
<span data-ttu-id="12327-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12327-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="12327-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="12327-120">-ServerName</span></span>
<span data-ttu-id="12327-121">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="12327-121">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="12327-122">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="12327-122">-SyncGroupName</span></span>
<span data-ttu-id="12327-123">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="12327-123">The sync group name.</span></span>

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

### <span data-ttu-id="12327-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12327-124">-DefaultProfile</span></span>
<span data-ttu-id="12327-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12327-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12327-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12327-126">CommonParameters</span></span>
<span data-ttu-id="12327-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12327-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12327-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12327-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12327-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12327-129">INPUTS</span></span>

## <span data-ttu-id="12327-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12327-130">OUTPUTS</span></span>

### <span data-ttu-id="12327-131">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="12327-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="12327-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12327-132">NOTES</span></span>

## <span data-ttu-id="12327-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12327-133">RELATED LINKS</span></span>

[<span data-ttu-id="12327-134">Nowe — AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="12327-134">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="12327-135">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="12327-135">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="12327-136">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="12327-136">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

