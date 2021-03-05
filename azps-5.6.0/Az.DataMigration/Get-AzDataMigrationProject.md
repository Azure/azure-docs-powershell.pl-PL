---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 5485693da87dbbb49b5e06e221e818de9bd222d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995569"
---
# <span data-ttu-id="8b744-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="8b744-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="8b744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b744-102">SYNOPSIS</span></span>
<span data-ttu-id="8b744-103">Pobiera właściwości projektu migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="8b744-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="8b744-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b744-104">SYNTAX</span></span>

### <span data-ttu-id="8b744-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8b744-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b744-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b744-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b744-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b744-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b744-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b744-108">DESCRIPTION</span></span>
<span data-ttu-id="8b744-109">Polecenie Get-AzDataMigrationProject pobiera właściwości projektu migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="8b744-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="8b744-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b744-110">EXAMPLES</span></span>

### <span data-ttu-id="8b744-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b744-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="8b744-112">Powyższy przykład pobiera projekt migracji bazy danych Azure o nazwie TestProject do grupy zasobów o nazwie testResourceGroup i w ramach usługi o nazwie testService</span><span class="sxs-lookup"><span data-stu-id="8b744-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="8b744-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8b744-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="8b744-114">Powyższy przykład pobiera projekt migracji bazy danych Azure na podstawie przekazywanego parametru wprowadzania obiektu PSProject.</span><span class="sxs-lookup"><span data-stu-id="8b744-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="8b744-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b744-115">PARAMETERS</span></span>

### <span data-ttu-id="8b744-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b744-116">-DefaultProfile</span></span>
<span data-ttu-id="8b744-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b744-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b744-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b744-118">-InputObject</span></span>
<span data-ttu-id="8b744-119">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="8b744-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="8b744-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8b744-120">-Name</span></span>
<span data-ttu-id="8b744-121">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="8b744-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b744-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b744-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b744-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8b744-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="8b744-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b744-124">-ResourceId</span></span>
<span data-ttu-id="8b744-125">Identyfikator zasobu usługi DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="8b744-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="8b744-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8b744-126">-ServiceName</span></span>
<span data-ttu-id="8b744-127">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8b744-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="8b744-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b744-128">CommonParameters</span></span>
<span data-ttu-id="8b744-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b744-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b744-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b744-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b744-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b744-131">INPUTS</span></span>

### <span data-ttu-id="8b744-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8b744-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="8b744-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8b744-133">System.String</span></span>

## <span data-ttu-id="8b744-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b744-134">OUTPUTS</span></span>

### <span data-ttu-id="8b744-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="8b744-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="8b744-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b744-136">NOTES</span></span>

## <span data-ttu-id="8b744-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b744-137">RELATED LINKS</span></span>
