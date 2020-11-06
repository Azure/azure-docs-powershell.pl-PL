---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 71a4d20c6296c8a9d725cb9a16960d6c4a06646c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542224"
---
# <span data-ttu-id="1548b-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1548b-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="1548b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1548b-102">SYNOPSIS</span></span>
<span data-ttu-id="1548b-103">Zwraca informacje dotyczące grup synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="1548b-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1548b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1548b-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1548b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1548b-105">DESCRIPTION</span></span>
<span data-ttu-id="1548b-106">Polecenie cmdlet **Get-AzureRmSqlSyncGroup** zwraca informacje o jednej lub większej liczbie grup synchronizacji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1548b-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="1548b-107">Określ nazwę grupy synchronizacji, aby wyświetlić informacje dotyczące tylko tej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="1548b-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="1548b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1548b-108">EXAMPLES</span></span>

### <span data-ttu-id="1548b-109">Przykład 1: pobieranie wszystkich wystąpień grupy synchronizacji Azure SQL przypisanej do bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="1548b-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="1548b-110">To polecenie pobiera informacje o grupach synchronizacji bazy danych SQL Azure przypisanych do bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1548b-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="1548b-111">Przykład 2: uzyskiwanie informacji o grupie Synchronizacja bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="1548b-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="1548b-112">To polecenie pobiera informacje o grupie synchronizowania bazy danych SQL Azure o nazwie "SyncGroup01".</span><span class="sxs-lookup"><span data-stu-id="1548b-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="1548b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1548b-113">PARAMETERS</span></span>

### <span data-ttu-id="1548b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1548b-114">-DatabaseName</span></span>
<span data-ttu-id="1548b-115">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="1548b-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1548b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1548b-116">-DefaultProfile</span></span>
<span data-ttu-id="1548b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1548b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1548b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1548b-118">-Name</span></span>
<span data-ttu-id="1548b-119">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="1548b-119">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1548b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1548b-120">-ResourceGroupName</span></span>
<span data-ttu-id="1548b-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1548b-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="1548b-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="1548b-122">-ServerName</span></span>
<span data-ttu-id="1548b-123">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1548b-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1548b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1548b-124">CommonParameters</span></span>
<span data-ttu-id="1548b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1548b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1548b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1548b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1548b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1548b-127">INPUTS</span></span>

### <span data-ttu-id="1548b-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1548b-128">None</span></span>
<span data-ttu-id="1548b-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1548b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1548b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1548b-130">OUTPUTS</span></span>

### <span data-ttu-id="1548b-131">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="1548b-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="1548b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1548b-132">NOTES</span></span>

## <span data-ttu-id="1548b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1548b-133">RELATED LINKS</span></span>

[<span data-ttu-id="1548b-134">Nowe — AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1548b-134">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="1548b-135">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1548b-135">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="1548b-136">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1548b-136">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

