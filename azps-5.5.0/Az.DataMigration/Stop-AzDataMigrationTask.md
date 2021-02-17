---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198082"
---
# <span data-ttu-id="c4e7a-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c4e7a-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="c4e7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e7a-103">Zatrzymuje zadanie usługi migracji bazy danych Azure, które znajduje się w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="c4e7a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c4e7a-104">SYNTAX</span></span>

### <span data-ttu-id="c4e7a-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c4e7a-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e7a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4e7a-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e7a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4e7a-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4e7a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c4e7a-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e7a-109">Stop-AzDataMigrationTask polecenie cmdlet zatrzymuje aktywność migracji bazy danych w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="c4e7a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c4e7a-110">EXAMPLES</span></span>

### <span data-ttu-id="c4e7a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c4e7a-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="c4e7a-112">Powyższy przykład zatrzymuje zadanie Usługi migracji bazy danych Azure o nazwie myDMSTask skojarzone z wystąpieniem programu Project myDMSProject i usługą migracji bazy danych Azure o nazwie TestService</span><span class="sxs-lookup"><span data-stu-id="c4e7a-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="c4e7a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c4e7a-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="c4e7a-114">Powyższy przykład zatrzymuje zadanie Usługi migracji bazy danych Azure przekazane jako parametr wejściowy OBIEKTU PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="c4e7a-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="c4e7a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4e7a-115">PARAMETERS</span></span>

### <span data-ttu-id="c4e7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e7a-116">-DefaultProfile</span></span>
<span data-ttu-id="c4e7a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4e7a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4e7a-118">-InputObject</span></span>
<span data-ttu-id="c4e7a-119">Obiekt PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="c4e7a-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c4e7a-120">-Name</span></span>
<span data-ttu-id="c4e7a-121">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-121">The name of the task.</span></span>

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

### <span data-ttu-id="c4e7a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4e7a-122">-PassThru</span></span>
<span data-ttu-id="c4e7a-123">Zwraca wartość prawda/fałsz.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-123">Returns an true/false.</span></span>
<span data-ttu-id="c4e7a-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c4e7a-125">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="c4e7a-125">-ProjectName</span></span>
<span data-ttu-id="c4e7a-126">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-126">The name of the project.</span></span>

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

### <span data-ttu-id="c4e7a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e7a-127">-ResourceGroupName</span></span>
<span data-ttu-id="c4e7a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="c4e7a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4e7a-129">-ResourceId</span></span>
<span data-ttu-id="c4e7a-130">Identyfikator zasobu projecttask.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="c4e7a-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c4e7a-131">-ServiceName</span></span>
<span data-ttu-id="c4e7a-132">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c4e7a-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4e7a-133">-Confirm</span></span>
<span data-ttu-id="c4e7a-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4e7a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4e7a-135">-WhatIf</span></span>
<span data-ttu-id="c4e7a-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4e7a-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4e7a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e7a-138">CommonParameters</span></span>
<span data-ttu-id="c4e7a-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e7a-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e7a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e7a-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4e7a-141">INPUTS</span></span>

### <span data-ttu-id="c4e7a-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="c4e7a-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="c4e7a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c4e7a-143">System.String</span></span>

## <span data-ttu-id="c4e7a-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4e7a-144">OUTPUTS</span></span>

### <span data-ttu-id="c4e7a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4e7a-145">System.Boolean</span></span>

## <span data-ttu-id="c4e7a-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c4e7a-146">NOTES</span></span>

## <span data-ttu-id="c4e7a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4e7a-147">RELATED LINKS</span></span>
