---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: c95b6a7a42327b7380e19ff333453f956797dcdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008353"
---
# <span data-ttu-id="475a6-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="475a6-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="475a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="475a6-102">SYNOPSIS</span></span>
<span data-ttu-id="475a6-103">Aktualizuje grupę synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="475a6-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="475a6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="475a6-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="475a6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="475a6-105">DESCRIPTION</span></span>
<span data-ttu-id="475a6-106">Polecenie **cmdlet Update-AzSqlSyncGroup** modyfikuje właściwości grupy synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="475a6-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="475a6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="475a6-107">EXAMPLES</span></span>

### <span data-ttu-id="475a6-108">Przykład 1. Aktualizowanie grupy synchronizacji dla usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="475a6-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
-DatabaseCredential $credential -IntervalInSeconds 100 -Schema ".\schema.json" | Format-List
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

<span data-ttu-id="475a6-109">To polecenie aktualizuje grupę synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="475a6-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="475a6-110">"schema.js" to plik na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="475a6-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="475a6-111">Zawiera ona ład w schemacie w formacie json.</span><span class="sxs-lookup"><span data-stu-id="475a6-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="475a6-112">Przykład schematu json: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="475a6-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="475a6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="475a6-113">PARAMETERS</span></span>

### <span data-ttu-id="475a6-114">- DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="475a6-114">-DatabaseCredential</span></span>
<span data-ttu-id="475a6-115">Poświadczenia uwierzytelniania SQL bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="475a6-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="475a6-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="475a6-116">-DatabaseName</span></span>
<span data-ttu-id="475a6-117">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="475a6-117">SQL Database name.</span></span>

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

### <span data-ttu-id="475a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475a6-118">-DefaultProfile</span></span>
<span data-ttu-id="475a6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="475a6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="475a6-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="475a6-120">-IntervalInSeconds</span></span>
<span data-ttu-id="475a6-121">Częstotliwość (w sekundach) wykonywania synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="475a6-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="475a6-122">Wartość domyślna to -1, co oznacza, że synchronizacja automatyczna nie jest włączona.</span><span class="sxs-lookup"><span data-stu-id="475a6-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="475a6-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="475a6-123">-Name</span></span>
<span data-ttu-id="475a6-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="475a6-124">The sync group name.</span></span>

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

### <span data-ttu-id="475a6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475a6-125">-ResourceGroupName</span></span>
<span data-ttu-id="475a6-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="475a6-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="475a6-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="475a6-127">-SchemaFile</span></span>
<span data-ttu-id="475a6-128">Ścieżka pliku schematu.</span><span class="sxs-lookup"><span data-stu-id="475a6-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="475a6-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="475a6-129">-ServerName</span></span>
<span data-ttu-id="475a6-130">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="475a6-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="475a6-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="475a6-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="475a6-132">Czy podczas nawiązywania połączenia z centrum tej grupy synchronizacji ma być nawiązywane połączenie z linkiem prywatnym.</span><span class="sxs-lookup"><span data-stu-id="475a6-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475a6-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="475a6-133">-Confirm</span></span>
<span data-ttu-id="475a6-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="475a6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="475a6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="475a6-135">-WhatIf</span></span>
<span data-ttu-id="475a6-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="475a6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="475a6-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="475a6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="475a6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475a6-138">CommonParameters</span></span>
<span data-ttu-id="475a6-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475a6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475a6-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="475a6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475a6-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="475a6-141">INPUTS</span></span>

### <span data-ttu-id="475a6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="475a6-142">System.String</span></span>

## <span data-ttu-id="475a6-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="475a6-143">OUTPUTS</span></span>

### <span data-ttu-id="475a6-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="475a6-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="475a6-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="475a6-145">NOTES</span></span>

## <span data-ttu-id="475a6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="475a6-146">RELATED LINKS</span></span>

[<span data-ttu-id="475a6-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="475a6-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="475a6-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="475a6-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="475a6-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="475a6-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

