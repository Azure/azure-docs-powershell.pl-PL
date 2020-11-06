---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 3041d7a25ad87e6e2b9242043645a66219ac7e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547899"
---
# <span data-ttu-id="9e6dd-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="9e6dd-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="9e6dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6dd-103">Zwraca informacje dotyczące agentów synchronizacji Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9e6dd-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e6dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e6dd-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e6dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e6dd-105">DESCRIPTION</span></span>
<span data-ttu-id="9e6dd-106">Polecenie cmdlet **Get-AzureRmSqlSyncAgent** zwraca informacje dotyczące co najmniej jednego agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9e6dd-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="9e6dd-107">Określ nazwę agenta synchronizacji, aby wyświetlić informacje dotyczące tylko tego agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9e6dd-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="9e6dd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e6dd-108">EXAMPLES</span></span>

### <span data-ttu-id="9e6dd-109">Przykład 1: pobieranie wszystkich wystąpień agenta synchronizacji usługi Azure SQL przypisanego do usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9e6dd-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
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

<span data-ttu-id="9e6dd-110">To polecenie pobiera informacje o wszystkich agentach synchronizacji Azure SQL przypisanych do programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9e6dd-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="9e6dd-111">Przykład 2: uzyskiwanie informacji o agencie synchronizacji Azure SQL Sync</span><span class="sxs-lookup"><span data-stu-id="9e6dd-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
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

<span data-ttu-id="9e6dd-112">To polecenie pobiera informacje o agencie synchronizacji bazy danych SQL Azure o nazwie "SyncAgent01".</span><span class="sxs-lookup"><span data-stu-id="9e6dd-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="9e6dd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e6dd-113">PARAMETERS</span></span>

### <span data-ttu-id="9e6dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6dd-114">-DefaultProfile</span></span>
<span data-ttu-id="9e6dd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9e6dd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e6dd-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e6dd-116">-Name</span></span>
<span data-ttu-id="9e6dd-117">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9e6dd-117">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e6dd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e6dd-118">-ResourceGroupName</span></span>
<span data-ttu-id="9e6dd-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e6dd-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e6dd-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="9e6dd-120">-ServerName</span></span>
<span data-ttu-id="9e6dd-121">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="9e6dd-121">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="9e6dd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6dd-122">CommonParameters</span></span>
<span data-ttu-id="9e6dd-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e6dd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6dd-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6dd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6dd-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e6dd-125">INPUTS</span></span>

### <span data-ttu-id="9e6dd-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9e6dd-126">None</span></span>
<span data-ttu-id="9e6dd-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9e6dd-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e6dd-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e6dd-128">OUTPUTS</span></span>

### <span data-ttu-id="9e6dd-129">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="9e6dd-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="9e6dd-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e6dd-130">NOTES</span></span>

## <span data-ttu-id="9e6dd-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e6dd-131">RELATED LINKS</span></span>

[<span data-ttu-id="9e6dd-132">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="9e6dd-132">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="9e6dd-133">Nowe — AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="9e6dd-133">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

