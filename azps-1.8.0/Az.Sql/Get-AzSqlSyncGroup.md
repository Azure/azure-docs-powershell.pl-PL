---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: fdee39766c7793b4d326077e5c18e0328a5e4c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707883"
---
# <span data-ttu-id="21989-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="21989-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="21989-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21989-102">SYNOPSIS</span></span>
<span data-ttu-id="21989-103">Zwraca informacje dotyczące grup synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="21989-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="21989-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21989-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21989-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21989-105">DESCRIPTION</span></span>
<span data-ttu-id="21989-106">Polecenie cmdlet **Get-AzSqlSyncGroup** zwraca informacje o jednej lub większej liczbie grup synchronizacji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="21989-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="21989-107">Określ nazwę grupy synchronizacji, aby wyświetlić informacje dotyczące tylko tej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="21989-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="21989-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21989-108">EXAMPLES</span></span>

### <span data-ttu-id="21989-109">Przykład 1: pobieranie wszystkich wystąpień grupy synchronizacji Azure SQL przypisanej do bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="21989-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="21989-110">To polecenie pobiera informacje o grupach synchronizacji bazy danych SQL Azure przypisanych do bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="21989-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="21989-111">Przykład 2: uzyskiwanie informacji o grupie Synchronizacja bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="21989-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="21989-112">To polecenie pobiera informacje o grupie synchronizowania bazy danych SQL Azure o nazwie "SyncGroup01".</span><span class="sxs-lookup"><span data-stu-id="21989-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="21989-113">Przykład 3: pobieranie wszystkich wystąpień grupy synchronizacji Azure SQL przypisanej do bazy danych SQL Azure przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="21989-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup*" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="21989-114">To polecenie pobiera informacje o grupach synchronizacji bazy danych SQL Azure przypisanych do bazy danych SQL Azure, która rozpoczyna się od "synch Group".</span><span class="sxs-lookup"><span data-stu-id="21989-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="21989-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21989-115">PARAMETERS</span></span>

### <span data-ttu-id="21989-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="21989-116">-DatabaseName</span></span>
<span data-ttu-id="21989-117">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="21989-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="21989-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21989-118">-DefaultProfile</span></span>
<span data-ttu-id="21989-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="21989-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21989-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21989-120">-Name</span></span>
<span data-ttu-id="21989-121">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="21989-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="21989-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21989-122">-ResourceGroupName</span></span>
<span data-ttu-id="21989-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21989-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="21989-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="21989-124">-ServerName</span></span>
<span data-ttu-id="21989-125">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="21989-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="21989-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21989-126">CommonParameters</span></span>
<span data-ttu-id="21989-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21989-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21989-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21989-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21989-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21989-129">INPUTS</span></span>

### <span data-ttu-id="21989-130">System. String</span><span class="sxs-lookup"><span data-stu-id="21989-130">System.String</span></span>

## <span data-ttu-id="21989-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21989-131">OUTPUTS</span></span>

### <span data-ttu-id="21989-132">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="21989-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="21989-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21989-133">NOTES</span></span>

## <span data-ttu-id="21989-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21989-134">RELATED LINKS</span></span>

[<span data-ttu-id="21989-135">Nowe — AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="21989-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="21989-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="21989-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="21989-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="21989-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

