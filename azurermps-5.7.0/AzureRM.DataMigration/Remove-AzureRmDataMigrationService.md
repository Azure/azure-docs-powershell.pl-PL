---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: dde0044642f81c098358cd86cabe8c066240a215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549020"
---
# <span data-ttu-id="859a1-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="859a1-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="859a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="859a1-102">SYNOPSIS</span></span>
<span data-ttu-id="859a1-103">Usuwa wystąpienie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="859a1-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="859a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="859a1-104">SYNTAX</span></span>

### <span data-ttu-id="859a1-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="859a1-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="859a1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="859a1-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="859a1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="859a1-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="859a1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="859a1-108">DESCRIPTION</span></span>
<span data-ttu-id="859a1-109">Polecenie cmdlet Remove-AzureRmDataMigrationService powoduje usunięcie wystąpienia usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="859a1-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="859a1-110">Podanie parametru DeleteRunningTask powoduje usunięcie wszystkich zadań usługi migracji bazy danych platformy Azure skojarzonych z usuwaną usługą.</span><span class="sxs-lookup"><span data-stu-id="859a1-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="859a1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="859a1-111">EXAMPLES</span></span>

### <span data-ttu-id="859a1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="859a1-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="859a1-113">W powyższym przykładzie usunięto wystąpienie usługi migracji bazy danych platformy Azure o nazwie TestService, która jest uwzględniona w grupie zasobów platformy Azure o nazwie moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="859a1-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="859a1-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="859a1-114">PARAMETERS</span></span>

### <span data-ttu-id="859a1-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="859a1-115">-Confirm</span></span>
<span data-ttu-id="859a1-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="859a1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="859a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859a1-117">-DefaultProfile</span></span>
<span data-ttu-id="859a1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="859a1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="859a1-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="859a1-119">-DeleteRunningTask</span></span>
<span data-ttu-id="859a1-120">Usuwanie uruchomionego zadania</span><span class="sxs-lookup"><span data-stu-id="859a1-120">Delete any running task</span></span>

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

### <span data-ttu-id="859a1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="859a1-121">-Force</span></span>
<span data-ttu-id="859a1-122">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="859a1-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="859a1-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="859a1-123">-InputObject</span></span>
<span data-ttu-id="859a1-124">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="859a1-124">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="859a1-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="859a1-125">-Name</span></span>
<span data-ttu-id="859a1-126">Nazwa usługi migracji danych.</span><span class="sxs-lookup"><span data-stu-id="859a1-126">The name of the Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859a1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="859a1-127">-PassThru</span></span>
<span data-ttu-id="859a1-128">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="859a1-128">Returns an true/false.</span></span>
<span data-ttu-id="859a1-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="859a1-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="859a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="859a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="859a1-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="859a1-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="859a1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="859a1-132">-ResourceId</span></span>
<span data-ttu-id="859a1-133">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="859a1-133">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="859a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859a1-134">-WhatIf</span></span>
<span data-ttu-id="859a1-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="859a1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="859a1-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="859a1-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="859a1-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="859a1-137">INPUTS</span></span>

### <span data-ttu-id="859a1-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="859a1-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="859a1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="859a1-139">System.String</span></span>


## <span data-ttu-id="859a1-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="859a1-140">OUTPUTS</span></span>

### <span data-ttu-id="859a1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="859a1-141">System.Boolean</span></span>


## <span data-ttu-id="859a1-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="859a1-142">NOTES</span></span>

## <span data-ttu-id="859a1-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="859a1-143">RELATED LINKS</span></span>


