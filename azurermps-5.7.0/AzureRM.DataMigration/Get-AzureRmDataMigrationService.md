---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548119"
---
# <span data-ttu-id="abf01-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="abf01-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="abf01-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="abf01-102">SYNOPSIS</span></span>
<span data-ttu-id="abf01-103">Pobiera właściwości skojarzone z wystąpieniem usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="abf01-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abf01-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="abf01-104">SYNTAX</span></span>

### <span data-ttu-id="abf01-105">ResourceGroupSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="abf01-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="abf01-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abf01-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="abf01-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="abf01-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## <span data-ttu-id="abf01-108">Opis</span><span class="sxs-lookup"><span data-stu-id="abf01-108">DESCRIPTION</span></span>
<span data-ttu-id="abf01-109">Polecenie cmdlet Get-AzureRmDataMigrationService pobiera właściwości skojarzone z wystąpieniem usługi migracji bazy danych platformy Azure na podstawie nazwy usługi i nazwy grupy zasobów platformy Azure jako parametrów wejściowych.</span><span class="sxs-lookup"><span data-stu-id="abf01-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="abf01-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="abf01-110">EXAMPLES</span></span>

### <span data-ttu-id="abf01-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="abf01-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="abf01-112">Powyższy przykład pobiera właściwości wystąpienia usługi migracji bazy danych platformy Azure o nazwie testService.</span><span class="sxs-lookup"><span data-stu-id="abf01-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="abf01-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="abf01-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

<span data-ttu-id="abf01-114">Powyższy przykład pobiera usługi migracji bazy danych platformy Azure w grupie zasobów o nazwie testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="abf01-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="abf01-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abf01-115">PARAMETERS</span></span>

### <span data-ttu-id="abf01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf01-116">-DefaultProfile</span></span>
<span data-ttu-id="abf01-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="abf01-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf01-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="abf01-118">-Name</span></span>
<span data-ttu-id="abf01-119">Nazwa usługi migracji danych.</span><span class="sxs-lookup"><span data-stu-id="abf01-119">Name of Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf01-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf01-120">-ResourceGroupName</span></span>
<span data-ttu-id="abf01-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="abf01-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf01-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abf01-122">-ResourceId</span></span>
<span data-ttu-id="abf01-123">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="abf01-123">DataMigrationService Resource Id.</span></span>

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

## <span data-ttu-id="abf01-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abf01-124">INPUTS</span></span>

### <span data-ttu-id="abf01-125">System. String</span><span class="sxs-lookup"><span data-stu-id="abf01-125">System.String</span></span>


## <span data-ttu-id="abf01-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="abf01-126">OUTPUTS</span></span>

### <span data-ttu-id="abf01-127">System. Collections. Generic. IList ' 1 [[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft. Azure. Commands. polecenie. datamigration, wersja = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="abf01-127">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="abf01-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="abf01-128">NOTES</span></span>

## <span data-ttu-id="abf01-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abf01-129">RELATED LINKS</span></span>





