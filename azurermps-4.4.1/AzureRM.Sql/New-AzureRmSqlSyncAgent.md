---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
ms.openlocfilehash: e296e338d519537f688085fc5c142e3c12804b0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716521"
---
# <span data-ttu-id="757d8-101">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="757d8-101">New-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="757d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="757d8-102">SYNOPSIS</span></span>
<span data-ttu-id="757d8-103">Tworzy agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="757d8-103">Creates an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="757d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="757d8-104">SYNTAX</span></span>

### <span data-ttu-id="757d8-105">SyncDatabaseComponent (domyślny)</span><span class="sxs-lookup"><span data-stu-id="757d8-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="757d8-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="757d8-106">SyncDatabaseResourceID</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="757d8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="757d8-107">DESCRIPTION</span></span>
<span data-ttu-id="757d8-108">Polecenie cmdlet **New-AzureRmSqlSyncAgent** umożliwia utworzenie agenta synchronizacji SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="757d8-108">The **New-AzureRmSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="757d8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="757d8-109">EXAMPLES</span></span>

### <span data-ttu-id="757d8-110">Przykład 1: tworzenie agenta synchronizacji dla programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="757d8-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="757d8-111">To polecenie tworzy agenta synchronizacji dla programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="757d8-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="757d8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="757d8-112">PARAMETERS</span></span>

### <span data-ttu-id="757d8-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="757d8-113">-Confirm</span></span>
<span data-ttu-id="757d8-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="757d8-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757d8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="757d8-115">-Name</span></span>
<span data-ttu-id="757d8-116">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="757d8-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="757d8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="757d8-117">-ResourceGroupName</span></span>
<span data-ttu-id="757d8-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="757d8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="757d8-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="757d8-119">-ServerName</span></span>
<span data-ttu-id="757d8-120">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="757d8-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="757d8-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="757d8-121">-SyncDatabaseName</span></span>
<span data-ttu-id="757d8-122">Baza danych używana do przechowywania metadanych powiązanych z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="757d8-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757d8-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="757d8-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="757d8-124">Grupa zasobów, do której należy baza danych synchronizacji metadanych.</span><span class="sxs-lookup"><span data-stu-id="757d8-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757d8-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="757d8-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="757d8-126">Identyfikator zasobu bazy danych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="757d8-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757d8-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="757d8-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="757d8-128">Serwer, na którym znajduje się baza danych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="757d8-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757d8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757d8-129">-WhatIf</span></span>
<span data-ttu-id="757d8-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="757d8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="757d8-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="757d8-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757d8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757d8-132">-DefaultProfile</span></span>
<span data-ttu-id="757d8-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="757d8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="757d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757d8-134">CommonParameters</span></span>
<span data-ttu-id="757d8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="757d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757d8-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="757d8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757d8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="757d8-137">INPUTS</span></span>

## <span data-ttu-id="757d8-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="757d8-138">OUTPUTS</span></span>

### <span data-ttu-id="757d8-139">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="757d8-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="757d8-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="757d8-140">NOTES</span></span>

## <span data-ttu-id="757d8-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="757d8-141">RELATED LINKS</span></span>

[<span data-ttu-id="757d8-142">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="757d8-142">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="757d8-143">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="757d8-143">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

