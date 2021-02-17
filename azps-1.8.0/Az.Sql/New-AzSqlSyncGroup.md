---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: 7789bdc098ab7bb02414ffc39f38ba25f1c7e5ae
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399570"
---
# <span data-ttu-id="d4f2d-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d4f2d-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="d4f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f2d-103">Tworzy grupę synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d4f2d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d4f2d-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4f2d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d4f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="d4f2d-106">Polecenie **cmdlet New-AzSqlSyncGroup** tworzy grupę synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d4f2d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d4f2d-107">EXAMPLES</span></span>

### <span data-ttu-id="d4f2d-108">Przykład 1. Tworzenie grupy synchronizacji dla usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
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
```

<span data-ttu-id="d4f2d-109">To polecenie tworzy grupę synchronizacji dla usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="d4f2d-110">"schema.js" to plik na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="d4f2d-111">Zawiera ona ładład treści shema w formacie json.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="d4f2d-112">Przykład schematu json: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="d4f2d-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="d4f2d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4f2d-113">PARAMETERS</span></span>

### <span data-ttu-id="d4f2d-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4f2d-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="d4f2d-115">Zasady rozwiązywania konfliktów między centrum a bazą danych członków w grupie synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f2d-116">- DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="d4f2d-116">-DatabaseCredential</span></span>
<span data-ttu-id="d4f2d-117">Poświadczenia uwierzytelniania SQL bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-117">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f2d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d4f2d-118">-DatabaseName</span></span>
<span data-ttu-id="d4f2d-119">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d4f2d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f2d-120">-DefaultProfile</span></span>
<span data-ttu-id="d4f2d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d4f2d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4f2d-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d4f2d-122">-IntervalInSeconds</span></span>
<span data-ttu-id="d4f2d-123">Częstotliwość (w sekundach) wykonywania synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="d4f2d-124">Wartość domyślna to -1, co oznacza, że synchronizacja automatyczna nie jest włączona.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f2d-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d4f2d-125">-Name</span></span>
<span data-ttu-id="d4f2d-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f2d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f2d-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4f2d-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4f2d-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="d4f2d-129">-SchemaFile</span></span>
<span data-ttu-id="d4f2d-130">Ścieżka pliku schematu.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-130">The path of the schema file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f2d-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d4f2d-131">-ServerName</span></span>
<span data-ttu-id="d4f2d-132">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d4f2d-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d4f2d-133">-SyncDatabaseName</span></span>
<span data-ttu-id="d4f2d-134">Baza danych używana do przechowywania powiązanych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-134">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f2d-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f2d-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="d4f2d-136">Grupa zasobów, do której baza metadanych należy.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f2d-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="d4f2d-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="d4f2d-138">Serwer, na którym jest hostowany baza metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f2d-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4f2d-139">-Confirm</span></span>
<span data-ttu-id="d4f2d-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4f2d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4f2d-141">-WhatIf</span></span>
<span data-ttu-id="d4f2d-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4f2d-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4f2d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f2d-144">CommonParameters</span></span>
<span data-ttu-id="d4f2d-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4f2d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f2d-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4f2d-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f2d-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4f2d-147">INPUTS</span></span>

### <span data-ttu-id="d4f2d-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d4f2d-148">System.String</span></span>

## <span data-ttu-id="d4f2d-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4f2d-149">OUTPUTS</span></span>

### <span data-ttu-id="d4f2d-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d4f2d-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d4f2d-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d4f2d-151">NOTES</span></span>

## <span data-ttu-id="d4f2d-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4f2d-152">RELATED LINKS</span></span>


[<span data-ttu-id="d4f2d-153">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d4f2d-153">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="d4f2d-154">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d4f2d-154">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

