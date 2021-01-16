---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352318"
---
# <span data-ttu-id="eb572-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="eb572-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="eb572-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb572-102">SYNOPSIS</span></span>
<span data-ttu-id="eb572-103">Zwraca informacje dotyczące agentów synchronizacji Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="eb572-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="eb572-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb572-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb572-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb572-105">DESCRIPTION</span></span>
<span data-ttu-id="eb572-106">Polecenie cmdlet **Get-AzSqlSyncAgent** zwraca informacje dotyczące co najmniej jednego agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="eb572-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="eb572-107">Określ nazwę agenta synchronizacji, aby wyświetlić informacje dotyczące tylko tego agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="eb572-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="eb572-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb572-108">EXAMPLES</span></span>

### <span data-ttu-id="eb572-109">Przykład 1: pobieranie wszystkich wystąpień agenta synchronizacji usługi Azure SQL przypisanego do usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="eb572-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="eb572-110">To polecenie pobiera informacje o wszystkich agentach synchronizacji Azure SQL przypisanych do programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="eb572-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="eb572-111">Przykład 2: uzyskiwanie informacji o agencie synchronizacji Azure SQL Sync</span><span class="sxs-lookup"><span data-stu-id="eb572-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="eb572-112">To polecenie pobiera informacje o agencie synchronizacji bazy danych SQL Azure o nazwie "SyncAgent01".</span><span class="sxs-lookup"><span data-stu-id="eb572-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="eb572-113">Przykład 3: pobieranie wszystkich wystąpień agenta synchronizacji usługi Azure SQL przypisanego do usługi Azure SQL Server przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="eb572-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name SyncAgent* | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="eb572-114">To polecenie pobiera informacje o wszystkich agentach synchronizacji usługi Azure SQL przypisanych do programu Azure SQL Server, który rozpoczyna się od "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="eb572-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="eb572-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb572-115">PARAMETERS</span></span>

### <span data-ttu-id="eb572-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb572-116">-DefaultProfile</span></span>
<span data-ttu-id="eb572-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eb572-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb572-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eb572-118">-Name</span></span>
<span data-ttu-id="eb572-119">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="eb572-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb572-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb572-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb572-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eb572-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="eb572-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="eb572-122">-ServerName</span></span>
<span data-ttu-id="eb572-123">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="eb572-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="eb572-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb572-124">CommonParameters</span></span>
<span data-ttu-id="eb572-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb572-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb572-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb572-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb572-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb572-127">INPUTS</span></span>

### <span data-ttu-id="eb572-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eb572-128">System.String</span></span>

## <span data-ttu-id="eb572-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb572-129">OUTPUTS</span></span>

### <span data-ttu-id="eb572-130">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="eb572-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="eb572-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb572-131">NOTES</span></span>

## <span data-ttu-id="eb572-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb572-132">RELATED LINKS</span></span>

[<span data-ttu-id="eb572-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="eb572-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="eb572-134">Nowe — AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="eb572-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

