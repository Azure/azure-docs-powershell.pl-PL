---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238160"
---
# <span data-ttu-id="28af8-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="28af8-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="28af8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28af8-102">SYNOPSIS</span></span>
<span data-ttu-id="28af8-103">Pobiera właściwości projektu migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="28af8-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="28af8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="28af8-104">SYNTAX</span></span>

### <span data-ttu-id="28af8-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="28af8-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28af8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28af8-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28af8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28af8-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28af8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="28af8-108">DESCRIPTION</span></span>
<span data-ttu-id="28af8-109">Polecenie Get-AzDataMigrationProject pobiera właściwości projektu migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="28af8-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="28af8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="28af8-110">EXAMPLES</span></span>

### <span data-ttu-id="28af8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28af8-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="28af8-112">Powyższy przykład pobiera projekt migracji bazy danych Azure o nazwie TestProject do grupy zasobów o nazwie testResourceGroup i w ramach usługi o nazwie testService</span><span class="sxs-lookup"><span data-stu-id="28af8-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="28af8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="28af8-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="28af8-114">Powyższy przykład pobiera projekt migracji bazy danych Azure na podstawie przekazywanego parametru wprowadzania obiektu PSProject.</span><span class="sxs-lookup"><span data-stu-id="28af8-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="28af8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28af8-115">PARAMETERS</span></span>

### <span data-ttu-id="28af8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28af8-116">-DefaultProfile</span></span>
<span data-ttu-id="28af8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="28af8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28af8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28af8-118">-InputObject</span></span>
<span data-ttu-id="28af8-119">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="28af8-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="28af8-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="28af8-120">-Name</span></span>
<span data-ttu-id="28af8-121">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="28af8-121">The name of the project.</span></span>

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

### <span data-ttu-id="28af8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28af8-122">-ResourceGroupName</span></span>
<span data-ttu-id="28af8-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="28af8-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="28af8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28af8-124">-ResourceId</span></span>
<span data-ttu-id="28af8-125">Identyfikator zasobu usługi DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="28af8-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="28af8-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="28af8-126">-ServiceName</span></span>
<span data-ttu-id="28af8-127">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="28af8-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="28af8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28af8-128">CommonParameters</span></span>
<span data-ttu-id="28af8-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28af8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28af8-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28af8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28af8-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28af8-131">INPUTS</span></span>

### <span data-ttu-id="28af8-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="28af8-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="28af8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="28af8-133">System.String</span></span>

## <span data-ttu-id="28af8-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28af8-134">OUTPUTS</span></span>

### <span data-ttu-id="28af8-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="28af8-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="28af8-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="28af8-136">NOTES</span></span>

## <span data-ttu-id="28af8-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28af8-137">RELATED LINKS</span></span>
