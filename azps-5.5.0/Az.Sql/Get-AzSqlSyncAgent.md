---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183298"
---
# <span data-ttu-id="b9759-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b9759-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="b9759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9759-102">SYNOPSIS</span></span>
<span data-ttu-id="b9759-103">Zwraca informacje o agentach synchronizacji języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b9759-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="b9759-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b9759-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9759-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b9759-105">DESCRIPTION</span></span>
<span data-ttu-id="b9759-106">Polecenie **cmdlet Get-AzSqlSyncAgent** zwraca informacje o jednym lub większej liczby agentów synchronizacji języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b9759-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="b9759-107">Określ nazwę agenta synchronizacji, aby wyświetlić informacje tylko dla tego agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="b9759-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="b9759-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b9759-108">EXAMPLES</span></span>

### <span data-ttu-id="b9759-109">Przykład 1. Uzyskiwanie wszystkich wystąpień programu Azure SQL Sync Agent przypisanego do serwera Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="b9759-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="b9759-110">To polecenie pobiera informacje o wszystkich agentach synchronizacji języka Azure SQL przypisanych do serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b9759-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="b9759-111">Przykład 2. Uzyskiwanie informacji o agentze azure SQL Sync Agent</span><span class="sxs-lookup"><span data-stu-id="b9759-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="b9759-112">To polecenie pobiera informacje o agentze synchronizacji bazy danych Azure SQL o nazwie "SyncAgent01"</span><span class="sxs-lookup"><span data-stu-id="b9759-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="b9759-113">Przykład 3. Uzyskiwanie wszystkich wystąpień programu Azure SQL Sync Agent przypisanego do serwera Azure SQL Server przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="b9759-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
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

<span data-ttu-id="b9759-114">To polecenie pobiera informacje o wszystkich agentach synchronizacji języka Azure SQL przypisanych do serwera Azure SQL Server, których nazwa rozpoczyna się od "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="b9759-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="b9759-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9759-115">PARAMETERS</span></span>

### <span data-ttu-id="b9759-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9759-116">-DefaultProfile</span></span>
<span data-ttu-id="b9759-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b9759-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9759-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b9759-118">-Name</span></span>
<span data-ttu-id="b9759-119">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="b9759-119">The sync agent name.</span></span>

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

### <span data-ttu-id="b9759-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9759-120">-ResourceGroupName</span></span>
<span data-ttu-id="b9759-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b9759-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9759-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9759-122">-ServerName</span></span>
<span data-ttu-id="b9759-123">Nazwa serwera Azure SQL Server, w którym znajduje się agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="b9759-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="b9759-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9759-124">CommonParameters</span></span>
<span data-ttu-id="b9759-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9759-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9759-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9759-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9759-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9759-127">INPUTS</span></span>

### <span data-ttu-id="b9759-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b9759-128">System.String</span></span>

## <span data-ttu-id="b9759-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9759-129">OUTPUTS</span></span>

### <span data-ttu-id="b9759-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="b9759-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="b9759-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b9759-131">NOTES</span></span>

## <span data-ttu-id="b9759-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9759-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9759-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b9759-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="b9759-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b9759-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

