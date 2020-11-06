---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: 31d37f740500247fed433c3e40b9d8220a5af663
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548704"
---
# <span data-ttu-id="f826e-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="f826e-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="f826e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f826e-102">SYNOPSIS</span></span>
<span data-ttu-id="f826e-103">Pobiera właściwości projektu migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f826e-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f826e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f826e-104">SYNTAX</span></span>

### <span data-ttu-id="f826e-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f826e-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f826e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f826e-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f826e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f826e-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f826e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f826e-108">DESCRIPTION</span></span>
<span data-ttu-id="f826e-109">Polecenie cmdlet Get-AzureRmDataMigrationProject pobiera właściwości projektu migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f826e-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="f826e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f826e-110">EXAMPLES</span></span>

### <span data-ttu-id="f826e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f826e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="f826e-112">Powyższy przykład pobiera projekt migracji bazy danych platformy Azure o nazwie TestProject w grupie zasobów o nazwie testResourceGroup i w obszarze usługa o nazwie testService</span><span class="sxs-lookup"><span data-stu-id="f826e-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="f826e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f826e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="f826e-114">Powyższy przykład pobiera projekt migracji bazy danych platformy Azure oparty na przekazanym parametrze wejściowym obiektu PSProject.</span><span class="sxs-lookup"><span data-stu-id="f826e-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="f826e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f826e-115">PARAMETERS</span></span>

### <span data-ttu-id="f826e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f826e-116">-DefaultProfile</span></span>
<span data-ttu-id="f826e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f826e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f826e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f826e-118">-InputObject</span></span>
<span data-ttu-id="f826e-119">Obiekt PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="f826e-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="f826e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f826e-120">-Name</span></span>
<span data-ttu-id="f826e-121">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="f826e-121">The name of the project.</span></span>

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

### <span data-ttu-id="f826e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f826e-122">-ResourceGroupName</span></span>
<span data-ttu-id="f826e-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f826e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f826e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f826e-124">-ResourceId</span></span>
<span data-ttu-id="f826e-125">Identyfikator zasobu DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="f826e-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="f826e-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f826e-126">-ServiceName</span></span>
<span data-ttu-id="f826e-127">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f826e-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="f826e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f826e-128">CommonParameters</span></span>
<span data-ttu-id="f826e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f826e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f826e-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f826e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f826e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f826e-131">INPUTS</span></span>

### <span data-ttu-id="f826e-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f826e-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="f826e-133">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f826e-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f826e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f826e-134">System.String</span></span>

## <span data-ttu-id="f826e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f826e-135">OUTPUTS</span></span>

### <span data-ttu-id="f826e-136">Microsoft. Azure. Commands. datamigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="f826e-136">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="f826e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f826e-137">NOTES</span></span>

## <span data-ttu-id="f826e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f826e-138">RELATED LINKS</span></span>
