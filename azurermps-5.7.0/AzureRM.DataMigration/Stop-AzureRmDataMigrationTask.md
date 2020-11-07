---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: 7cf68cd27125580c6f0e57a7849c1fadc8cb47fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717333"
---
# <span data-ttu-id="e932a-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="e932a-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="e932a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e932a-102">SYNOPSIS</span></span>
<span data-ttu-id="e932a-103">Zatrzymuje zadanie usługi migracji bazy danych platformy Azure, które jest w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e932a-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e932a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e932a-104">SYNTAX</span></span>

### <span data-ttu-id="e932a-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e932a-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e932a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e932a-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e932a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e932a-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e932a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e932a-108">DESCRIPTION</span></span>
<span data-ttu-id="e932a-109">Polecenie cmdlet Stop-AzureRmDataMigrationTask zatrzymuje działanie migrowania bazy danych w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="e932a-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="e932a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e932a-110">EXAMPLES</span></span>

### <span data-ttu-id="e932a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e932a-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="e932a-112">W powyższym przykładzie zatrzymano zadanie usługi migracji bazy danych platformy Azure o nazwie myDMSTask skojarzonego z usługą Project myDMSProject i wystąpieniem usługi migracji bazy danych platformy Azure o nazwie</span><span class="sxs-lookup"><span data-stu-id="e932a-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="e932a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e932a-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="e932a-114">W powyższym przykładzie zatrzymano zadanie usługi migracji bazy danych platformy Azure przekazane jako parametr wejściowy PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="e932a-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="e932a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e932a-115">PARAMETERS</span></span>

### <span data-ttu-id="e932a-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e932a-116">-Confirm</span></span>
<span data-ttu-id="e932a-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e932a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e932a-118">-DefaultProfile</span></span>
<span data-ttu-id="e932a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e932a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e932a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e932a-120">-InputObject</span></span>
<span data-ttu-id="e932a-121">Obiekt PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="e932a-121">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e932a-122">-Name</span></span>
<span data-ttu-id="e932a-123">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="e932a-123">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e932a-124">-PassThru</span></span>
<span data-ttu-id="e932a-125">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="e932a-125">Returns an true/false.</span></span>
<span data-ttu-id="e932a-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e932a-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-127">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="e932a-127">-ProjectName</span></span>
<span data-ttu-id="e932a-128">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="e932a-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e932a-129">-ResourceGroupName</span></span>
<span data-ttu-id="e932a-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e932a-130">The name of the resource group .</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e932a-131">-ResourceId</span></span>
<span data-ttu-id="e932a-132">Identyfikator zasobu ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="e932a-132">ProjectTask Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e932a-133">-ServiceName</span></span>
<span data-ttu-id="e932a-134">Nazwa usługi migracji danych.</span><span class="sxs-lookup"><span data-stu-id="e932a-134">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e932a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e932a-135">-WhatIf</span></span>
<span data-ttu-id="e932a-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e932a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e932a-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e932a-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e932a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e932a-138">INPUTS</span></span>

### <span data-ttu-id="e932a-139">Microsoft. Azure. Commands. datamigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="e932a-139">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="e932a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e932a-140">System.String</span></span>


## <span data-ttu-id="e932a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e932a-141">OUTPUTS</span></span>

### <span data-ttu-id="e932a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e932a-142">System.Boolean</span></span>


## <span data-ttu-id="e932a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e932a-143">NOTES</span></span>

## <span data-ttu-id="e932a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e932a-144">RELATED LINKS</span></span>

