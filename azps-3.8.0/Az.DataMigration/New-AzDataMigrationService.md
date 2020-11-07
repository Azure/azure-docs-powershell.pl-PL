---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: c8e81cf727894adfa7378bbed996a1a476521148
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894474"
---
# <span data-ttu-id="176d5-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="176d5-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="176d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="176d5-102">SYNOPSIS</span></span>
<span data-ttu-id="176d5-103">Tworzy nowe wystąpienie usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="176d5-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="176d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="176d5-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176d5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="176d5-105">DESCRIPTION</span></span>
<span data-ttu-id="176d5-106">Polecenie cmdlet New-AzDataMigrationService tworzy nowe wystąpienie usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="176d5-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="176d5-107">To polecenie cmdlet przyjmuje nazwę istniejącej grupy zasobów platformy Azure, unikatową nazwę nowego wystąpienia usługi migracji bazy danych platformy Azure, która ma zostać utworzona, region, w którym jest inicjowana instancja, nazwa SKU procesu roboczego DMS oraz nazwa podsieci wirtualnej platformy Azure, w której ma się znajdować usługa.</span><span class="sxs-lookup"><span data-stu-id="176d5-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="176d5-108">Brak parametru nazwy subskrypcji, ponieważ oczekuje się, że użytkownik określi domyślną subskrypcję sesji logowania platformy Azure lub wykona Get-AzSubscription-Subscriptionname "Moja subskrypcja" | Select-AzSubscription, aby wybrać inny abonament.</span><span class="sxs-lookup"><span data-stu-id="176d5-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="176d5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="176d5-109">EXAMPLES</span></span>

### <span data-ttu-id="176d5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="176d5-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="176d5-111">W powyższym przykładzie pokazano, jak utworzyć nowe wystąpienie usługi migracji bazy danych platformy Azure o nazwie TestService w regionie Central Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="176d5-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="176d5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="176d5-112">PARAMETERS</span></span>

### <span data-ttu-id="176d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176d5-113">-DefaultProfile</span></span>
<span data-ttu-id="176d5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="176d5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="176d5-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="176d5-115">-Location</span></span>
<span data-ttu-id="176d5-116">Lokalizacja wystąpienia usługi migracji bazy danych platformy Azure do utworzenia, które odpowiada obszarowi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="176d5-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176d5-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="176d5-117">-Name</span></span>
<span data-ttu-id="176d5-118">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="176d5-118">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="176d5-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="176d5-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176d5-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="176d5-121">-Sku</span></span>
<span data-ttu-id="176d5-122">Jednostka SKU wystąpienia usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="176d5-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="176d5-123">Możliwe wartości są obecnie Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="176d5-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176d5-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="176d5-124">-VirtualSubnetId</span></span>
<span data-ttu-id="176d5-125">Nazwa podsieci w określonej sieci wirtualnej używanej dla wystąpienia usługi migracji bazy danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="176d5-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176d5-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="176d5-126">-Confirm</span></span>
<span data-ttu-id="176d5-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176d5-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176d5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176d5-128">-WhatIf</span></span>
<span data-ttu-id="176d5-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176d5-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="176d5-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="176d5-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176d5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176d5-131">CommonParameters</span></span>
<span data-ttu-id="176d5-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176d5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176d5-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="176d5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176d5-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="176d5-134">INPUTS</span></span>

### <span data-ttu-id="176d5-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="176d5-135">None</span></span>

## <span data-ttu-id="176d5-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="176d5-136">OUTPUTS</span></span>

### <span data-ttu-id="176d5-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="176d5-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="176d5-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="176d5-138">NOTES</span></span>

## <span data-ttu-id="176d5-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="176d5-139">RELATED LINKS</span></span>
