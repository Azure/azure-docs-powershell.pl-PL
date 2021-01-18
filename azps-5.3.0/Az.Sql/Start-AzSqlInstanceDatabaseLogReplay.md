---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499761"
---
# <span data-ttu-id="2b79a-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="2b79a-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="2b79a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b79a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b79a-103">Uruchamia usługę powtarzania dziennika z podanymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="2b79a-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="2b79a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b79a-104">SYNTAX</span></span>

### <span data-ttu-id="2b79a-105">LogReplayInstanceDatabaseFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2b79a-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b79a-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="2b79a-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b79a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2b79a-107">DESCRIPTION</span></span>
<span data-ttu-id="2b79a-108">Polecenie cmdlet **Start-AzSqlInstanceDatabaseLogReplay** inicjuje uruchomienie usługi powtarzania dziennika.</span><span class="sxs-lookup"><span data-stu-id="2b79a-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="2b79a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b79a-109">EXAMPLES</span></span>

### <span data-ttu-id="2b79a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2b79a-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="2b79a-111">To polecenie utworzy nową zarządzaną bazę danych i rozpocznie przywracanie kopii zapasowych z danego kontenera do momentu przywrócenia last_backup. bak.</span><span class="sxs-lookup"><span data-stu-id="2b79a-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="2b79a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2b79a-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="2b79a-113">To polecenie utworzy nową zarządzaną bazę danych i rozpocznie przywracanie kopii zapasowych z danego kontenera do momentu wywołania Complete-AzSqlInstanceDatabaseLogReplay przy użyciu ostatniej odpowiedniej kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2b79a-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="2b79a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b79a-114">PARAMETERS</span></span>

### <span data-ttu-id="2b79a-115">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="2b79a-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="2b79a-116">Wskaźnik określający, czy ma być automatycznie uzupełniane przywracanie po zakończeniu.</span><span class="sxs-lookup"><span data-stu-id="2b79a-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="2b79a-117">— Sortowanie</span><span class="sxs-lookup"><span data-stu-id="2b79a-117">-Collation</span></span>
<span data-ttu-id="2b79a-118">Sortowanie bazy danych wystąpienia do użycia.</span><span class="sxs-lookup"><span data-stu-id="2b79a-118">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="2b79a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b79a-119">-DefaultProfile</span></span>
<span data-ttu-id="2b79a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b79a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b79a-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2b79a-121">-InputObject</span></span>
<span data-ttu-id="2b79a-122">Obiekt bazy danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="2b79a-122">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b79a-123">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2b79a-123">-InstanceName</span></span>
<span data-ttu-id="2b79a-124">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="2b79a-124">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b79a-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="2b79a-125">-LastBackupName</span></span>
<span data-ttu-id="2b79a-126">Nazwa ostatniego pliku kopii zapasowej, który ma zostać przywrócony.</span><span class="sxs-lookup"><span data-stu-id="2b79a-126">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="2b79a-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b79a-127">-Name</span></span>
<span data-ttu-id="2b79a-128">Nazwa bazy danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="2b79a-128">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b79a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b79a-129">-PassThru</span></span>
<span data-ttu-id="2b79a-130">Określa, czy ma być zwracana Grupa synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="2b79a-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="2b79a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b79a-131">-ResourceGroupName</span></span>
<span data-ttu-id="2b79a-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2b79a-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b79a-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="2b79a-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="2b79a-134">Token SAS kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="2b79a-134">The storage container Sas token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasToken

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b79a-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="2b79a-135">-StorageContainerUri</span></span>
<span data-ttu-id="2b79a-136">Identyfikator URI kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="2b79a-136">The storage container URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Storage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b79a-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b79a-137">-Confirm</span></span>
<span data-ttu-id="2b79a-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b79a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b79a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b79a-139">-WhatIf</span></span>
<span data-ttu-id="2b79a-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b79a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b79a-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b79a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b79a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b79a-142">CommonParameters</span></span>
<span data-ttu-id="2b79a-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b79a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b79a-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b79a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b79a-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b79a-145">INPUTS</span></span>

### <span data-ttu-id="2b79a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2b79a-146">System.String</span></span>

### <span data-ttu-id="2b79a-147">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2b79a-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="2b79a-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b79a-148">OUTPUTS</span></span>

### <span data-ttu-id="2b79a-149">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2b79a-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="2b79a-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b79a-150">NOTES</span></span>

## <span data-ttu-id="2b79a-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b79a-151">RELATED LINKS</span></span>
