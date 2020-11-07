---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: f74a031079ab35e1584d8c7e5536e2605ea665ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886889"
---
# <span data-ttu-id="fac8d-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="fac8d-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="fac8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fac8d-102">SYNOPSIS</span></span>
<span data-ttu-id="fac8d-103">Zwraca informacje dotyczące agentów synchronizacji Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fac8d-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="fac8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fac8d-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fac8d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fac8d-105">DESCRIPTION</span></span>
<span data-ttu-id="fac8d-106">Polecenie cmdlet **Get-AzSqlSyncAgent** zwraca informacje dotyczące co najmniej jednego agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fac8d-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="fac8d-107">Określ nazwę agenta synchronizacji, aby wyświetlić informacje dotyczące tylko tego agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fac8d-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="fac8d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fac8d-108">EXAMPLES</span></span>

### <span data-ttu-id="fac8d-109">Przykład 1: pobieranie wszystkich wystąpień agenta synchronizacji usługi Azure SQL przypisanego do usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="fac8d-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="fac8d-110">To polecenie pobiera informacje o wszystkich agentach synchronizacji Azure SQL przypisanych do programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fac8d-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="fac8d-111">Przykład 2: uzyskiwanie informacji o agencie synchronizacji Azure SQL Sync</span><span class="sxs-lookup"><span data-stu-id="fac8d-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="fac8d-112">To polecenie pobiera informacje o agencie synchronizacji bazy danych SQL Azure o nazwie "SyncAgent01".</span><span class="sxs-lookup"><span data-stu-id="fac8d-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="fac8d-113">Przykład 3: pobieranie wszystkich wystąpień agenta synchronizacji usługi Azure SQL przypisanego do usługi Azure SQL Server przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="fac8d-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
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

<span data-ttu-id="fac8d-114">To polecenie pobiera informacje o wszystkich agentach synchronizacji usługi Azure SQL przypisanych do programu Azure SQL Server, który rozpoczyna się od "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="fac8d-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="fac8d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fac8d-115">PARAMETERS</span></span>

### <span data-ttu-id="fac8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac8d-116">-DefaultProfile</span></span>
<span data-ttu-id="fac8d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fac8d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fac8d-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fac8d-118">-Name</span></span>
<span data-ttu-id="fac8d-119">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fac8d-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fac8d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fac8d-120">-ResourceGroupName</span></span>
<span data-ttu-id="fac8d-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fac8d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="fac8d-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fac8d-122">-ServerName</span></span>
<span data-ttu-id="fac8d-123">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="fac8d-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="fac8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac8d-124">CommonParameters</span></span>
<span data-ttu-id="fac8d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fac8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac8d-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fac8d-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac8d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fac8d-127">INPUTS</span></span>

### <span data-ttu-id="fac8d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fac8d-128">System.String</span></span>

## <span data-ttu-id="fac8d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fac8d-129">OUTPUTS</span></span>

### <span data-ttu-id="fac8d-130">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="fac8d-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="fac8d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fac8d-131">NOTES</span></span>

## <span data-ttu-id="fac8d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fac8d-132">RELATED LINKS</span></span>

[<span data-ttu-id="fac8d-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="fac8d-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="fac8d-134">Nowe — AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="fac8d-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

