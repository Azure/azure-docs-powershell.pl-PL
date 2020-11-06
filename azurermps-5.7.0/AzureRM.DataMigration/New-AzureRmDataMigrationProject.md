---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 99884c23ff99287deb721e3cb76871766cdfa7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552927"
---
# <span data-ttu-id="16842-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="16842-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="16842-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16842-102">SYNOPSIS</span></span>
<span data-ttu-id="16842-103">Tworzy nowy projekt usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="16842-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16842-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16842-104">SYNTAX</span></span>

### <span data-ttu-id="16842-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="16842-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform>
 [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="16842-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16842-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="16842-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16842-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="16842-108">Opis</span><span class="sxs-lookup"><span data-stu-id="16842-108">DESCRIPTION</span></span>
<span data-ttu-id="16842-109">Polecenie cmdlet New-AzureRmDataMigrationProject tworzy nowy projekt usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="16842-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="16842-110">To polecenie cmdlet zajmuje wszystkie wymagane parametry, takie jak nazwa grupy zasobów platformy Azure, nazwa usługi Azure Data Migration, w której ma zostać utworzony nowy projekt, region, w którym ma zostać utworzony projekt, unikatowa nazwa nowego projektu, obiekt źródło i docelowe oraz obiekt typ docelowy, jako dane wejściowe listy baz danych do zmigrowania.</span><span class="sxs-lookup"><span data-stu-id="16842-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="16842-111">Za pomocą polecenia cmdlet New-AzureRmDataMigrationConnectionInfo Utwórz nowy obiekt ConnectionInfo dla połączeń źródłowych i docelowych.</span><span class="sxs-lookup"><span data-stu-id="16842-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="16842-112">Dla wybranych baz danych jest oczekiwana lista Microsoft. Azure. Management. datamigration. models. DatabaseInfo. Ten obiekt można utworzyć przy użyciu New-AzureRmDataMigrationDatabaseInfo polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16842-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="16842-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16842-113">EXAMPLES</span></span>

### <span data-ttu-id="16842-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="16842-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="16842-115">W powyższym przykładzie pokazano, jak utworzyć nowy projekt o nazwie MyDMSProject znajdujący się w regionie centralnego Stanów Zjednoczonych w ramach wystąpienia usługi migracji bazy danych platformy Azure o nazwie TestService.</span><span class="sxs-lookup"><span data-stu-id="16842-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>



## <span data-ttu-id="16842-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16842-116">PARAMETERS</span></span>

### <span data-ttu-id="16842-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16842-117">-Confirm</span></span>
<span data-ttu-id="16842-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16842-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16842-119">-DatabaseInfo[]</span><span class="sxs-lookup"><span data-stu-id="16842-119">-DatabaseInfo[]</span></span>
<span data-ttu-id="16842-120">Informacje o bazie danych</span><span class="sxs-lookup"><span data-stu-id="16842-120">Database information</span></span>

```yaml
Type: DatabaseInfo[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16842-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16842-121">-DefaultProfile</span></span>
<span data-ttu-id="16842-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16842-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16842-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="16842-123">-Location</span></span>
<span data-ttu-id="16842-124">Lokalizacja wystąpienia usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="16842-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16842-125">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="16842-125">-ProjectName</span></span>
<span data-ttu-id="16842-126">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="16842-126">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16842-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16842-127">-ResourceGroupName</span></span>
<span data-ttu-id="16842-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="16842-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16842-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="16842-129">-ServiceName</span></span>
<span data-ttu-id="16842-130">Nazwa wystąpienia usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="16842-130">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16842-131">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="16842-131">-SourceConnection</span></span>
<span data-ttu-id="16842-132">Informacje o połączeniu źródłowym.</span><span class="sxs-lookup"><span data-stu-id="16842-132">Source Connection Info.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16842-133">-SourceType</span><span class="sxs-lookup"><span data-stu-id="16842-133">-SourceType</span></span>
<span data-ttu-id="16842-134">Typ platformy źródłowej dla programu Project.</span><span class="sxs-lookup"><span data-stu-id="16842-134">Source platform type for project.</span></span>

```yaml
Type: ProjectSourcePlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16842-135">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="16842-135">-TargetConnection</span></span>
<span data-ttu-id="16842-136">Informacje o połączeniu docelowym.</span><span class="sxs-lookup"><span data-stu-id="16842-136">Target connection information.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16842-137">-TargetType</span><span class="sxs-lookup"><span data-stu-id="16842-137">-TargetType</span></span>
<span data-ttu-id="16842-138">Docelowy typ platformy dla programu Project.</span><span class="sxs-lookup"><span data-stu-id="16842-138">Target platform type for project.</span></span>

```yaml
Type: ProjectTargetPlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="16842-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16842-139">OUTPUTS</span></span>

### <span data-ttu-id="16842-140">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="16842-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>


## <span data-ttu-id="16842-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16842-141">NOTES</span></span>

## <span data-ttu-id="16842-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16842-142">RELATED LINKS</span></span>

