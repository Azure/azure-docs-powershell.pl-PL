---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: c8e81cf727894adfa7378bbed996a1a476521148
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198098"
---
# <span data-ttu-id="ad230-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ad230-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="ad230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad230-102">SYNOPSIS</span></span>
<span data-ttu-id="ad230-103">Tworzy nowe wystąpienie usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="ad230-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="ad230-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad230-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad230-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad230-105">DESCRIPTION</span></span>
<span data-ttu-id="ad230-106">Polecenie New-AzDataMigrationService tworzy nowe wystąpienie usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="ad230-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="ad230-107">To polecenie cmdlet przyjmuje nazwę istniejącej grupy zasobów platformy Azure, unikatową nazwę nowego wystąpienia usługi migracji bazy danych Azure, region, w którym jest aprowowana obsługa wystąpień, nazwę sKU DMS Worker oraz nazwę wirtualnej podsieci platformy Azure, w której ma się znajdować usługa.</span><span class="sxs-lookup"><span data-stu-id="ad230-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="ad230-108">Nie ma parametru dla nazwy subskrypcji, ponieważ użytkownik powinien określić domyślną subskrypcję sesji logowania platformy Azure lub wykonać polecenie Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription, aby wybrać inną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="ad230-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="ad230-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad230-109">EXAMPLES</span></span>

### <span data-ttu-id="ad230-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad230-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="ad230-111">W powyższym przykładzie pokazano, jak utworzyć nowe wystąpienie usługi migracji bazy danych Azure o nazwie TestService w regionie Środkowych Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="ad230-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="ad230-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad230-112">PARAMETERS</span></span>

### <span data-ttu-id="ad230-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad230-113">-DefaultProfile</span></span>
<span data-ttu-id="ad230-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad230-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad230-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ad230-115">-Location</span></span>
<span data-ttu-id="ad230-116">Lokalizacja wystąpienia usługi migracji bazy danych Azure, które ma zostać utworzone, które odpowiada regionowi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ad230-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="ad230-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad230-117">-Name</span></span>
<span data-ttu-id="ad230-118">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ad230-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="ad230-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad230-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad230-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad230-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad230-121">- SKU</span><span class="sxs-lookup"><span data-stu-id="ad230-121">-Sku</span></span>
<span data-ttu-id="ad230-122">SKU wystąpienia usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="ad230-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="ad230-123">Obecnie możliwe wartości to Basic_1vCore;Basic_2vCores;GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="ad230-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="ad230-124">- VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="ad230-124">-VirtualSubnetId</span></span>
<span data-ttu-id="ad230-125">Nazwa podsieci w określonej sieci wirtualnej do użycia w wystąpieniu usługi migracji bazy danych Azure.</span><span class="sxs-lookup"><span data-stu-id="ad230-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="ad230-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad230-126">-Confirm</span></span>
<span data-ttu-id="ad230-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ad230-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad230-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad230-128">-WhatIf</span></span>
<span data-ttu-id="ad230-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad230-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad230-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ad230-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad230-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad230-131">CommonParameters</span></span>
<span data-ttu-id="ad230-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad230-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad230-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad230-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad230-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad230-134">INPUTS</span></span>

### <span data-ttu-id="ad230-135">Brak</span><span class="sxs-lookup"><span data-stu-id="ad230-135">None</span></span>

## <span data-ttu-id="ad230-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad230-136">OUTPUTS</span></span>

### <span data-ttu-id="ad230-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ad230-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="ad230-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad230-138">NOTES</span></span>

## <span data-ttu-id="ad230-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad230-139">RELATED LINKS</span></span>
