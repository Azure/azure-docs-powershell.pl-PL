---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223542"
---
# <span data-ttu-id="80291-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="80291-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="80291-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80291-102">SYNOPSIS</span></span>
<span data-ttu-id="80291-103">Usuwa zadanie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80291-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="80291-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80291-104">SYNTAX</span></span>

### <span data-ttu-id="80291-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="80291-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80291-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80291-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80291-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80291-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80291-108">Opis</span><span class="sxs-lookup"><span data-stu-id="80291-108">DESCRIPTION</span></span>
<span data-ttu-id="80291-109">Polecenie cmdlet Remove-AzDataMigrationTask usuwa zadanie usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80291-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="80291-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80291-110">EXAMPLES</span></span>

### <span data-ttu-id="80291-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80291-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="80291-112">W powyższym przykładzie usunięto zadanie usługi migracji bazy danych platformy Azure o nazwie TestTask z usługi Azure na podstawie parametru nazwy zadania.</span><span class="sxs-lookup"><span data-stu-id="80291-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="80291-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="80291-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="80291-114">W powyższym przykładzie zadanie usługi migracji bazy danych platformy Azure zostało usunięte na podstawie przekazanego obiektu PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="80291-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="80291-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80291-115">PARAMETERS</span></span>

### <span data-ttu-id="80291-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80291-116">-DefaultProfile</span></span>
<span data-ttu-id="80291-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80291-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80291-118">-Force</span><span class="sxs-lookup"><span data-stu-id="80291-118">-Force</span></span>
<span data-ttu-id="80291-119">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="80291-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="80291-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="80291-120">-InputObject</span></span>
<span data-ttu-id="80291-121">Obiekt PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="80291-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="80291-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="80291-122">-Name</span></span>
<span data-ttu-id="80291-123">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="80291-123">The name of the task.</span></span>

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

### <span data-ttu-id="80291-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80291-124">-PassThru</span></span>
<span data-ttu-id="80291-125">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="80291-125">Returns an true/false.</span></span>
<span data-ttu-id="80291-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="80291-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="80291-127">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="80291-127">-ProjectName</span></span>
<span data-ttu-id="80291-128">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="80291-128">The name of the project.</span></span>

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

### <span data-ttu-id="80291-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80291-129">-ResourceGroupName</span></span>
<span data-ttu-id="80291-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="80291-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="80291-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80291-131">-ResourceId</span></span>
<span data-ttu-id="80291-132">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="80291-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="80291-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="80291-133">-ServiceName</span></span>
<span data-ttu-id="80291-134">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="80291-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="80291-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80291-135">-Confirm</span></span>
<span data-ttu-id="80291-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80291-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80291-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80291-137">-WhatIf</span></span>
<span data-ttu-id="80291-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80291-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80291-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80291-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80291-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80291-140">CommonParameters</span></span>
<span data-ttu-id="80291-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80291-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80291-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80291-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80291-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80291-143">INPUTS</span></span>

### <span data-ttu-id="80291-144">Microsoft. Azure. Commands. datamigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="80291-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="80291-145">System. String</span><span class="sxs-lookup"><span data-stu-id="80291-145">System.String</span></span>

## <span data-ttu-id="80291-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80291-146">OUTPUTS</span></span>

### <span data-ttu-id="80291-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80291-147">System.Boolean</span></span>

## <span data-ttu-id="80291-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80291-148">NOTES</span></span>

## <span data-ttu-id="80291-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80291-149">RELATED LINKS</span></span>
