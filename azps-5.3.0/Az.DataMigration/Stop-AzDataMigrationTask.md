---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377531"
---
# <span data-ttu-id="788f2-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="788f2-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="788f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="788f2-102">SYNOPSIS</span></span>
<span data-ttu-id="788f2-103">Zatrzymuje zadanie usługi migracji bazy danych platformy Azure, które jest w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="788f2-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="788f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="788f2-104">SYNTAX</span></span>

### <span data-ttu-id="788f2-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="788f2-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="788f2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="788f2-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="788f2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="788f2-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="788f2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="788f2-108">DESCRIPTION</span></span>
<span data-ttu-id="788f2-109">Polecenie cmdlet Stop-AzDataMigrationTask zatrzymuje działanie migrowania bazy danych w stanie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="788f2-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="788f2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="788f2-110">EXAMPLES</span></span>

### <span data-ttu-id="788f2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="788f2-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="788f2-112">W powyższym przykładzie zatrzymano zadanie usługi migracji bazy danych platformy Azure o nazwie myDMSTask skojarzonego z usługą Project myDMSProject i wystąpieniem usługi migracji bazy danych platformy Azure o nazwie</span><span class="sxs-lookup"><span data-stu-id="788f2-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="788f2-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="788f2-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="788f2-114">W powyższym przykładzie zatrzymano zadanie usługi migracji bazy danych platformy Azure przekazane jako parametr wejściowy PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="788f2-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="788f2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="788f2-115">PARAMETERS</span></span>

### <span data-ttu-id="788f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788f2-116">-DefaultProfile</span></span>
<span data-ttu-id="788f2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="788f2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="788f2-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="788f2-118">-InputObject</span></span>
<span data-ttu-id="788f2-119">Obiekt PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="788f2-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="788f2-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="788f2-120">-Name</span></span>
<span data-ttu-id="788f2-121">Nazwa zadania.</span><span class="sxs-lookup"><span data-stu-id="788f2-121">The name of the task.</span></span>

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

### <span data-ttu-id="788f2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="788f2-122">-PassThru</span></span>
<span data-ttu-id="788f2-123">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="788f2-123">Returns an true/false.</span></span>
<span data-ttu-id="788f2-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="788f2-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="788f2-125">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="788f2-125">-ProjectName</span></span>
<span data-ttu-id="788f2-126">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="788f2-126">The name of the project.</span></span>

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

### <span data-ttu-id="788f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="788f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="788f2-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="788f2-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="788f2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="788f2-129">-ResourceId</span></span>
<span data-ttu-id="788f2-130">Identyfikator zasobu ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="788f2-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="788f2-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="788f2-131">-ServiceName</span></span>
<span data-ttu-id="788f2-132">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="788f2-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="788f2-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="788f2-133">-Confirm</span></span>
<span data-ttu-id="788f2-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="788f2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="788f2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="788f2-135">-WhatIf</span></span>
<span data-ttu-id="788f2-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="788f2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="788f2-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="788f2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="788f2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788f2-138">CommonParameters</span></span>
<span data-ttu-id="788f2-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="788f2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788f2-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="788f2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788f2-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="788f2-141">INPUTS</span></span>

### <span data-ttu-id="788f2-142">Microsoft. Azure. Commands. datamigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="788f2-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="788f2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="788f2-143">System.String</span></span>

## <span data-ttu-id="788f2-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="788f2-144">OUTPUTS</span></span>

### <span data-ttu-id="788f2-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="788f2-145">System.Boolean</span></span>

## <span data-ttu-id="788f2-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="788f2-146">NOTES</span></span>

## <span data-ttu-id="788f2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="788f2-147">RELATED LINKS</span></span>
