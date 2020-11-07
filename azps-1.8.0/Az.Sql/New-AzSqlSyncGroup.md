---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: 512ed43ac1770a7a1a026c5a64d20a25016d547e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707837"
---
# <span data-ttu-id="3a89e-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3a89e-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="3a89e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a89e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a89e-103">Tworzy grupę usługi Azure SQL Database Sync.</span><span class="sxs-lookup"><span data-stu-id="3a89e-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="3a89e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a89e-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a89e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a89e-105">DESCRIPTION</span></span>
<span data-ttu-id="3a89e-106">Polecenie cmdlet **New-AzSqlSyncGroup** umożliwia utworzenie grupy synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3a89e-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="3a89e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a89e-107">EXAMPLES</span></span>

### <span data-ttu-id="3a89e-108">Przykład 1: Tworzenie grupy synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3a89e-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="3a89e-109">To polecenie tworzy grupę synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3a89e-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="3a89e-110">"schema.json" to plik na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="3a89e-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="3a89e-111">Zawiera ładunek Shema w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="3a89e-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="3a89e-112">Przykładem kodu JSON schematu jest: {"Tables": [{"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}; {"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "cytowanie": "MayQuotedTable1"}, {"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"" b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2 "}]," pocytowana ":" MayQuotedTable2 "}]," MasterSyncMemberName ": null}</span><span class="sxs-lookup"><span data-stu-id="3a89e-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="3a89e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a89e-113">PARAMETERS</span></span>

### <span data-ttu-id="3a89e-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a89e-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="3a89e-115">Zasady rozwiązywania konfliktów między węzłem a bazą danych członków w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="3a89e-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="3a89e-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="3a89e-116">-DatabaseCredential</span></span>
<span data-ttu-id="3a89e-117">Poświadczenia uwierzytelniania SQL bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="3a89e-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="3a89e-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a89e-118">-DatabaseName</span></span>
<span data-ttu-id="3a89e-119">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="3a89e-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3a89e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a89e-120">-DefaultProfile</span></span>
<span data-ttu-id="3a89e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3a89e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a89e-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3a89e-122">-IntervalInSeconds</span></span>
<span data-ttu-id="3a89e-123">Częstotliwość (w sekundach) wykonywania synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="3a89e-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="3a89e-124">Wartość domyślna to-1, co oznacza, że synchronizacja automatyczna nie jest włączona.</span><span class="sxs-lookup"><span data-stu-id="3a89e-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="3a89e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a89e-125">-Name</span></span>
<span data-ttu-id="3a89e-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="3a89e-126">The sync group name.</span></span>

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

### <span data-ttu-id="3a89e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a89e-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a89e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a89e-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a89e-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="3a89e-129">-SchemaFile</span></span>
<span data-ttu-id="3a89e-130">Ścieżka pliku schematu.</span><span class="sxs-lookup"><span data-stu-id="3a89e-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="3a89e-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3a89e-131">-ServerName</span></span>
<span data-ttu-id="3a89e-132">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3a89e-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="3a89e-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a89e-133">-SyncDatabaseName</span></span>
<span data-ttu-id="3a89e-134">Baza danych używana do przechowywania metadanych powiązanych z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="3a89e-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="3a89e-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a89e-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="3a89e-136">Grupa zasobów, do której należy baza danych synchronizacji metadanych.</span><span class="sxs-lookup"><span data-stu-id="3a89e-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="3a89e-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="3a89e-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="3a89e-138">Serwer, na którym znajduje się baza danych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="3a89e-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="3a89e-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a89e-139">-Confirm</span></span>
<span data-ttu-id="3a89e-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a89e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a89e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a89e-141">-WhatIf</span></span>
<span data-ttu-id="3a89e-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a89e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a89e-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a89e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a89e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a89e-144">CommonParameters</span></span>
<span data-ttu-id="3a89e-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a89e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a89e-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a89e-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a89e-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a89e-147">INPUTS</span></span>

### <span data-ttu-id="3a89e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3a89e-148">System.String</span></span>

## <span data-ttu-id="3a89e-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a89e-149">OUTPUTS</span></span>

### <span data-ttu-id="3a89e-150">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="3a89e-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="3a89e-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a89e-151">NOTES</span></span>

## <span data-ttu-id="3a89e-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a89e-152">RELATED LINKS</span></span>

[<span data-ttu-id="3a89e-153">Set-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3a89e-153">Set-AzSqlSyncGroup</span></span>](./Set-AzSqlSyncGroup.md)

[<span data-ttu-id="3a89e-154">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3a89e-154">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="3a89e-155">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3a89e-155">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)
