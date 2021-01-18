---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: 4a4ce99eb30aaa959eabdc9c1385b567aef2b0fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498313"
---
# <span data-ttu-id="dd3ab-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="dd3ab-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="dd3ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="dd3ab-103">Tworzy agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="dd3ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd3ab-104">SYNTAX</span></span>

### <span data-ttu-id="dd3ab-105">SyncDatabaseComponent (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dd3ab-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd3ab-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="dd3ab-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd3ab-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dd3ab-107">DESCRIPTION</span></span>
<span data-ttu-id="dd3ab-108">Polecenie cmdlet **New-AzSqlSyncAgent** umożliwia utworzenie agenta synchronizacji SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="dd3ab-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd3ab-109">EXAMPLES</span></span>

### <span data-ttu-id="dd3ab-110">Przykład 1: tworzenie agenta synchronizacji dla programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
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

<span data-ttu-id="dd3ab-111">To polecenie tworzy agenta synchronizacji dla programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="dd3ab-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd3ab-112">PARAMETERS</span></span>

### <span data-ttu-id="dd3ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd3ab-113">-DefaultProfile</span></span>
<span data-ttu-id="dd3ab-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dd3ab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd3ab-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd3ab-115">-Name</span></span>
<span data-ttu-id="dd3ab-116">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-116">The sync agent name.</span></span>

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

### <span data-ttu-id="dd3ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd3ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd3ab-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="dd3ab-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="dd3ab-119">-ServerName</span></span>
<span data-ttu-id="dd3ab-120">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="dd3ab-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd3ab-121">-SyncDatabaseName</span></span>
<span data-ttu-id="dd3ab-122">Baza danych używana do przechowywania metadanych powiązanych z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-122">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="dd3ab-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd3ab-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="dd3ab-124">Grupa zasobów, do której należy baza danych synchronizacji metadanych.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-124">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="dd3ab-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="dd3ab-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="dd3ab-126">Identyfikator zasobu bazy danych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-126">The resource ID of  the sync metadata database.</span></span>

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

### <span data-ttu-id="dd3ab-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="dd3ab-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="dd3ab-128">Serwer, na którym znajduje się baza danych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-128">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="dd3ab-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd3ab-129">-Confirm</span></span>
<span data-ttu-id="dd3ab-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd3ab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd3ab-131">-WhatIf</span></span>
<span data-ttu-id="dd3ab-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd3ab-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd3ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3ab-134">CommonParameters</span></span>
<span data-ttu-id="dd3ab-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd3ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd3ab-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd3ab-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3ab-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd3ab-137">INPUTS</span></span>

### <span data-ttu-id="dd3ab-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dd3ab-138">System.String</span></span>

## <span data-ttu-id="dd3ab-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd3ab-139">OUTPUTS</span></span>

### <span data-ttu-id="dd3ab-140">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="dd3ab-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="dd3ab-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd3ab-141">NOTES</span></span>

## <span data-ttu-id="dd3ab-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd3ab-142">RELATED LINKS</span></span>

[<span data-ttu-id="dd3ab-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="dd3ab-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="dd3ab-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="dd3ab-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

