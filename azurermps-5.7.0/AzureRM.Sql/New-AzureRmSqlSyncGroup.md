---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 65ac7bb4a63fa8519bd8f0b0c006209d5f171833
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547868"
---
# <span data-ttu-id="d7c51-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d7c51-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="d7c51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7c51-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c51-103">Tworzy grupę usługi Azure SQL Database Sync.</span><span class="sxs-lookup"><span data-stu-id="d7c51-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7c51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7c51-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7c51-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7c51-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c51-106">Polecenie cmdlet **New-AzureRmSqlSyncGroup** umożliwia utworzenie grupy synchronizacji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d7c51-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d7c51-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7c51-107">EXAMPLES</span></span>

### <span data-ttu-id="d7c51-108">Przykład 1: Tworzenie grupy synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d7c51-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
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

<span data-ttu-id="d7c51-109">To polecenie tworzy grupę synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d7c51-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="d7c51-110">"schema.json" to plik na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="d7c51-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="d7c51-111">Zawiera ładunek Shema w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="d7c51-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="d7c51-112">Przykładem kodu JSON schematu jest: {"Tables": [{"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}; {"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "cytowanie": "MayQuotedTable1"}, {"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"" b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2 "}]," pocytowana ":" MayQuotedTable2 "}]," MasterSyncMemberName ": null}</span><span class="sxs-lookup"><span data-stu-id="d7c51-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="d7c51-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7c51-113">PARAMETERS</span></span>

### <span data-ttu-id="d7c51-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d7c51-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="d7c51-115">Zasady rozwiązywania konfliktów między węzłem a bazą danych członków w grupie synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="d7c51-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="d7c51-116">-DatabaseCredential</span></span>
<span data-ttu-id="d7c51-117">Poświadczenia uwierzytelniania SQL bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="d7c51-117">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7c51-118">-DatabaseName</span></span>
<span data-ttu-id="d7c51-119">Nazwa bazy danych SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="d7c51-119">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c51-120">-DefaultProfile</span></span>
<span data-ttu-id="d7c51-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d7c51-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7c51-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d7c51-122">-IntervalInSeconds</span></span>
<span data-ttu-id="d7c51-123">Częstotliwość (w sekundach) wykonywania synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="d7c51-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="d7c51-124">Wartość domyślna to-1, co oznacza, że synchronizacja automatyczna nie jest włączona.</span><span class="sxs-lookup"><span data-stu-id="d7c51-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7c51-125">-Name</span></span>
<span data-ttu-id="d7c51-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d7c51-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7c51-127">-ResourceGroupName</span></span>
<span data-ttu-id="d7c51-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7c51-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7c51-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="d7c51-129">-SchemaFile</span></span>
<span data-ttu-id="d7c51-130">Ścieżka pliku schematu.</span><span class="sxs-lookup"><span data-stu-id="d7c51-130">The path of the schema file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d7c51-131">-ServerName</span></span>
<span data-ttu-id="d7c51-132">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d7c51-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d7c51-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7c51-133">-SyncDatabaseName</span></span>
<span data-ttu-id="d7c51-134">Baza danych używana do przechowywania metadanych powiązanych z synchronizacją.</span><span class="sxs-lookup"><span data-stu-id="d7c51-134">The database used to store sync related metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7c51-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="d7c51-136">Grupa zasobów, do której należy baza danych synchronizacji metadanych.</span><span class="sxs-lookup"><span data-stu-id="d7c51-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="d7c51-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="d7c51-138">Serwer, na którym znajduje się baza danych metadanych synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d7c51-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7c51-139">-Confirm</span></span>
<span data-ttu-id="d7c51-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7c51-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7c51-141">-WhatIf</span></span>
<span data-ttu-id="d7c51-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7c51-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7c51-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7c51-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c51-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c51-144">CommonParameters</span></span>
<span data-ttu-id="d7c51-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7c51-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c51-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7c51-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c51-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7c51-147">INPUTS</span></span>

### <span data-ttu-id="d7c51-148">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d7c51-148">None</span></span>
<span data-ttu-id="d7c51-149">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d7c51-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7c51-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7c51-150">OUTPUTS</span></span>

### <span data-ttu-id="d7c51-151">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d7c51-151">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d7c51-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7c51-152">NOTES</span></span>

## <span data-ttu-id="d7c51-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7c51-153">RELATED LINKS</span></span>

[<span data-ttu-id="d7c51-154">Set-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d7c51-154">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="d7c51-155">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d7c51-155">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="d7c51-156">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d7c51-156">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

