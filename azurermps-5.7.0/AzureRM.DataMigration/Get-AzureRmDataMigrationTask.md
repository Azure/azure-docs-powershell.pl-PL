---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: 5ca6edfa811a1b73cbdaae59e8d3b0e2f76cc15f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544375"
---
# <span data-ttu-id="2e3a8-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2e3a8-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="2e3a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3a8-103">Pobiera obiekt PSProjectTask skojarzony z zadaniem migracji usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e3a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e3a8-104">SYNTAX</span></span>

### <span data-ttu-id="2e3a8-105">ListByComponent (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e3a8-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2e3a8-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e3a8-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2e3a8-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e3a8-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2e3a8-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="2e3a8-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2e3a8-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e3a8-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2e3a8-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e3a8-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2e3a8-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="2e3a8-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2e3a8-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="2e3a8-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2e3a8-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="2e3a8-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="2e3a8-114">Opis</span><span class="sxs-lookup"><span data-stu-id="2e3a8-114">DESCRIPTION</span></span>
<span data-ttu-id="2e3a8-115">Polecenie cmdlet Get-AzureRmDataMigrationTask pobiera właściwości skojarzone z zadaniem migracji usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="2e3a8-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e3a8-116">EXAMPLES</span></span>

### <span data-ttu-id="2e3a8-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2e3a8-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="2e3a8-118">Powyższy przykład ilustruje użycie polecenia cmdlet Get-AzureRmDataMigrationTask w celu pobrania właściwości skojarzonych z zadaniem migracji usługi migracji bazy danych platformy Azure opartym na nazwie zadania przekazanej jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="2e3a8-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="2e3a8-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2e3a8-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="2e3a8-120">Powyższy przykład ilustruje użycie polecenia cmdlet Get-AzureRmDataMigrationTask w celu pobrania wszystkich zadań migracji skojarzonych z obiektem PSProject przekazanym jako parametr wejściowy</span><span class="sxs-lookup"><span data-stu-id="2e3a8-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="2e3a8-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e3a8-121">PARAMETERS</span></span>

### <span data-ttu-id="2e3a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3a8-122">-DefaultProfile</span></span>
<span data-ttu-id="2e3a8-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e3a8-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="2e3a8-124">-Expand</span></span>
<span data-ttu-id="2e3a8-125">Rozwijanie danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="2e3a8-125">Expand output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3a8-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e3a8-126">-InputObject</span></span>
<span data-ttu-id="2e3a8-127">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-127">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3a8-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e3a8-128">-Name</span></span>
<span data-ttu-id="2e3a8-129">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-129">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3a8-130">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="2e3a8-130">-ProjectName</span></span>
<span data-ttu-id="2e3a8-131">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-131">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3a8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e3a8-132">-ResourceGroupName</span></span>
<span data-ttu-id="2e3a8-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3a8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e3a8-134">-ResourceId</span></span>
<span data-ttu-id="2e3a8-135">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3a8-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="2e3a8-136">-ResultType</span></span>
<span data-ttu-id="2e3a8-137">Rozwijanie danych wyjściowych danego typu wyników.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-137">Expand output of given result type.</span></span>

```yaml
Type: ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3a8-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2e3a8-138">-ServiceName</span></span>
<span data-ttu-id="2e3a8-139">Nazwa usługi migracji danych.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-139">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3a8-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="2e3a8-140">-TaskType</span></span>
<span data-ttu-id="2e3a8-141">Filtrowanie wedługtype zadania.</span><span class="sxs-lookup"><span data-stu-id="2e3a8-141">Filter by TaskType.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="2e3a8-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e3a8-142">INPUTS</span></span>

### <span data-ttu-id="2e3a8-143">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="2e3a8-143">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="2e3a8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2e3a8-144">System.String</span></span>

## <span data-ttu-id="2e3a8-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e3a8-145">OUTPUTS</span></span>

### <span data-ttu-id="2e3a8-146">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. datamigration. MODELES. PSProjectTask, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="2e3a8-146">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2e3a8-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e3a8-147">NOTES</span></span>

## <span data-ttu-id="2e3a8-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e3a8-148">RELATED LINKS</span></span>

