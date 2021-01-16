---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: beed4ef06d567250fefa8cef86da133447a9f20c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350434"
---
# <span data-ttu-id="ca2ae-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="ca2ae-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="ca2ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ca2ae-103">Tworzy nowy projekt usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="ca2ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca2ae-104">SYNTAX</span></span>

### <span data-ttu-id="ca2ae-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ca2ae-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca2ae-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca2ae-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca2ae-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca2ae-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca2ae-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ca2ae-108">DESCRIPTION</span></span>
<span data-ttu-id="ca2ae-109">Polecenie cmdlet New-AzDataMigrationProject tworzy nowy projekt usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="ca2ae-110">To polecenie cmdlet zajmuje wszystkie wymagane parametry, takie jak nazwa grupy zasobów platformy Azure, nazwa usługi Azure Data Migration, w której ma zostać utworzony nowy projekt, region, w którym ma zostać utworzony projekt, unikatowa nazwa nowego projektu, obiekt źródło i docelowe oraz obiekt typ docelowy, jako dane wejściowe listy baz danych do zmigrowania.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="ca2ae-111">Za pomocą polecenia cmdlet New-AzDataMigrationConnectionInfo Utwórz nowy obiekt ConnectionInfo dla połączeń źródłowych i docelowych.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="ca2ae-112">Dla wybranych baz danych jest oczekiwana lista Microsoft. Azure. Management. datamigration. models. DatabaseInfo. Ten obiekt można utworzyć przy użyciu New-AzDataMigrationDatabaseInfo polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="ca2ae-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca2ae-113">EXAMPLES</span></span>

### <span data-ttu-id="ca2ae-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca2ae-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="ca2ae-115">W powyższym przykładzie pokazano, jak utworzyć nowy projekt o nazwie MyDMSProject znajdujący się w regionie centralnego Stanów Zjednoczonych w ramach wystąpienia usługi migracji bazy danych platformy Azure o nazwie TestService.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="ca2ae-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca2ae-116">PARAMETERS</span></span>

### <span data-ttu-id="ca2ae-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="ca2ae-117">-DatabaseInfo</span></span>
<span data-ttu-id="ca2ae-118">Informacje o bazie danych.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-118">Database Infos.</span></span>

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

### <span data-ttu-id="ca2ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca2ae-119">-DefaultProfile</span></span>
<span data-ttu-id="ca2ae-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca2ae-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ca2ae-121">-InputObject</span></span>
<span data-ttu-id="ca2ae-122">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="ca2ae-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ca2ae-123">-Location</span></span>
<span data-ttu-id="ca2ae-124">Lokalizacja wystąpienia usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="ca2ae-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca2ae-125">-Name</span></span>
<span data-ttu-id="ca2ae-126">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-126">The name of the project.</span></span>

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

### <span data-ttu-id="ca2ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca2ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="ca2ae-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca2ae-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca2ae-129">-ResourceId</span></span>
<span data-ttu-id="ca2ae-130">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="ca2ae-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ca2ae-131">-ServiceName</span></span>
<span data-ttu-id="ca2ae-132">Nazwa wystąpienia usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="ca2ae-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="ca2ae-133">-SourceConnection</span></span>
<span data-ttu-id="ca2ae-134">Informacje o połączeniu źródłowym.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="ca2ae-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="ca2ae-135">-SourceType</span></span>
<span data-ttu-id="ca2ae-136">Typ platformy źródłowej dla programu Project.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="ca2ae-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="ca2ae-137">-TargetConnection</span></span>
<span data-ttu-id="ca2ae-138">Informacje o połączeniu docelowym.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-138">Target connection information.</span></span>

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

### <span data-ttu-id="ca2ae-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="ca2ae-139">-TargetType</span></span>
<span data-ttu-id="ca2ae-140">Docelowy typ platformy dla programu Project.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="ca2ae-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca2ae-141">-Confirm</span></span>
<span data-ttu-id="ca2ae-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca2ae-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca2ae-143">-WhatIf</span></span>
<span data-ttu-id="ca2ae-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca2ae-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca2ae-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca2ae-146">CommonParameters</span></span>
<span data-ttu-id="ca2ae-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca2ae-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca2ae-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca2ae-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca2ae-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca2ae-149">INPUTS</span></span>

### <span data-ttu-id="ca2ae-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ca2ae-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="ca2ae-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ca2ae-151">System.String</span></span>

## <span data-ttu-id="ca2ae-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca2ae-152">OUTPUTS</span></span>

### <span data-ttu-id="ca2ae-153">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="ca2ae-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="ca2ae-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca2ae-154">NOTES</span></span>

## <span data-ttu-id="ca2ae-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca2ae-155">RELATED LINKS</span></span>
