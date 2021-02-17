---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: d117ef9685a235528cb91c82a148ff0dddb2d96c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178442"
---
# <span data-ttu-id="1e5c3-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1e5c3-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="1e5c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5c3-103">Zwraca informacje o grupach synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="1e5c3-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="1e5c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e5c3-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e5c3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e5c3-105">DESCRIPTION</span></span>
<span data-ttu-id="1e5c3-106">Polecenie **cmdlet Get-AzSqlSyncGroup** zwraca informacje o co najmniej jednej grupie synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1e5c3-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="1e5c3-107">Określ nazwę grupy synchronizacji, aby wyświetlić informacje tylko dla tej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="1e5c3-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="1e5c3-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e5c3-108">EXAMPLES</span></span>

### <span data-ttu-id="1e5c3-109">Przykład 1. Uzyskiwanie wszystkich wystąpień grupy azure SQL Sync Group przypisanej do bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="1e5c3-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="1e5c3-110">To polecenie pobiera informacje o wszystkich grupach synchronizacji usługi Azure SQL Database przypisanych do usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="1e5c3-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="1e5c3-111">Przykład 2. Uzyskiwanie informacji o grupie synchronizacji usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="1e5c3-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="1e5c3-112">To polecenie pobiera informacje o grupie synchronizacji bazy danych Azure SQL o nazwie "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="1e5c3-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="1e5c3-113">Przykład 3. Uzyskiwanie wszystkich wystąpień grupy Azure SQL Sync Group przypisanej do bazy danych Azure SQL Database przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="1e5c3-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
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

<span data-ttu-id="1e5c3-114">To polecenie pobiera informacje o wszystkich grupach synchronizacji usługi Azure SQL Database przypisanych do bazy danych Azure SQL Database, których nazwa rozpoczyna się od "SyncGroup".</span><span class="sxs-lookup"><span data-stu-id="1e5c3-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="1e5c3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e5c3-115">PARAMETERS</span></span>

### <span data-ttu-id="1e5c3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e5c3-116">-DatabaseName</span></span>
<span data-ttu-id="1e5c3-117">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="1e5c3-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1e5c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5c3-118">-DefaultProfile</span></span>
<span data-ttu-id="1e5c3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1e5c3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e5c3-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1e5c3-120">-Name</span></span>
<span data-ttu-id="1e5c3-121">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="1e5c3-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5c3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5c3-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e5c3-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e5c3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="1e5c3-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1e5c3-124">-ServerName</span></span>
<span data-ttu-id="1e5c3-125">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1e5c3-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1e5c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5c3-126">CommonParameters</span></span>
<span data-ttu-id="1e5c3-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e5c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5c3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e5c3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5c3-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e5c3-129">INPUTS</span></span>

### <span data-ttu-id="1e5c3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1e5c3-130">System.String</span></span>

## <span data-ttu-id="1e5c3-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e5c3-131">OUTPUTS</span></span>

### <span data-ttu-id="1e5c3-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="1e5c3-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="1e5c3-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e5c3-133">NOTES</span></span>

## <span data-ttu-id="1e5c3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e5c3-134">RELATED LINKS</span></span>

[<span data-ttu-id="1e5c3-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1e5c3-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="1e5c3-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1e5c3-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="1e5c3-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1e5c3-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

