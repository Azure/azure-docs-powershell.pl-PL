---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: e581f0bd94e58f725055c0dc1a4f1d704b891c86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716661"
---
# <span data-ttu-id="9fec6-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9fec6-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="9fec6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fec6-102">SYNOPSIS</span></span>
<span data-ttu-id="9fec6-103">Zwraca informacje dotyczące grup synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9fec6-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fec6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fec6-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fec6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9fec6-105">DESCRIPTION</span></span>
<span data-ttu-id="9fec6-106">Polecenie cmdlet **Get-AzureRmSqlSyncGroup** zwraca informacje o jednej lub większej liczbie grup synchronizacji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9fec6-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="9fec6-107">Określ nazwę grupy synchronizacji, aby wyświetlić informacje dotyczące tylko tej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9fec6-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="9fec6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fec6-108">EXAMPLES</span></span>

### <span data-ttu-id="9fec6-109">Przykład 1: pobieranie wszystkich wystąpień grupy synchronizacji Azure SQL przypisanej do bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="9fec6-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
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

<span data-ttu-id="9fec6-110">To polecenie pobiera informacje o grupach synchronizacji bazy danych SQL Azure przypisanych do bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9fec6-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="9fec6-111">Przykład 2: uzyskiwanie informacji o grupie Synchronizacja bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="9fec6-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
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

<span data-ttu-id="9fec6-112">To polecenie pobiera informacje o grupie synchronizowania bazy danych SQL Azure o nazwie "SyncGroup01".</span><span class="sxs-lookup"><span data-stu-id="9fec6-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="9fec6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fec6-113">PARAMETERS</span></span>

### <span data-ttu-id="9fec6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9fec6-114">-DatabaseName</span></span>
<span data-ttu-id="9fec6-115">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="9fec6-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9fec6-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fec6-116">-Name</span></span>
<span data-ttu-id="9fec6-117">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9fec6-117">The sync group name.</span></span>

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

### <span data-ttu-id="9fec6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fec6-118">-ResourceGroupName</span></span>
<span data-ttu-id="9fec6-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fec6-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="9fec6-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="9fec6-120">-ServerName</span></span>
<span data-ttu-id="9fec6-121">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9fec6-121">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9fec6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fec6-122">-DefaultProfile</span></span>
<span data-ttu-id="9fec6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fec6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fec6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fec6-124">CommonParameters</span></span>
<span data-ttu-id="9fec6-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fec6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fec6-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fec6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fec6-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fec6-127">INPUTS</span></span>

## <span data-ttu-id="9fec6-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fec6-128">OUTPUTS</span></span>

### <span data-ttu-id="9fec6-129">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="9fec6-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="9fec6-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fec6-130">NOTES</span></span>

## <span data-ttu-id="9fec6-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fec6-131">RELATED LINKS</span></span>

[<span data-ttu-id="9fec6-132">Nowe — AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9fec6-132">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="9fec6-133">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9fec6-133">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="9fec6-134">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9fec6-134">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

