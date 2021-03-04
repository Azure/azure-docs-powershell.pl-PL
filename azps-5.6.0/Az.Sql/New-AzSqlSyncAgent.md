---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: b3cd900760821765d135810acaaafdeac45c0eb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007585"
---
# <span data-ttu-id="cd1b8-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cd1b8-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="cd1b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1b8-103">Tworzy agenta azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="cd1b8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd1b8-104">SYNTAX</span></span>

### <span data-ttu-id="cd1b8-105">SyncDatabaseComponent (Default)</span><span class="sxs-lookup"><span data-stu-id="cd1b8-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd1b8-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="cd1b8-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd1b8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd1b8-107">DESCRIPTION</span></span>
<span data-ttu-id="cd1b8-108">Polecenie **cmdlet New-AzSqlSyncAgent** tworzy agenta azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="cd1b8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd1b8-109">EXAMPLES</span></span>

### <span data-ttu-id="cd1b8-110">Przykład 1. Tworzenie agenta synchronizacji dla serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
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

<span data-ttu-id="cd1b8-111">To polecenie tworzy agenta synchronizacji dla serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="cd1b8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd1b8-112">PARAMETERS</span></span>

### <span data-ttu-id="cd1b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1b8-113">-DefaultProfile</span></span>
<span data-ttu-id="cd1b8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cd1b8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd1b8-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cd1b8-115">-Name</span></span>
<span data-ttu-id="cd1b8-116">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-116">The sync agent name.</span></span>

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

### <span data-ttu-id="cd1b8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd1b8-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd1b8-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cd1b8-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cd1b8-119">-ServerName</span></span>
<span data-ttu-id="cd1b8-120">Nazwa serwera Azure SQL Server, w którym znajduje się agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="cd1b8-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd1b8-121">-SyncDatabaseName</span></span>
<span data-ttu-id="cd1b8-122">Baza danych używana do przechowywania powiązanych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-122">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="cd1b8-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd1b8-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="cd1b8-124">Grupa zasobów, do której baza metadanych należy.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-124">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="cd1b8-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="cd1b8-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="cd1b8-126">Identyfikator zasobu w centrum baza metadanych.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-126">The resource ID of  the sync metadata database.</span></span>

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

### <span data-ttu-id="cd1b8-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="cd1b8-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="cd1b8-128">Serwer, na którym jest hostowany baza metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-128">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="cd1b8-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd1b8-129">-Confirm</span></span>
<span data-ttu-id="cd1b8-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd1b8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd1b8-131">-WhatIf</span></span>
<span data-ttu-id="cd1b8-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd1b8-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd1b8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1b8-134">CommonParameters</span></span>
<span data-ttu-id="cd1b8-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd1b8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd1b8-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd1b8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1b8-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd1b8-137">INPUTS</span></span>

### <span data-ttu-id="cd1b8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cd1b8-138">System.String</span></span>

## <span data-ttu-id="cd1b8-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd1b8-139">OUTPUTS</span></span>

### <span data-ttu-id="cd1b8-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="cd1b8-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="cd1b8-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd1b8-141">NOTES</span></span>

## <span data-ttu-id="cd1b8-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd1b8-142">RELATED LINKS</span></span>

[<span data-ttu-id="cd1b8-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cd1b8-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="cd1b8-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cd1b8-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

