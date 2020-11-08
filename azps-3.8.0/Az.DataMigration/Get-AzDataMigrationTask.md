---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051533"
---
# <span data-ttu-id="2bb7e-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2bb7e-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="2bb7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2bb7e-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb7e-103">Pobiera obiekt PSProjectTask skojarzony z zadaniem migracji usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="2bb7e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2bb7e-104">SYNTAX</span></span>

### <span data-ttu-id="2bb7e-105">ListByComponent (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2bb7e-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bb7e-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="2bb7e-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bb7e-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2bb7e-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bb7e-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="2bb7e-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bb7e-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="2bb7e-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bb7e-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2bb7e-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bb7e-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="2bb7e-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bb7e-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="2bb7e-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bb7e-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="2bb7e-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bb7e-114">Opis</span><span class="sxs-lookup"><span data-stu-id="2bb7e-114">DESCRIPTION</span></span>
<span data-ttu-id="2bb7e-115">Polecenie cmdlet Get-AzDataMigrationTask pobiera właściwości skojarzone z zadaniem migracji usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="2bb7e-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2bb7e-116">EXAMPLES</span></span>

### <span data-ttu-id="2bb7e-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2bb7e-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="2bb7e-118">Powyższy przykład ilustruje użycie polecenia cmdlet Get-AzDataMigrationTask w celu pobrania właściwości skojarzonych z zadaniem migracji usługi migracji bazy danych platformy Azure opartym na nazwie zadania przekazanej jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="2bb7e-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="2bb7e-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2bb7e-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="2bb7e-120">Powyższy przykład ilustruje użycie polecenia cmdlet Get-AzDataMigrationTask w celu pobrania wszystkich zadań migracji skojarzonych z obiektem PSProject przekazanym jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="2bb7e-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="2bb7e-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2bb7e-121">PARAMETERS</span></span>

### <span data-ttu-id="2bb7e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb7e-122">-DefaultProfile</span></span>
<span data-ttu-id="2bb7e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bb7e-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="2bb7e-124">-Expand</span></span>
<span data-ttu-id="2bb7e-125">Rozwijanie danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="2bb7e-125">Expand output</span></span>

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

### <span data-ttu-id="2bb7e-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2bb7e-126">-InputObject</span></span>
<span data-ttu-id="2bb7e-127">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-127">PSProject Object.</span></span>

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

### <span data-ttu-id="2bb7e-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2bb7e-128">-Name</span></span>
<span data-ttu-id="2bb7e-129">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-129">The name of the task.</span></span>

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

### <span data-ttu-id="2bb7e-130">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="2bb7e-130">-ProjectName</span></span>
<span data-ttu-id="2bb7e-131">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-131">The name of the project.</span></span>

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

### <span data-ttu-id="2bb7e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bb7e-132">-ResourceGroupName</span></span>
<span data-ttu-id="2bb7e-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="2bb7e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bb7e-134">-ResourceId</span></span>
<span data-ttu-id="2bb7e-135">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="2bb7e-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="2bb7e-136">-ResultType</span></span>
<span data-ttu-id="2bb7e-137">Rozwijanie danych wyjściowych danego typu wyników.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-137">Expand output of given result type.</span></span>

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

### <span data-ttu-id="2bb7e-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2bb7e-138">-ServiceName</span></span>
<span data-ttu-id="2bb7e-139">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="2bb7e-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="2bb7e-140">-TaskType</span></span>
<span data-ttu-id="2bb7e-141">Filtrowanie wedługtype zadania.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-141">Filter by TaskType.</span></span>

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

### <span data-ttu-id="2bb7e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb7e-142">CommonParameters</span></span>
<span data-ttu-id="2bb7e-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb7e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb7e-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bb7e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb7e-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bb7e-145">INPUTS</span></span>

### <span data-ttu-id="2bb7e-146">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="2bb7e-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="2bb7e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2bb7e-147">System.String</span></span>

## <span data-ttu-id="2bb7e-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2bb7e-148">OUTPUTS</span></span>

### <span data-ttu-id="2bb7e-149">Microsoft. Azure. Commands. datamigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="2bb7e-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="2bb7e-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2bb7e-150">NOTES</span></span>

## <span data-ttu-id="2bb7e-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2bb7e-151">RELATED LINKS</span></span>
