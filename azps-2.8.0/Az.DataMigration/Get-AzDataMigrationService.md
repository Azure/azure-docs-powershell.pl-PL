---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: dcb9d6e58a743f37aa71d91b0b73772c239f252e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705751"
---
# <span data-ttu-id="5743e-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5743e-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="5743e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5743e-102">SYNOPSIS</span></span>
<span data-ttu-id="5743e-103">Pobiera właściwości skojarzone z wystąpieniem usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5743e-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="5743e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5743e-104">SYNTAX</span></span>

### <span data-ttu-id="5743e-105">ResourceGroupSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5743e-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5743e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5743e-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5743e-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="5743e-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5743e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5743e-108">DESCRIPTION</span></span>
<span data-ttu-id="5743e-109">Polecenie cmdlet Get-AzDataMigrationService pobiera właściwości skojarzone z wystąpieniem usługi migracji bazy danych platformy Azure na podstawie nazwy usługi i nazwy grupy zasobów platformy Azure jako parametrów wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5743e-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="5743e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5743e-110">EXAMPLES</span></span>

### <span data-ttu-id="5743e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5743e-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="5743e-112">Powyższy przykład pobiera właściwości wystąpienia usługi migracji bazy danych platformy Azure o nazwie testService.</span><span class="sxs-lookup"><span data-stu-id="5743e-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="5743e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5743e-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="5743e-114">Powyższy przykład pobiera usługi migracji bazy danych platformy Azure w grupie zasobów o nazwie testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5743e-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="5743e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5743e-115">PARAMETERS</span></span>

### <span data-ttu-id="5743e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5743e-116">-DefaultProfile</span></span>
<span data-ttu-id="5743e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5743e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5743e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5743e-118">-Name</span></span>
<span data-ttu-id="5743e-119">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5743e-119">Name of Database Migration Service.</span></span>

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

### <span data-ttu-id="5743e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5743e-120">-ResourceGroupName</span></span>
<span data-ttu-id="5743e-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5743e-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="5743e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5743e-122">-ResourceId</span></span>
<span data-ttu-id="5743e-123">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="5743e-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="5743e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5743e-124">CommonParameters</span></span>
<span data-ttu-id="5743e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5743e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5743e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5743e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5743e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5743e-127">INPUTS</span></span>

### <span data-ttu-id="5743e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5743e-128">System.String</span></span>

## <span data-ttu-id="5743e-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5743e-129">OUTPUTS</span></span>

### <span data-ttu-id="5743e-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5743e-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="5743e-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5743e-131">NOTES</span></span>

## <span data-ttu-id="5743e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5743e-132">RELATED LINKS</span></span>