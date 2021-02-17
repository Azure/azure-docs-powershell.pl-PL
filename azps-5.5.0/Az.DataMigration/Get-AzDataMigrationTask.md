---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177075"
---
# <span data-ttu-id="bc863-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="bc863-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="bc863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc863-102">SYNOPSIS</span></span>
<span data-ttu-id="bc863-103">Pobiera obiekt PSProjectTask skojarzony z zadaniem migracji usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="bc863-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="bc863-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc863-104">SYNTAX</span></span>

### <span data-ttu-id="bc863-105">ListByComponent (Default)</span><span class="sxs-lookup"><span data-stu-id="bc863-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc863-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="bc863-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc863-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="bc863-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc863-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="bc863-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc863-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc863-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc863-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc863-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc863-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="bc863-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc863-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="bc863-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc863-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="bc863-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc863-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc863-114">DESCRIPTION</span></span>
<span data-ttu-id="bc863-115">Polecenie Get-AzDataMigrationTask pobiera właściwości skojarzone z zadaniem migracji usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="bc863-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="bc863-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc863-116">EXAMPLES</span></span>

### <span data-ttu-id="bc863-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc863-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="bc863-118">W powyższym przykładzie pokazano użycie polecenia cmdlet Get-AzDataMigrationTask w celu pobrania właściwości skojarzonych z zadaniem migracji usługi migracji bazy danych Azure na podstawie nazwy zadania przekazanej jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="bc863-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="bc863-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bc863-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="bc863-120">W powyższym przykładzie pokazano użycie polecenia cmdlet Get-AzDataMigrationTask w celu pobrania wszystkich zadań migracji skojarzonych z obiektem PSProject przekazanym jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="bc863-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="bc863-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc863-121">PARAMETERS</span></span>

### <span data-ttu-id="bc863-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc863-122">-DefaultProfile</span></span>
<span data-ttu-id="bc863-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc863-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc863-124">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="bc863-124">-Expand</span></span>
<span data-ttu-id="bc863-125">Rozwijanie danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="bc863-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc863-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc863-126">-InputObject</span></span>
<span data-ttu-id="bc863-127">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="bc863-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc863-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bc863-128">-Name</span></span>
<span data-ttu-id="bc863-129">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="bc863-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc863-130">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="bc863-130">-ProjectName</span></span>
<span data-ttu-id="bc863-131">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="bc863-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc863-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc863-132">-ResourceGroupName</span></span>
<span data-ttu-id="bc863-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bc863-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc863-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc863-134">-ResourceId</span></span>
<span data-ttu-id="bc863-135">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="bc863-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc863-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="bc863-136">-ResultType</span></span>
<span data-ttu-id="bc863-137">Rozwijanie danych wyjściowych danego typu wyników.</span><span class="sxs-lookup"><span data-stu-id="bc863-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc863-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bc863-138">-ServiceName</span></span>
<span data-ttu-id="bc863-139">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bc863-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc863-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="bc863-140">-TaskType</span></span>
<span data-ttu-id="bc863-141">Filtruj według typu Zadania.</span><span class="sxs-lookup"><span data-stu-id="bc863-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc863-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc863-142">CommonParameters</span></span>
<span data-ttu-id="bc863-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc863-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc863-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc863-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc863-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc863-145">INPUTS</span></span>

### <span data-ttu-id="bc863-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="bc863-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="bc863-147">System.String</span><span class="sxs-lookup"><span data-stu-id="bc863-147">System.String</span></span>

## <span data-ttu-id="bc863-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc863-148">OUTPUTS</span></span>

### <span data-ttu-id="bc863-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="bc863-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="bc863-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc863-150">NOTES</span></span>

## <span data-ttu-id="bc863-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc863-151">RELATED LINKS</span></span>
