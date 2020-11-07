---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: f45134cae9c77108aca4084470fd7f919fde02a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894462"
---
# <span data-ttu-id="b71e1-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="b71e1-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="b71e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b71e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b71e1-103">Usuwa projekt usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b71e1-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="b71e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b71e1-104">SYNTAX</span></span>

### <span data-ttu-id="b71e1-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b71e1-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b71e1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71e1-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71e1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71e1-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b71e1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b71e1-108">DESCRIPTION</span></span>
<span data-ttu-id="b71e1-109">Polecenie cmdlet Remove-AzDataMigrationProject usuwa projekt usługi migracji bazy danych platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b71e1-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="b71e1-110">Podanie parametru DeleteRunningTask powoduje usunięcie wszystkich zadań usługi migracji bazy danych platformy Azure skojarzonych z tym projektem, który jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="b71e1-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="b71e1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b71e1-111">EXAMPLES</span></span>

### <span data-ttu-id="b71e1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b71e1-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="b71e1-113">W powyższym przykładzie usunięto projekt usługi migracji bazy danych platformy Azure o nazwie myDMProject z usługi Azure na podstawie nazwy jako parametru wejściowego</span><span class="sxs-lookup"><span data-stu-id="b71e1-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="b71e1-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b71e1-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="b71e1-115">W powyższym przykładzie usunięto projekt usługi migracji bazy danych platformy Azure oparty na obiekcie PSProject jako parametr wejściowy.</span><span class="sxs-lookup"><span data-stu-id="b71e1-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="b71e1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b71e1-116">PARAMETERS</span></span>

### <span data-ttu-id="b71e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71e1-117">-DefaultProfile</span></span>
<span data-ttu-id="b71e1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b71e1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b71e1-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="b71e1-119">-DeleteRunningTask</span></span>
<span data-ttu-id="b71e1-120">Usuwanie uruchomionego zadania</span><span class="sxs-lookup"><span data-stu-id="b71e1-120">Delete any running task</span></span>

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

### <span data-ttu-id="b71e1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b71e1-121">-Force</span></span>
<span data-ttu-id="b71e1-122">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="b71e1-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b71e1-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b71e1-123">-InputObject</span></span>
<span data-ttu-id="b71e1-124">Obiekt PSProject.</span><span class="sxs-lookup"><span data-stu-id="b71e1-124">PSProject Object.</span></span>

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

### <span data-ttu-id="b71e1-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b71e1-125">-Name</span></span>
<span data-ttu-id="b71e1-126">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="b71e1-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b71e1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b71e1-127">-PassThru</span></span>
<span data-ttu-id="b71e1-128">Zwraca wartość PRAWDA lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="b71e1-128">Returns an true/false.</span></span>
<span data-ttu-id="b71e1-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b71e1-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b71e1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b71e1-130">-ResourceGroupName</span></span>
<span data-ttu-id="b71e1-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b71e1-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="b71e1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b71e1-132">-ResourceId</span></span>
<span data-ttu-id="b71e1-133">Identyfikator zasobu projektu.</span><span class="sxs-lookup"><span data-stu-id="b71e1-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="b71e1-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b71e1-134">-ServiceName</span></span>
<span data-ttu-id="b71e1-135">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b71e1-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="b71e1-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b71e1-136">-Confirm</span></span>
<span data-ttu-id="b71e1-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b71e1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b71e1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b71e1-138">-WhatIf</span></span>
<span data-ttu-id="b71e1-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b71e1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b71e1-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b71e1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b71e1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71e1-141">CommonParameters</span></span>
<span data-ttu-id="b71e1-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b71e1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71e1-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b71e1-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71e1-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b71e1-144">INPUTS</span></span>

### <span data-ttu-id="b71e1-145">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="b71e1-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="b71e1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b71e1-146">System.String</span></span>

## <span data-ttu-id="b71e1-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b71e1-147">OUTPUTS</span></span>

### <span data-ttu-id="b71e1-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b71e1-148">System.Boolean</span></span>

## <span data-ttu-id="b71e1-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b71e1-149">NOTES</span></span>

## <span data-ttu-id="b71e1-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b71e1-150">RELATED LINKS</span></span>
