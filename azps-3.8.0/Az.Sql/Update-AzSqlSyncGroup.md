---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: cef62c85f42c2c9f0e6fbda776c58d6818659474
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895594"
---
# <span data-ttu-id="c367d-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c367d-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="c367d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c367d-102">SYNOPSIS</span></span>
<span data-ttu-id="c367d-103">Umożliwia zaktualizowanie grupy synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c367d-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="c367d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c367d-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c367d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c367d-105">DESCRIPTION</span></span>
<span data-ttu-id="c367d-106">Polecenie cmdlet **Update-AzSqlSyncGroup** modyfikuje właściwości grupy synchronizacji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c367d-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="c367d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c367d-107">EXAMPLES</span></span>

### <span data-ttu-id="c367d-108">Przykład 1: aktualizowanie grupy synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c367d-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="c367d-109">To polecenie aktualizuje grupę synchronizacji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c367d-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="c367d-110">"schema.json" to plik na dysku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="c367d-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="c367d-111">Zawiera ładunek schematu w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="c367d-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="c367d-112">Przykładem kodu JSON schematu jest: {"Tables": [{"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}; {"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}]; "cytowanie": "MayQuotedTable1"}, {"kolumny": [{"cytowana": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"" b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2 "}]," pocytowana ":" MayQuotedTable2 "}]," MasterSyncMemberName ": null}</span><span class="sxs-lookup"><span data-stu-id="c367d-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="c367d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c367d-113">PARAMETERS</span></span>

### <span data-ttu-id="c367d-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="c367d-114">-DatabaseCredential</span></span>
<span data-ttu-id="c367d-115">Poświadczenia uwierzytelniania SQL bazy danych centrum.</span><span class="sxs-lookup"><span data-stu-id="c367d-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="c367d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c367d-116">-DatabaseName</span></span>
<span data-ttu-id="c367d-117">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="c367d-117">SQL Database name.</span></span>

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

### <span data-ttu-id="c367d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c367d-118">-DefaultProfile</span></span>
<span data-ttu-id="c367d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c367d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c367d-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c367d-120">-IntervalInSeconds</span></span>
<span data-ttu-id="c367d-121">Częstotliwość (w sekundach) wykonywania synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="c367d-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="c367d-122">Wartość domyślna to-1, co oznacza, że synchronizacja automatyczna nie jest włączona.</span><span class="sxs-lookup"><span data-stu-id="c367d-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="c367d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c367d-123">-Name</span></span>
<span data-ttu-id="c367d-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="c367d-124">The sync group name.</span></span>

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

### <span data-ttu-id="c367d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c367d-125">-ResourceGroupName</span></span>
<span data-ttu-id="c367d-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c367d-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="c367d-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="c367d-127">-SchemaFile</span></span>
<span data-ttu-id="c367d-128">Ścieżka pliku schematu.</span><span class="sxs-lookup"><span data-stu-id="c367d-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="c367d-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c367d-129">-ServerName</span></span>
<span data-ttu-id="c367d-130">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c367d-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="c367d-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c367d-131">-Confirm</span></span>
<span data-ttu-id="c367d-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c367d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c367d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c367d-133">-WhatIf</span></span>
<span data-ttu-id="c367d-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c367d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c367d-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c367d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c367d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c367d-136">CommonParameters</span></span>
<span data-ttu-id="c367d-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c367d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c367d-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c367d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c367d-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c367d-139">INPUTS</span></span>

### <span data-ttu-id="c367d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c367d-140">System.String</span></span>

## <span data-ttu-id="c367d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c367d-141">OUTPUTS</span></span>

### <span data-ttu-id="c367d-142">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="c367d-142">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="c367d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c367d-143">NOTES</span></span>

## <span data-ttu-id="c367d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c367d-144">RELATED LINKS</span></span>

[<span data-ttu-id="c367d-145">Nowe — AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c367d-145">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="c367d-146">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c367d-146">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="c367d-147">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c367d-147">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

