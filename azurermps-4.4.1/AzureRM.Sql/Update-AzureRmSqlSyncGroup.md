---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
ms.openlocfilehash: a530a9e99c698ca6b827df94b1966e4df065790d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549088"
---
# <span data-ttu-id="b12c5-101">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b12c5-101">Update-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="b12c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b12c5-102">SYNOPSIS</span></span>
<span data-ttu-id="b12c5-103">Umożliwia zaktualizowanie grupy synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b12c5-103">Updates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b12c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b12c5-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b12c5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b12c5-105">DESCRIPTION</span></span>
<span data-ttu-id="b12c5-106">Polecenie cmdlet **Update-AzureRmSqlSyncGroup** modyfikuje właściwości grupy synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b12c5-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="b12c5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b12c5-107">EXAMPLES</span></span>

### <span data-ttu-id="b12c5-108">Przykład 1: aktualizowanie grupy synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b12c5-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="b12c5-109">To polecenie aktualizuje grupę synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b12c5-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="b12c5-110">"schema.json" to plik na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="b12c5-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="b12c5-111">Zawiera ładunek Shema w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="b12c5-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="b12c5-112">Przykładem kodu JSON schematu jest: {"Tables": [{"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}; {"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "cytowanie": "MayQuotedTable1"}, {"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"" b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2 "}]," pocytowana ":" MayQuotedTable2 "}]," MasterSyncMemberName ": null}</span><span class="sxs-lookup"><span data-stu-id="b12c5-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="b12c5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b12c5-113">PARAMETERS</span></span>

### <span data-ttu-id="b12c5-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b12c5-114">-Confirm</span></span>
<span data-ttu-id="b12c5-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b12c5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b12c5-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="b12c5-116">-DatabaseCredential</span></span>
<span data-ttu-id="b12c5-117">Poświadczenia uwierzytelniania SQL bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="b12c5-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="b12c5-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b12c5-118">-DatabaseName</span></span>
<span data-ttu-id="b12c5-119">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b12c5-119">SQL Database name.</span></span>

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

### <span data-ttu-id="b12c5-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b12c5-120">-IntervalInSeconds</span></span>
<span data-ttu-id="b12c5-121">Częstotliwość (w sekundach) wykonywania synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="b12c5-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="b12c5-122">Wartość domyślna to-1, co oznacza, że synchronizacja automatyczna nie jest włączona.</span><span class="sxs-lookup"><span data-stu-id="b12c5-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="b12c5-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b12c5-123">-Name</span></span>
<span data-ttu-id="b12c5-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="b12c5-124">The sync group name.</span></span>

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

### <span data-ttu-id="b12c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b12c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="b12c5-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b12c5-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="b12c5-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="b12c5-127">-SchemaFile</span></span>
<span data-ttu-id="b12c5-128">Ścieżka pliku schematu.</span><span class="sxs-lookup"><span data-stu-id="b12c5-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="b12c5-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b12c5-129">-ServerName</span></span>
<span data-ttu-id="b12c5-130">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b12c5-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b12c5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b12c5-131">-WhatIf</span></span>
<span data-ttu-id="b12c5-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b12c5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b12c5-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b12c5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b12c5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b12c5-134">-DefaultProfile</span></span>
<span data-ttu-id="b12c5-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b12c5-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b12c5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b12c5-136">CommonParameters</span></span>
<span data-ttu-id="b12c5-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b12c5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b12c5-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b12c5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b12c5-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b12c5-139">INPUTS</span></span>

## <span data-ttu-id="b12c5-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b12c5-140">OUTPUTS</span></span>

### <span data-ttu-id="b12c5-141">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="b12c5-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="b12c5-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b12c5-142">NOTES</span></span>

## <span data-ttu-id="b12c5-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b12c5-143">RELATED LINKS</span></span>

[<span data-ttu-id="b12c5-144">Nowe — AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b12c5-144">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="b12c5-145">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b12c5-145">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="b12c5-146">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b12c5-146">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

