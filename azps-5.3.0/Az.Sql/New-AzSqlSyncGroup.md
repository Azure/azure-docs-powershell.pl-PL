---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: d6964f076dd1e6882a8031f19101f55d19b9e4d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498305"
---
# <span data-ttu-id="a9cc3-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a9cc3-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="a9cc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="a9cc3-103">Tworzy grupę usługi Azure SQL Database Sync.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="a9cc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9cc3-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9cc3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="a9cc3-106">Polecenie cmdlet **New-AzSqlSyncGroup** umożliwia utworzenie grupy synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="a9cc3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9cc3-107">EXAMPLES</span></span>

### <span data-ttu-id="a9cc3-108">Przykład 1: Tworzenie grupy synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="a9cc3-109">To polecenie tworzy grupę synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="a9cc3-110">"schema.json" to plik na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="a9cc3-111">Zawiera ładunek schematu w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="a9cc3-112">Przykładem kodu JSON schematu jest: {"Tables": [{"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}; {"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "cytowanie": "MayQuotedTable1"}, {"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"" b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2 "}]," pocytowana ":" MayQuotedTable2 "}]," MasterSyncMemberName ": null}</span><span class="sxs-lookup"><span data-stu-id="a9cc3-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="a9cc3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9cc3-113">PARAMETERS</span></span>

### <span data-ttu-id="a9cc3-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a9cc3-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="a9cc3-115">Zasady rozwiązywania konfliktów między bazą danych w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="a9cc3-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="a9cc3-116">-DatabaseCredential</span></span>
<span data-ttu-id="a9cc3-117">Poświadczenia uwierzytelniania SQL bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="a9cc3-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a9cc3-118">-DatabaseName</span></span>
<span data-ttu-id="a9cc3-119">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a9cc3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9cc3-120">-DefaultProfile</span></span>
<span data-ttu-id="a9cc3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a9cc3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9cc3-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a9cc3-122">-IntervalInSeconds</span></span>
<span data-ttu-id="a9cc3-123">Częstotliwość (w sekundach) wykonywania synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="a9cc3-124">Wartość domyślna to-1, co oznacza, że synchronizacja automatyczna nie jest włączona.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="a9cc3-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9cc3-125">-Name</span></span>
<span data-ttu-id="a9cc3-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-126">The sync group name.</span></span>

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

### <span data-ttu-id="a9cc3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9cc3-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9cc3-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a9cc3-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="a9cc3-129">-SchemaFile</span></span>
<span data-ttu-id="a9cc3-130">Ścieżka pliku schematu.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="a9cc3-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a9cc3-131">-ServerName</span></span>
<span data-ttu-id="a9cc3-132">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a9cc3-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a9cc3-133">-SyncDatabaseName</span></span>
<span data-ttu-id="a9cc3-134">Baza danych używana do przechowywania metadanych powiązanych z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="a9cc3-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9cc3-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="a9cc3-136">Grupa zasobów, do której należy baza danych synchronizacji metadanych.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="a9cc3-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="a9cc3-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="a9cc3-138">Serwer, na którym znajduje się baza danych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="a9cc3-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a9cc3-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="a9cc3-140">Podczas nawiązywania połączenia z węzłem tej grupy synchronizacji Użyj połączenia prywatnego.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9cc3-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9cc3-141">-Confirm</span></span>
<span data-ttu-id="a9cc3-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9cc3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9cc3-143">-WhatIf</span></span>
<span data-ttu-id="a9cc3-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9cc3-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9cc3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9cc3-146">CommonParameters</span></span>
<span data-ttu-id="a9cc3-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9cc3-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9cc3-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9cc3-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9cc3-149">INPUTS</span></span>

### <span data-ttu-id="a9cc3-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a9cc3-150">System.String</span></span>

## <span data-ttu-id="a9cc3-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9cc3-151">OUTPUTS</span></span>

### <span data-ttu-id="a9cc3-152">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a9cc3-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a9cc3-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9cc3-153">NOTES</span></span>

## <span data-ttu-id="a9cc3-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9cc3-154">RELATED LINKS</span></span>

[<span data-ttu-id="a9cc3-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a9cc3-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="a9cc3-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a9cc3-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="a9cc3-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a9cc3-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

