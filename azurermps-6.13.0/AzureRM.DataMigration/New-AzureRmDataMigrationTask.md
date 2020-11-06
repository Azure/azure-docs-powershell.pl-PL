---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 8352f7a63e40986e27c4b521dca58aaf003679bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552103"
---
# <span data-ttu-id="794bc-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="794bc-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="794bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="794bc-102">SYNOPSIS</span></span>
<span data-ttu-id="794bc-103">Tworzy i rozpoczyna zadanie migracji danych w usłudze migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="794bc-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="794bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="794bc-104">SYNTAX</span></span>

### <span data-ttu-id="794bc-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="794bc-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="794bc-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="794bc-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="794bc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="794bc-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="794bc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="794bc-108">DESCRIPTION</span></span>
<span data-ttu-id="794bc-109">Polecenie cmdlet New-AzureRmDataMigrationTask służy do tworzenia zadania migracji danych.</span><span class="sxs-lookup"><span data-stu-id="794bc-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="794bc-110">To polecenie cmdlet przyjmuje parametry dla modułu wyliczającego typ zadania, grupę zasobów platformy Azure, nazwę skojarzonej usługi migracji bazy danych platformy Azure i projektu jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="794bc-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="794bc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="794bc-111">EXAMPLES</span></span>

### <span data-ttu-id="794bc-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="794bc-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```

<span data-ttu-id="794bc-113">Ten przykładowy skrypt przedstawia sposób tworzenia nowego zadania migracji danych o nazwie MyMigrationTask w projekcie o nazwie myDMSProject i usługi o nazwie TestService.</span><span class="sxs-lookup"><span data-stu-id="794bc-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="794bc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="794bc-114">PARAMETERS</span></span>

### <span data-ttu-id="794bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="794bc-115">-DefaultProfile</span></span>
<span data-ttu-id="794bc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="794bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="794bc-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="794bc-117">-InputObject</span></span>
<span data-ttu-id="794bc-118">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="794bc-118">PSProject Object.</span></span>

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

### <span data-ttu-id="794bc-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="794bc-119">-Name</span></span>
<span data-ttu-id="794bc-120">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="794bc-120">The name of the task.</span></span>

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

### <span data-ttu-id="794bc-121">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="794bc-121">-ProjectName</span></span>
<span data-ttu-id="794bc-122">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="794bc-122">The name of the project.</span></span>

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

### <span data-ttu-id="794bc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="794bc-123">-ResourceGroupName</span></span>
<span data-ttu-id="794bc-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="794bc-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="794bc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="794bc-125">-ResourceId</span></span>
<span data-ttu-id="794bc-126">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="794bc-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="794bc-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="794bc-127">-ServiceName</span></span>
<span data-ttu-id="794bc-128">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="794bc-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="794bc-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="794bc-129">-TaskType</span></span>
<span data-ttu-id="794bc-130">Typ zadania.</span><span class="sxs-lookup"><span data-stu-id="794bc-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="794bc-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="794bc-131">-Confirm</span></span>
<span data-ttu-id="794bc-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="794bc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="794bc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="794bc-133">-WhatIf</span></span>
<span data-ttu-id="794bc-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="794bc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="794bc-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="794bc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="794bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794bc-136">CommonParameters</span></span>
<span data-ttu-id="794bc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="794bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794bc-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="794bc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794bc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="794bc-139">INPUTS</span></span>

### <span data-ttu-id="794bc-140">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="794bc-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="794bc-141">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="794bc-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="794bc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="794bc-142">System.String</span></span>

## <span data-ttu-id="794bc-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="794bc-143">OUTPUTS</span></span>

### <span data-ttu-id="794bc-144">Microsoft. Azure. Commands. datamigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="794bc-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="794bc-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="794bc-145">NOTES</span></span>

## <span data-ttu-id="794bc-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="794bc-146">RELATED LINKS</span></span>
