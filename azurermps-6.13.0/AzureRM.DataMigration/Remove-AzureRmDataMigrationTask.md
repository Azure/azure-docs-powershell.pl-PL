---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: 295ac647bcbe04e26e761e4fdf8fe2bd30282218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553591"
---
# <span data-ttu-id="0bb08-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="0bb08-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="0bb08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0bb08-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb08-103">Usuwa zadanie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb08-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bb08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0bb08-104">SYNTAX</span></span>

### <span data-ttu-id="0bb08-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0bb08-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bb08-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bb08-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bb08-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bb08-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bb08-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0bb08-108">DESCRIPTION</span></span>
<span data-ttu-id="0bb08-109">Polecenie cmdlet Remove-AzureRmDataMigrationTask usuwa zadanie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb08-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="0bb08-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0bb08-110">EXAMPLES</span></span>

### <span data-ttu-id="0bb08-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0bb08-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="0bb08-112">W powyższym przykładzie usunięto zadanie usługi migracji bazy danych platformy Azure o nazwie TestTask z usługi Azure na podstawie parametru nazwy zadania.</span><span class="sxs-lookup"><span data-stu-id="0bb08-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="0bb08-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0bb08-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="0bb08-114">W powyższym przykładzie zadanie usługi migracji bazy danych platformy Azure zostało usunięte na podstawie przekazanego obiektu PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="0bb08-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="0bb08-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0bb08-115">PARAMETERS</span></span>

### <span data-ttu-id="0bb08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb08-116">-DefaultProfile</span></span>
<span data-ttu-id="0bb08-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb08-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bb08-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0bb08-118">-Force</span></span>
<span data-ttu-id="0bb08-119">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="0bb08-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0bb08-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0bb08-120">-InputObject</span></span>
<span data-ttu-id="0bb08-121">Obiekt PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="0bb08-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bb08-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0bb08-122">-Name</span></span>
<span data-ttu-id="0bb08-123">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="0bb08-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb08-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bb08-124">-PassThru</span></span>
<span data-ttu-id="0bb08-125">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="0bb08-125">Returns an true/false.</span></span>
<span data-ttu-id="0bb08-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0bb08-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0bb08-127">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="0bb08-127">-ProjectName</span></span>
<span data-ttu-id="0bb08-128">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="0bb08-128">The name of the project.</span></span>

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

### <span data-ttu-id="0bb08-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bb08-129">-ResourceGroupName</span></span>
<span data-ttu-id="0bb08-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0bb08-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="0bb08-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bb08-131">-ResourceId</span></span>
<span data-ttu-id="0bb08-132">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="0bb08-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="0bb08-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0bb08-133">-ServiceName</span></span>
<span data-ttu-id="0bb08-134">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0bb08-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="0bb08-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0bb08-135">-Confirm</span></span>
<span data-ttu-id="0bb08-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bb08-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bb08-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bb08-137">-WhatIf</span></span>
<span data-ttu-id="0bb08-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bb08-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bb08-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0bb08-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bb08-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb08-140">CommonParameters</span></span>
<span data-ttu-id="0bb08-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb08-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb08-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb08-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb08-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bb08-143">INPUTS</span></span>

### <span data-ttu-id="0bb08-144">Microsoft. Azure. Commands. datamigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="0bb08-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="0bb08-145">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0bb08-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0bb08-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0bb08-146">System.String</span></span>

## <span data-ttu-id="0bb08-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0bb08-147">OUTPUTS</span></span>

### <span data-ttu-id="0bb08-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0bb08-148">System.Boolean</span></span>

## <span data-ttu-id="0bb08-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0bb08-149">NOTES</span></span>

## <span data-ttu-id="0bb08-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bb08-150">RELATED LINKS</span></span>
