---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 198dee21b2674f3c10d0679cbb57fdee6e1f6ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547836"
---
# <span data-ttu-id="575bf-101">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="575bf-101">Update-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="575bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="575bf-102">SYNOPSIS</span></span>
<span data-ttu-id="575bf-103">Umożliwia zaktualizowanie grupy synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="575bf-103">Updates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="575bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="575bf-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="575bf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="575bf-105">DESCRIPTION</span></span>
<span data-ttu-id="575bf-106">Polecenie cmdlet **Update-AzureRmSqlSyncGroup** modyfikuje właściwości grupy synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="575bf-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="575bf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="575bf-107">EXAMPLES</span></span>

### <span data-ttu-id="575bf-108">Przykład 1: aktualizowanie grupy synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="575bf-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
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

<span data-ttu-id="575bf-109">To polecenie aktualizuje grupę synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="575bf-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="575bf-110">"schema.json" to plik na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="575bf-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="575bf-111">Zawiera ładunek Shema w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="575bf-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="575bf-112">Przykładem kodu JSON schematu jest: {"Tables": [{"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}; {"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "cytowanie": "MayQuotedTable1"}, {"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"" b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2 "}]," pocytowana ":" MayQuotedTable2 "}]," MasterSyncMemberName ": null}</span><span class="sxs-lookup"><span data-stu-id="575bf-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="575bf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="575bf-113">PARAMETERS</span></span>

### <span data-ttu-id="575bf-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="575bf-114">-DatabaseCredential</span></span>
<span data-ttu-id="575bf-115">Poświadczenia uwierzytelniania SQL bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="575bf-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="575bf-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="575bf-116">-DatabaseName</span></span>
<span data-ttu-id="575bf-117">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="575bf-117">SQL Database name.</span></span>

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

### <span data-ttu-id="575bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575bf-118">-DefaultProfile</span></span>
<span data-ttu-id="575bf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="575bf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="575bf-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="575bf-120">-IntervalInSeconds</span></span>
<span data-ttu-id="575bf-121">Częstotliwość (w sekundach) wykonywania synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="575bf-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="575bf-122">Wartość domyślna to-1, co oznacza, że synchronizacja automatyczna nie jest włączona.</span><span class="sxs-lookup"><span data-stu-id="575bf-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="575bf-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="575bf-123">-Name</span></span>
<span data-ttu-id="575bf-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="575bf-124">The sync group name.</span></span>

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

### <span data-ttu-id="575bf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="575bf-125">-ResourceGroupName</span></span>
<span data-ttu-id="575bf-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="575bf-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="575bf-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="575bf-127">-SchemaFile</span></span>
<span data-ttu-id="575bf-128">Ścieżka pliku schematu.</span><span class="sxs-lookup"><span data-stu-id="575bf-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="575bf-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="575bf-129">-ServerName</span></span>
<span data-ttu-id="575bf-130">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="575bf-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="575bf-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="575bf-131">-Confirm</span></span>
<span data-ttu-id="575bf-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="575bf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="575bf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="575bf-133">-WhatIf</span></span>
<span data-ttu-id="575bf-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="575bf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="575bf-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="575bf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="575bf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575bf-136">CommonParameters</span></span>
<span data-ttu-id="575bf-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="575bf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575bf-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="575bf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575bf-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="575bf-139">INPUTS</span></span>

### <span data-ttu-id="575bf-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="575bf-140">None</span></span>
<span data-ttu-id="575bf-141">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="575bf-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="575bf-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="575bf-142">OUTPUTS</span></span>

### <span data-ttu-id="575bf-143">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="575bf-143">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="575bf-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="575bf-144">NOTES</span></span>

## <span data-ttu-id="575bf-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="575bf-145">RELATED LINKS</span></span>

[<span data-ttu-id="575bf-146">Nowe — AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="575bf-146">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="575bf-147">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="575bf-147">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="575bf-148">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="575bf-148">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

