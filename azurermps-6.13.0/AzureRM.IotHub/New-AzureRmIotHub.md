---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
ms.openlocfilehash: a24f06c07552f60aa5e18ab6af0c7d25b78b567d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546599"
---
# <span data-ttu-id="87c73-101">New-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="87c73-101">New-AzureRmIotHub</span></span>

## <span data-ttu-id="87c73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87c73-102">SYNOPSIS</span></span>
<span data-ttu-id="87c73-103">Tworzy nowy IotHub.</span><span class="sxs-lookup"><span data-stu-id="87c73-103">Creates a new IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87c73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87c73-104">SYNTAX</span></span>

```
New-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87c73-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87c73-105">DESCRIPTION</span></span>
<span data-ttu-id="87c73-106">Tworzy nowy IotHub.</span><span class="sxs-lookup"><span data-stu-id="87c73-106">Creates a new IotHub.</span></span>
<span data-ttu-id="87c73-107">IotHub można utworzyć przy użyciu właściwości domyślnych lub określić proerties wejściowy.</span><span class="sxs-lookup"><span data-stu-id="87c73-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="87c73-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87c73-108">EXAMPLES</span></span>

### <span data-ttu-id="87c73-109">Przykład 1 Tworzenie nowego IotHub z właściwościami domyślnymi</span><span class="sxs-lookup"><span data-stu-id="87c73-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="87c73-110">Tworzy nowy IotHub o nazwie "myiothub" w wersji SKU "S1", wydajności 1 i lokalizacji "northeurope".</span><span class="sxs-lookup"><span data-stu-id="87c73-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="87c73-111">Przykład 2 Utwórz nowy IotHub z MaxDeliveryCount kolejki CloudtoDevice o wartości 20</span><span class="sxs-lookup"><span data-stu-id="87c73-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="87c73-112">Tworzy nowy IotHub o nazwie "myiothub" w wersji SKU "S1", wydajności 1 i lokalizacji "northeurope" z zaawansowanymi właściwościami wejściowymi przedstawionymi przez $properties.</span><span class="sxs-lookup"><span data-stu-id="87c73-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="87c73-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. MODELES. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzureRmIotHub-ResourceGroupName "Moja resourceName"-name-myiothub</span><span class="sxs-lookup"><span data-stu-id="87c73-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="87c73-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87c73-114">PARAMETERS</span></span>

### <span data-ttu-id="87c73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c73-115">-DefaultProfile</span></span>
<span data-ttu-id="87c73-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="87c73-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87c73-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="87c73-117">-Location</span></span>
<span data-ttu-id="87c73-118">Lokalizacja, w której należy utworzyć Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="87c73-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="87c73-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87c73-119">-Name</span></span>
<span data-ttu-id="87c73-120">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="87c73-120">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c73-121">-Properties</span><span class="sxs-lookup"><span data-stu-id="87c73-121">-Properties</span></span>
<span data-ttu-id="87c73-122">Właściwości Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="87c73-122">Properties of the IoT hub.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c73-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c73-123">-ResourceGroupName</span></span>
<span data-ttu-id="87c73-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="87c73-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c73-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="87c73-125">-SkuName</span></span>
<span data-ttu-id="87c73-126">Nazwa jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="87c73-126">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c73-127">-Jednostki</span><span class="sxs-lookup"><span data-stu-id="87c73-127">-Units</span></span>
<span data-ttu-id="87c73-128">Liczba jednostek</span><span class="sxs-lookup"><span data-stu-id="87c73-128">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c73-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87c73-129">-Confirm</span></span>
<span data-ttu-id="87c73-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87c73-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c73-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c73-131">-WhatIf</span></span>
<span data-ttu-id="87c73-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87c73-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87c73-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87c73-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c73-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c73-134">CommonParameters</span></span>
<span data-ttu-id="87c73-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c73-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c73-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c73-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c73-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87c73-137">INPUTS</span></span>

### <span data-ttu-id="87c73-138">System. String</span><span class="sxs-lookup"><span data-stu-id="87c73-138">System.String</span></span>

## <span data-ttu-id="87c73-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87c73-139">OUTPUTS</span></span>

### <span data-ttu-id="87c73-140">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="87c73-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="87c73-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87c73-141">NOTES</span></span>

## <span data-ttu-id="87c73-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87c73-142">RELATED LINKS</span></span>
