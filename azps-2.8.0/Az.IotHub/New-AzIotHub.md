---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: f3ee19d5389958741e8258db8b807acce7494ff8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705228"
---
# <span data-ttu-id="cbf67-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="cbf67-101">New-AzIotHub</span></span>

## <span data-ttu-id="cbf67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbf67-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf67-103">Tworzy nowy IotHub.</span><span class="sxs-lookup"><span data-stu-id="cbf67-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="cbf67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbf67-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbf67-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cbf67-105">DESCRIPTION</span></span>
<span data-ttu-id="cbf67-106">Tworzy nowy IotHub.</span><span class="sxs-lookup"><span data-stu-id="cbf67-106">Creates a new IotHub.</span></span>
<span data-ttu-id="cbf67-107">IotHub można utworzyć przy użyciu właściwości domyślnych lub określać właściwości wejścia.</span><span class="sxs-lookup"><span data-stu-id="cbf67-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="cbf67-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbf67-108">EXAMPLES</span></span>

### <span data-ttu-id="cbf67-109">Przykład 1 Tworzenie nowego IotHub z właściwościami domyślnymi</span><span class="sxs-lookup"><span data-stu-id="cbf67-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="cbf67-110">Tworzy nowy IotHub o nazwie "myiothub" w wersji SKU "S1", wydajności 1 i lokalizacji "northeurope".</span><span class="sxs-lookup"><span data-stu-id="cbf67-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="cbf67-111">Przykład 2 Utwórz nowy IotHub z MaxDeliveryCount kolejki CloudToDevice o wartości 20</span><span class="sxs-lookup"><span data-stu-id="cbf67-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="cbf67-112">Tworzy nowy IotHub o nazwie "myiothub" w wersji SKU "S1", wydajności 1 i lokalizacji "northeurope" z zaawansowanymi właściwościami wejściowymi przedstawionymi przez $properties.</span><span class="sxs-lookup"><span data-stu-id="cbf67-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="cbf67-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. MODELES. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "Moja resourceName"-name-myiothub</span><span class="sxs-lookup"><span data-stu-id="cbf67-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="cbf67-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbf67-114">PARAMETERS</span></span>

### <span data-ttu-id="cbf67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf67-115">-DefaultProfile</span></span>
<span data-ttu-id="cbf67-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cbf67-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbf67-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cbf67-117">-Location</span></span>
<span data-ttu-id="cbf67-118">Lokalizacja, w której należy utworzyć Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="cbf67-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="cbf67-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cbf67-119">-Name</span></span>
<span data-ttu-id="cbf67-120">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="cbf67-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="cbf67-121">-Properties</span><span class="sxs-lookup"><span data-stu-id="cbf67-121">-Properties</span></span>
<span data-ttu-id="cbf67-122">Właściwości Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="cbf67-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="cbf67-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf67-123">-ResourceGroupName</span></span>
<span data-ttu-id="cbf67-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cbf67-124">Resource Group Name</span></span>

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

### <span data-ttu-id="cbf67-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cbf67-125">-SkuName</span></span>
<span data-ttu-id="cbf67-126">Nazwa jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="cbf67-126">Name of the sku</span></span>

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

### <span data-ttu-id="cbf67-127">-Jednostki</span><span class="sxs-lookup"><span data-stu-id="cbf67-127">-Units</span></span>
<span data-ttu-id="cbf67-128">Liczba jednostek</span><span class="sxs-lookup"><span data-stu-id="cbf67-128">Number of units</span></span>

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

### <span data-ttu-id="cbf67-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cbf67-129">-Confirm</span></span>
<span data-ttu-id="cbf67-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbf67-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbf67-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbf67-131">-WhatIf</span></span>
<span data-ttu-id="cbf67-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbf67-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbf67-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cbf67-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbf67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf67-134">CommonParameters</span></span>
<span data-ttu-id="cbf67-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf67-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf67-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf67-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbf67-137">INPUTS</span></span>

### <span data-ttu-id="cbf67-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cbf67-138">System.String</span></span>

## <span data-ttu-id="cbf67-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbf67-139">OUTPUTS</span></span>

### <span data-ttu-id="cbf67-140">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cbf67-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="cbf67-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbf67-141">NOTES</span></span>

## <span data-ttu-id="cbf67-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbf67-142">RELATED LINKS</span></span>