---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: 06899e35e9119025aa13a310a3d6200c30b223df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548703"
---
# <span data-ttu-id="9fc1a-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9fc1a-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="9fc1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fc1a-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc1a-103">Pobiera właściwości skojarzone z wystąpieniem usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc1a-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fc1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fc1a-104">SYNTAX</span></span>

### <span data-ttu-id="9fc1a-105">ResourceGroupSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9fc1a-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fc1a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fc1a-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fc1a-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="9fc1a-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fc1a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9fc1a-108">DESCRIPTION</span></span>
<span data-ttu-id="9fc1a-109">Polecenie cmdlet Get-AzureRmDataMigrationService pobiera właściwości skojarzone z wystąpieniem usługi migracji bazy danych platformy Azure na podstawie nazwy usługi i nazwy grupy zasobów platformy Azure jako parametrów wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9fc1a-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="9fc1a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fc1a-110">EXAMPLES</span></span>

### <span data-ttu-id="9fc1a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9fc1a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="9fc1a-112">Powyższy przykład pobiera właściwości wystąpienia usługi migracji bazy danych platformy Azure o nazwie testService.</span><span class="sxs-lookup"><span data-stu-id="9fc1a-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="9fc1a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9fc1a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="9fc1a-114">Powyższy przykład pobiera usługi migracji bazy danych platformy Azure w grupie zasobów o nazwie testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9fc1a-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="9fc1a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fc1a-115">PARAMETERS</span></span>

### <span data-ttu-id="9fc1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc1a-116">-DefaultProfile</span></span>
<span data-ttu-id="9fc1a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc1a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc1a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fc1a-118">-Name</span></span>
<span data-ttu-id="9fc1a-119">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9fc1a-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc1a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc1a-120">-ResourceGroupName</span></span>
<span data-ttu-id="9fc1a-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fc1a-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc1a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fc1a-122">-ResourceId</span></span>
<span data-ttu-id="9fc1a-123">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="9fc1a-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="9fc1a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc1a-124">CommonParameters</span></span>
<span data-ttu-id="9fc1a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc1a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc1a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fc1a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc1a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fc1a-127">INPUTS</span></span>

### <span data-ttu-id="9fc1a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9fc1a-128">System.String</span></span>

## <span data-ttu-id="9fc1a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fc1a-129">OUTPUTS</span></span>

### <span data-ttu-id="9fc1a-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9fc1a-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="9fc1a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fc1a-131">NOTES</span></span>

## <span data-ttu-id="9fc1a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fc1a-132">RELATED LINKS</span></span>
