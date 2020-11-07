---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 00a0e0a688f49615cadff3990071cd49d1356443
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710007"
---
# <span data-ttu-id="43bc1-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="43bc1-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="43bc1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="43bc1-103">Pobiera właściwości projektu migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43bc1-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="43bc1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43bc1-104">SYNTAX</span></span>

### <span data-ttu-id="43bc1-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="43bc1-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43bc1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43bc1-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43bc1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43bc1-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43bc1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="43bc1-108">DESCRIPTION</span></span>
<span data-ttu-id="43bc1-109">Polecenie cmdlet Get-AzDataMigrationProject pobiera właściwości projektu migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43bc1-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="43bc1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43bc1-110">EXAMPLES</span></span>

### <span data-ttu-id="43bc1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="43bc1-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="43bc1-112">Powyższy przykład pobiera projekt migracji bazy danych platformy Azure o nazwie TestProject w grupie zasobów o nazwie testResourceGroup i w obszarze usługa o nazwie testService</span><span class="sxs-lookup"><span data-stu-id="43bc1-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="43bc1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="43bc1-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="43bc1-114">Powyższy przykład pobiera projekt migracji bazy danych platformy Azure oparty na przekazanym parametrze wejściowym obiektu PSProject.</span><span class="sxs-lookup"><span data-stu-id="43bc1-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="43bc1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43bc1-115">PARAMETERS</span></span>

### <span data-ttu-id="43bc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43bc1-116">-DefaultProfile</span></span>
<span data-ttu-id="43bc1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43bc1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43bc1-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43bc1-118">-InputObject</span></span>
<span data-ttu-id="43bc1-119">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="43bc1-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="43bc1-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43bc1-120">-Name</span></span>
<span data-ttu-id="43bc1-121">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="43bc1-121">The name of the project.</span></span>

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

### <span data-ttu-id="43bc1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43bc1-122">-ResourceGroupName</span></span>
<span data-ttu-id="43bc1-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="43bc1-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="43bc1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43bc1-124">-ResourceId</span></span>
<span data-ttu-id="43bc1-125">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="43bc1-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="43bc1-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="43bc1-126">-ServiceName</span></span>
<span data-ttu-id="43bc1-127">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="43bc1-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="43bc1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43bc1-128">CommonParameters</span></span>
<span data-ttu-id="43bc1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43bc1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43bc1-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43bc1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43bc1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43bc1-131">INPUTS</span></span>

### <span data-ttu-id="43bc1-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="43bc1-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="43bc1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="43bc1-133">System.String</span></span>

## <span data-ttu-id="43bc1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43bc1-134">OUTPUTS</span></span>

### <span data-ttu-id="43bc1-135">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="43bc1-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="43bc1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43bc1-136">NOTES</span></span>

## <span data-ttu-id="43bc1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43bc1-137">RELATED LINKS</span></span>
