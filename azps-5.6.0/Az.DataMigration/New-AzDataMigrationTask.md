---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 5e9e121e3210510ed073cacfe93d6ec196888db6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991397"
---
# <span data-ttu-id="7f76e-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="7f76e-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="7f76e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f76e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f76e-103">Tworzy i uruchamia zadanie migracji danych w usłudze migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="7f76e-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="7f76e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7f76e-104">SYNTAX</span></span>

### <span data-ttu-id="7f76e-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7f76e-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f76e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f76e-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f76e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f76e-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f76e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7f76e-108">DESCRIPTION</span></span>
<span data-ttu-id="7f76e-109">Polecenie New-AzDataMigrationTask umożliwia utworzenie zadania migracji danych.</span><span class="sxs-lookup"><span data-stu-id="7f76e-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="7f76e-110">To polecenie cmdlet pobiera parametry do wyliczenia typów zadań, grupy zasobów platformy Azure, nazwy skojarzonej usługi migracji bazy danych Azure i programu Project jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7f76e-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="7f76e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7f76e-111">EXAMPLES</span></span>

### <span data-ttu-id="7f76e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f76e-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="7f76e-113">W tym przykładowym skrypcie pokazano, jak utworzyć nowe zadanie migracji danych o nazwie MojeMigrationTask w projekcie o nazwie myDMSProject i usłudze o nazwie TestService.</span><span class="sxs-lookup"><span data-stu-id="7f76e-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="7f76e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f76e-114">PARAMETERS</span></span>

### <span data-ttu-id="7f76e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f76e-115">-DefaultProfile</span></span>
<span data-ttu-id="7f76e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f76e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f76e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f76e-117">-InputObject</span></span>
<span data-ttu-id="7f76e-118">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="7f76e-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f76e-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7f76e-119">-Name</span></span>
<span data-ttu-id="7f76e-120">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="7f76e-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f76e-121">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="7f76e-121">-ProjectName</span></span>
<span data-ttu-id="7f76e-122">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="7f76e-122">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f76e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f76e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7f76e-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f76e-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f76e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f76e-125">-ResourceId</span></span>
<span data-ttu-id="7f76e-126">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="7f76e-126">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f76e-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7f76e-127">-ServiceName</span></span>
<span data-ttu-id="7f76e-128">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7f76e-128">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f76e-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="7f76e-129">-TaskType</span></span>
<span data-ttu-id="7f76e-130">Typ zadania.</span><span class="sxs-lookup"><span data-stu-id="7f76e-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f76e-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="7f76e-131">-MigrationValidation</span></span> 
<span data-ttu-id="7f76e-132">Obiekt odpowiedzi zadania według wywołania sprawdzania poprawności (opcjonalny, ale zalecany).</span><span class="sxs-lookup"><span data-stu-id="7f76e-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f76e-133">— Czekanie</span><span class="sxs-lookup"><span data-stu-id="7f76e-133">-Wait</span></span>
<span data-ttu-id="7f76e-134">Czy należy zaczekać na zakończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="7f76e-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="7f76e-135">Jeśli flaga jest ustawiona, sprawdza co sekundy do zakończenia zadania i zwraca użytkownikowi właściwości zadania, gdzie można sprawdzić dane wyjściowe lub błędy.</span><span class="sxs-lookup"><span data-stu-id="7f76e-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="7f76e-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f76e-136">-Confirm</span></span>
<span data-ttu-id="7f76e-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7f76e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f76e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f76e-138">-WhatIf</span></span>
<span data-ttu-id="7f76e-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f76e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f76e-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7f76e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f76e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f76e-141">CommonParameters</span></span>
<span data-ttu-id="7f76e-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f76e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f76e-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f76e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f76e-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f76e-144">INPUTS</span></span>

### <span data-ttu-id="7f76e-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="7f76e-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="7f76e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7f76e-146">System.String</span></span>

## <span data-ttu-id="7f76e-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f76e-147">OUTPUTS</span></span>

### <span data-ttu-id="7f76e-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="7f76e-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="7f76e-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7f76e-149">NOTES</span></span>

## <span data-ttu-id="7f76e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f76e-150">RELATED LINKS</span></span>
