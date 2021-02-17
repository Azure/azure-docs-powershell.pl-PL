---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196251"
---
# <span data-ttu-id="edf47-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="edf47-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="edf47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edf47-102">SYNOPSIS</span></span>
<span data-ttu-id="edf47-103">Kończy usługę ponownego odtwarzania dziennika dla danej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="edf47-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="edf47-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="edf47-104">SYNTAX</span></span>

### <span data-ttu-id="edf47-105">LogReplayInstanceDatabaseFromInputParameters (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="edf47-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edf47-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="edf47-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edf47-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="edf47-107">DESCRIPTION</span></span>
<span data-ttu-id="edf47-108">Polecenie **cmdlet Complete-AzSqlInstanceDatabaseLogReplay** kończy usługę ponownego odtwarzania dziennika w danej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="edf47-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="edf47-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="edf47-109">EXAMPLES</span></span>

### <span data-ttu-id="edf47-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="edf47-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="edf47-111">To polecenie spowoduje ukończenie usługi ponownego odtwarzania dziennika dla danej bazy danych po przywróceniu ostatniej kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="edf47-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="edf47-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edf47-112">PARAMETERS</span></span>

### <span data-ttu-id="edf47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf47-113">-DefaultProfile</span></span>
<span data-ttu-id="edf47-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="edf47-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edf47-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edf47-115">-InputObject</span></span>
<span data-ttu-id="edf47-116">Obiekt bazy danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="edf47-116">The instance database object.</span></span>

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

### <span data-ttu-id="edf47-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="edf47-117">-InstanceName</span></span>
<span data-ttu-id="edf47-118">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="edf47-118">The name of the instance.</span></span>

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

### <span data-ttu-id="edf47-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="edf47-119">-LastBackupName</span></span>
<span data-ttu-id="edf47-120">Nazwa ostatniego pliku kopii zapasowej do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="edf47-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="edf47-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="edf47-121">-Name</span></span>
<span data-ttu-id="edf47-122">Nazwa bazy danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="edf47-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="edf47-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edf47-123">-PassThru</span></span>
<span data-ttu-id="edf47-124">Określa, czy grupa synchronizacji ma być zwracana.</span><span class="sxs-lookup"><span data-stu-id="edf47-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="edf47-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf47-125">-ResourceGroupName</span></span>
<span data-ttu-id="edf47-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="edf47-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="edf47-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edf47-127">-Confirm</span></span>
<span data-ttu-id="edf47-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="edf47-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edf47-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edf47-129">-WhatIf</span></span>
<span data-ttu-id="edf47-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edf47-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edf47-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="edf47-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edf47-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf47-132">CommonParameters</span></span>
<span data-ttu-id="edf47-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf47-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf47-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edf47-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf47-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edf47-135">INPUTS</span></span>

### <span data-ttu-id="edf47-136">System.String</span><span class="sxs-lookup"><span data-stu-id="edf47-136">System.String</span></span>

### <span data-ttu-id="edf47-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="edf47-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="edf47-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="edf47-138">OUTPUTS</span></span>

## <span data-ttu-id="edf47-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="edf47-139">NOTES</span></span>

## <span data-ttu-id="edf47-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edf47-140">RELATED LINKS</span></span>
