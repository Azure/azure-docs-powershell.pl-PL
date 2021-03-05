---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: 158ae87c636f0ecf8b8c78d2a6d380640ff49677
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972033"
---
# <span data-ttu-id="a711c-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="a711c-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="a711c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a711c-102">SYNOPSIS</span></span>
<span data-ttu-id="a711c-103">Tworzy nowy projekt usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="a711c-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="a711c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a711c-104">SYNTAX</span></span>

### <span data-ttu-id="a711c-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a711c-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a711c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a711c-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a711c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a711c-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a711c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a711c-108">DESCRIPTION</span></span>
<span data-ttu-id="a711c-109">Polecenie New-AzDataMigrationProject cmdlet tworzy nowy projekt usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="a711c-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="a711c-110">To polecenie cmdlet zawiera wszystkie niezbędne parametry, takie jak nazwa grupy zasobów Azure, nazwa usługi Azure Data Migration Service, w której ma zostać utworzony nowy projekt, region, w którym ma zostać utworzony projekt, unikatowa nazwa nowego projektu, obiekty połączenia źródłowego i docelowego oraz obiekt typu docelowego, jako dane wejściowe listy baz danych do zmigrowania.</span><span class="sxs-lookup"><span data-stu-id="a711c-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="a711c-111">Użyj New-AzDataMigrationConnectionInfo cmdlet, aby utworzyć nowy obiekt ConnectionInfo zarówno dla połączeń źródłowych, jak i docelowych.</span><span class="sxs-lookup"><span data-stu-id="a711c-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="a711c-112">Lista plików Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo jest oczekiwana dla wybranych baz danych. Ten obiekt można utworzyć za pomocą New-AzDataMigrationDatabaseInfo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a711c-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="a711c-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a711c-113">EXAMPLES</span></span>

### <span data-ttu-id="a711c-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a711c-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="a711c-115">W powyższym przykładzie pokazano, jak utworzyć nowy projekt o nazwie MyDMSProject znajdujący się w regionie Środkowych Stanów Zjednoczonych w ramach wystąpienia usługi migracji bazy danych Azure o nazwie TestService.</span><span class="sxs-lookup"><span data-stu-id="a711c-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="a711c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a711c-116">PARAMETERS</span></span>

### <span data-ttu-id="a711c-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="a711c-117">-DatabaseInfo</span></span>
<span data-ttu-id="a711c-118">Informacje o bazie danych.</span><span class="sxs-lookup"><span data-stu-id="a711c-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a711c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a711c-119">-DefaultProfile</span></span>
<span data-ttu-id="a711c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a711c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a711c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a711c-121">-InputObject</span></span>
<span data-ttu-id="a711c-122">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="a711c-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a711c-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a711c-123">-Location</span></span>
<span data-ttu-id="a711c-124">Lokalizacja wystąpienia usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="a711c-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a711c-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a711c-125">-Name</span></span>
<span data-ttu-id="a711c-126">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="a711c-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a711c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a711c-127">-ResourceGroupName</span></span>
<span data-ttu-id="a711c-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a711c-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a711c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a711c-129">-ResourceId</span></span>
<span data-ttu-id="a711c-130">Identyfikator zasobu usługi DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="a711c-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="a711c-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a711c-131">-ServiceName</span></span>
<span data-ttu-id="a711c-132">Nazwa wystąpienia usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="a711c-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="a711c-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="a711c-133">-SourceConnection</span></span>
<span data-ttu-id="a711c-134">Informacje o połączeniu źródłowym.</span><span class="sxs-lookup"><span data-stu-id="a711c-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a711c-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="a711c-135">-SourceType</span></span>
<span data-ttu-id="a711c-136">Typ platformy źródłowej dla projektu.</span><span class="sxs-lookup"><span data-stu-id="a711c-136">Source platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a711c-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="a711c-137">-TargetConnection</span></span>
<span data-ttu-id="a711c-138">Informacje o połączeniu docelowym.</span><span class="sxs-lookup"><span data-stu-id="a711c-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a711c-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="a711c-139">-TargetType</span></span>
<span data-ttu-id="a711c-140">Typ platformy docelowej dla projektu.</span><span class="sxs-lookup"><span data-stu-id="a711c-140">Target platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a711c-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a711c-141">-Confirm</span></span>
<span data-ttu-id="a711c-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a711c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a711c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a711c-143">-WhatIf</span></span>
<span data-ttu-id="a711c-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a711c-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a711c-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a711c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a711c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a711c-146">CommonParameters</span></span>
<span data-ttu-id="a711c-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a711c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a711c-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a711c-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a711c-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a711c-149">INPUTS</span></span>

### <span data-ttu-id="a711c-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a711c-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="a711c-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a711c-151">System.String</span></span>

## <span data-ttu-id="a711c-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a711c-152">OUTPUTS</span></span>

### <span data-ttu-id="a711c-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="a711c-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="a711c-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a711c-154">NOTES</span></span>

## <span data-ttu-id="a711c-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a711c-155">RELATED LINKS</span></span>
