---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7fe59a6ae103da1fa0ff40bfd300fdbf183fea33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195906"
---
# <span data-ttu-id="3a1e1-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="3a1e1-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="3a1e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1e1-103">Uruchamia usługę ponownego odtwarzania dziennika z parametrami.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="3a1e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a1e1-104">SYNTAX</span></span>

### <span data-ttu-id="3a1e1-105">LogReplayInstanceDatabaseFromInputParameters (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3a1e1-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a1e1-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="3a1e1-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a1e1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a1e1-107">DESCRIPTION</span></span>
<span data-ttu-id="3a1e1-108">Polecenie **cmdlet Start-AzSqlInstanceDatabaseLogReplay** inicjuje uruchomienie usługi ponownego odtwarzania dziennika.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="3a1e1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a1e1-109">EXAMPLES</span></span>

### <span data-ttu-id="3a1e1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a1e1-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="3a1e1-111">To polecenie spowoduje utworzenie nowej zarządzanej bazy danych i rozpoczęcie przywracania kopii zapasowych z danego kontenera do momentu przywrócenia pliku last_backup.bak.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="3a1e1-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3a1e1-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="3a1e1-113">To polecenie utworzy nową zarządzaną bazę danych i rozpocznie przywracanie kopii zapasowych z danego kontenera, Complete-AzSqlInstanceDatabaseLogReplay zostanie wywołana ostatnia poszukiwana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="3a1e1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a1e1-114">PARAMETERS</span></span>

### <span data-ttu-id="3a1e1-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3a1e1-115">-AsJob</span></span>
<span data-ttu-id="3a1e1-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3a1e1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a1e1-117">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="3a1e1-117">-AutoCompleteRestore</span></span>
<span data-ttu-id="3a1e1-118">Wskaźnik, czy autouzupełniać przywracanie po ukończeniu, czy nie.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-118">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="3a1e1-119">— sortowanie</span><span class="sxs-lookup"><span data-stu-id="3a1e1-119">-Collation</span></span>
<span data-ttu-id="3a1e1-120">Sortowanie bazy danych wystąpienia, która ma być w użyciu.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-120">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="3a1e1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1e1-121">-DefaultProfile</span></span>
<span data-ttu-id="3a1e1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a1e1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a1e1-123">-InputObject</span></span>
<span data-ttu-id="3a1e1-124">Obiekt bazy danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-124">The instance database object.</span></span>

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

### <span data-ttu-id="3a1e1-125">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3a1e1-125">-InstanceName</span></span>
<span data-ttu-id="3a1e1-126">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-126">The name of the instance.</span></span>

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

### <span data-ttu-id="3a1e1-127">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="3a1e1-127">-LastBackupName</span></span>
<span data-ttu-id="3a1e1-128">Nazwa ostatniego pliku kopii zapasowej do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-128">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="3a1e1-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3a1e1-129">-Name</span></span>
<span data-ttu-id="3a1e1-130">Nazwa bazy danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-130">The name of the instance database.</span></span>

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

### <span data-ttu-id="3a1e1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a1e1-131">-PassThru</span></span>
<span data-ttu-id="3a1e1-132">Określa, czy grupa synchronizacji ma być zwracana.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-132">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="3a1e1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a1e1-133">-ResourceGroupName</span></span>
<span data-ttu-id="3a1e1-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a1e1-135">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="3a1e1-135">-StorageContainerSasToken</span></span>
<span data-ttu-id="3a1e1-136">Token Sas kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-136">The storage container Sas token.</span></span>

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

### <span data-ttu-id="3a1e1-137">— StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="3a1e1-137">-StorageContainerUri</span></span>
<span data-ttu-id="3a1e1-138">URI kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-138">The storage container URI.</span></span>

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

### <span data-ttu-id="3a1e1-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a1e1-139">-Confirm</span></span>
<span data-ttu-id="3a1e1-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a1e1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a1e1-141">-WhatIf</span></span>
<span data-ttu-id="3a1e1-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a1e1-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a1e1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1e1-144">CommonParameters</span></span>
<span data-ttu-id="3a1e1-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1e1-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a1e1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1e1-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a1e1-147">INPUTS</span></span>

### <span data-ttu-id="3a1e1-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3a1e1-148">System.String</span></span>

### <span data-ttu-id="3a1e1-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3a1e1-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="3a1e1-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a1e1-150">OUTPUTS</span></span>

### <span data-ttu-id="3a1e1-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3a1e1-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="3a1e1-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a1e1-152">NOTES</span></span>

## <span data-ttu-id="3a1e1-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a1e1-153">RELATED LINKS</span></span>
