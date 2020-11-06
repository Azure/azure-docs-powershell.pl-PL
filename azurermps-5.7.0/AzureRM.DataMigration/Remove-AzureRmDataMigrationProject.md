---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 8ec046df13302ece90e57bcb722816f2019ff2e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552920"
---
# <span data-ttu-id="9577a-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="9577a-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="9577a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9577a-102">SYNOPSIS</span></span>
<span data-ttu-id="9577a-103">Usuwa projekt usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9577a-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9577a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9577a-104">SYNTAX</span></span>

### <span data-ttu-id="9577a-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9577a-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9577a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9577a-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9577a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9577a-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9577a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9577a-108">DESCRIPTION</span></span>
<span data-ttu-id="9577a-109">Polecenie cmdlet Remove-AzureRmDataMigrationProject usuwa projekt usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9577a-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="9577a-110">Podanie parametru DeleteRunningTask powoduje usunięcie wszystkich zadań usługi migracji bazy danych platformy Azure skojarzonych z tym projektem, który jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="9577a-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="9577a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9577a-111">EXAMPLES</span></span>

### <span data-ttu-id="9577a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9577a-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="9577a-113">W powyższym przykładzie usunięto projekt usługi migracji bazy danych platformy Azure o nazwie myDMProject z usługi Azure na podstawie nazwy jako parametru wejściowego</span><span class="sxs-lookup"><span data-stu-id="9577a-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="9577a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9577a-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="9577a-115">W powyższym przykładzie usunięto projekt usługi migracji bazy danych platformy Azure oparty na obiekcie PSProject jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="9577a-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="9577a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9577a-116">PARAMETERS</span></span>

### <span data-ttu-id="9577a-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9577a-117">-Confirm</span></span>
<span data-ttu-id="9577a-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9577a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9577a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9577a-119">-DefaultProfile</span></span>
<span data-ttu-id="9577a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9577a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9577a-121">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="9577a-121">-DeleteRunningTask</span></span>
<span data-ttu-id="9577a-122">Usuwanie uruchomionego zadania</span><span class="sxs-lookup"><span data-stu-id="9577a-122">Delete any running task</span></span>

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

### <span data-ttu-id="9577a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9577a-123">-Force</span></span>
<span data-ttu-id="9577a-124">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="9577a-124">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9577a-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9577a-125">-InputObject</span></span>
<span data-ttu-id="9577a-126">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="9577a-126">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9577a-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9577a-127">-Name</span></span>
<span data-ttu-id="9577a-128">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="9577a-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9577a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9577a-129">-PassThru</span></span>
<span data-ttu-id="9577a-130">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="9577a-130">Returns an true/false.</span></span>
<span data-ttu-id="9577a-131">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9577a-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9577a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9577a-132">-ResourceGroupName</span></span>
<span data-ttu-id="9577a-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9577a-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="9577a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9577a-134">-ResourceId</span></span>
<span data-ttu-id="9577a-135">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="9577a-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="9577a-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9577a-136">-ServiceName</span></span>
<span data-ttu-id="9577a-137">Nazwa usługi migracji danych.</span><span class="sxs-lookup"><span data-stu-id="9577a-137">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="9577a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9577a-138">-WhatIf</span></span>
<span data-ttu-id="9577a-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9577a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9577a-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9577a-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="9577a-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9577a-141">INPUTS</span></span>

### <span data-ttu-id="9577a-142">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="9577a-142">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="9577a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9577a-143">System.String</span></span>


## <span data-ttu-id="9577a-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9577a-144">OUTPUTS</span></span>

### <span data-ttu-id="9577a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9577a-145">System.Boolean</span></span>


## <span data-ttu-id="9577a-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9577a-146">NOTES</span></span>

## <span data-ttu-id="9577a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9577a-147">RELATED LINKS</span></span>

