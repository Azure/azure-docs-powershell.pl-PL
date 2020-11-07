---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718927"
---
# <span data-ttu-id="884bb-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="884bb-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="884bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="884bb-102">SYNOPSIS</span></span>
<span data-ttu-id="884bb-103">Tworzy nowe wystąpienie usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="884bb-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="884bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="884bb-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="884bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="884bb-105">DESCRIPTION</span></span>
<span data-ttu-id="884bb-106">Polecenie cmdlet New-AzureRmDataMigrationService tworzy nowe wystąpienie usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="884bb-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="884bb-107">To polecenie cmdlet przyjmuje nazwę istniejącej grupy zasobów platformy Azure, unikatową nazwę nowego wystąpienia usługi migracji bazy danych platformy Azure, która ma zostać utworzona, region, w którym jest inicjowana instancja, nazwa SKU procesu roboczego DMS oraz nazwa podsieci wirtualnej platformy Azure, w której ma się znajdować usługa.</span><span class="sxs-lookup"><span data-stu-id="884bb-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="884bb-108">Brak parametru dla nazwy subskrypcji, ponieważ oczekuje się, że użytkownik określi domyślną subskrypcję sesji logowania platformy Azure lub wykona Get-AzureRmSubscription-Subscriptionname "Moja subskrypcja" | Select-AzureRmSubscription, aby wybrać inny abonament.</span><span class="sxs-lookup"><span data-stu-id="884bb-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription –SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="884bb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="884bb-109">EXAMPLES</span></span>

### <span data-ttu-id="884bb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="884bb-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="884bb-111">W powyższym przykładzie pokazano, jak utworzyć nowe wystąpienie usługi migracji bazy danych platformy Azure o nazwie TestService w regionie Central Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="884bb-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>


## <span data-ttu-id="884bb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="884bb-112">PARAMETERS</span></span>

### <span data-ttu-id="884bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884bb-113">-DefaultProfile</span></span>
<span data-ttu-id="884bb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="884bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="884bb-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="884bb-115">-Location</span></span>
<span data-ttu-id="884bb-116">Lokalizacja wystąpienia usługi migracji bazy danych platformy Azure do utworzenia, które odpowiada obszarowi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="884bb-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="884bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="884bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="884bb-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="884bb-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="884bb-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="884bb-119">-ServiceName</span></span>
<span data-ttu-id="884bb-120">Nazwa wystąpienia usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="884bb-120">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="884bb-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="884bb-121">-Sku</span></span>
<span data-ttu-id="884bb-122">Jednostka SKU wystąpienia usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="884bb-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="884bb-123">Możliwe wartości są obecnie Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="884bb-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="884bb-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="884bb-124">-VirtualSubnetId</span></span>
<span data-ttu-id="884bb-125">Nazwa podsieci w określonej sieci wirtualnej używanej dla wystąpienia usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="884bb-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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




## <span data-ttu-id="884bb-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="884bb-126">OUTPUTS</span></span>

### <span data-ttu-id="884bb-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="884bb-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>


## <span data-ttu-id="884bb-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="884bb-128">NOTES</span></span>

## <span data-ttu-id="884bb-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="884bb-129">RELATED LINKS</span></span>

