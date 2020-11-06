---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551764"
---
# <span data-ttu-id="4e9ec-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="4e9ec-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="4e9ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9ec-103">Pobiera właściwości projektu migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9ec-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e9ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e9ec-104">SYNTAX</span></span>

### <span data-ttu-id="4e9ec-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4e9ec-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="4e9ec-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e9ec-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="4e9ec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e9ec-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="4e9ec-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4e9ec-108">DESCRIPTION</span></span>
<span data-ttu-id="4e9ec-109">Polecenie cmdlet Get-AzureRmDataMigrationProject pobiera właściwości projektu migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9ec-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="4e9ec-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e9ec-110">EXAMPLES</span></span>

### <span data-ttu-id="4e9ec-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4e9ec-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="4e9ec-112">Powyższy przykład pobiera projekt migracji bazy danych platformy Azure o nazwie TestProject w grupie zasobów o nazwie testResourceGroup i w obszarze usługa o nazwie testService</span><span class="sxs-lookup"><span data-stu-id="4e9ec-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="4e9ec-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4e9ec-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="4e9ec-114">Powyższy przykład pobiera projekt migracji bazy danych platformy Azure oparty na przekazanym parametrze wejściowym obiektu PSProject.</span><span class="sxs-lookup"><span data-stu-id="4e9ec-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 


## <span data-ttu-id="4e9ec-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e9ec-115">PARAMETERS</span></span>

### <span data-ttu-id="4e9ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e9ec-116">-DefaultProfile</span></span>
<span data-ttu-id="4e9ec-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9ec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e9ec-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4e9ec-118">-InputObject</span></span>
<span data-ttu-id="4e9ec-119">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="4e9ec-119">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9ec-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4e9ec-120">-Name</span></span>
<span data-ttu-id="4e9ec-121">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="4e9ec-121">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9ec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e9ec-122">-ResourceGroupName</span></span>
<span data-ttu-id="4e9ec-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4e9ec-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9ec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e9ec-124">-ResourceId</span></span>
<span data-ttu-id="4e9ec-125">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="4e9ec-125">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9ec-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4e9ec-126">-ServiceName</span></span>
<span data-ttu-id="4e9ec-127">Nazwa usługi migracji danych.</span><span class="sxs-lookup"><span data-stu-id="4e9ec-127">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="4e9ec-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e9ec-128">INPUTS</span></span>

### <span data-ttu-id="4e9ec-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="4e9ec-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="4e9ec-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4e9ec-130">System.String</span></span>


## <span data-ttu-id="4e9ec-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e9ec-131">OUTPUTS</span></span>

### <span data-ttu-id="4e9ec-132">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. datamigration. MODELES. PSProject, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="4e9ec-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProject, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="4e9ec-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e9ec-133">NOTES</span></span>

## <span data-ttu-id="4e9ec-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e9ec-134">RELATED LINKS</span></span>

