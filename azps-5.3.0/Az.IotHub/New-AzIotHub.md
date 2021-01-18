---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 392f9362df1cafdb6c047020b3381a7b16320607
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503389"
---
# <span data-ttu-id="bae7c-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="bae7c-101">New-AzIotHub</span></span>

## <span data-ttu-id="bae7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bae7c-102">SYNOPSIS</span></span>
<span data-ttu-id="bae7c-103">Tworzy nowy IotHub.</span><span class="sxs-lookup"><span data-stu-id="bae7c-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="bae7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bae7c-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bae7c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bae7c-105">DESCRIPTION</span></span>
<span data-ttu-id="bae7c-106">Tworzy nowy IotHub.</span><span class="sxs-lookup"><span data-stu-id="bae7c-106">Creates a new IotHub.</span></span>
<span data-ttu-id="bae7c-107">IotHub można utworzyć przy użyciu właściwości domyślnych lub określać właściwości wejścia.</span><span class="sxs-lookup"><span data-stu-id="bae7c-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="bae7c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bae7c-108">EXAMPLES</span></span>

### <span data-ttu-id="bae7c-109">Przykład 1 Tworzenie nowego IotHub z właściwościami domyślnymi</span><span class="sxs-lookup"><span data-stu-id="bae7c-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="bae7c-110">Tworzy nowy IotHub o nazwie "myiothub" w wersji SKU "S1", pojemności 1 i lokalizacji "northeurope", która jest uwzględniona w tagach.</span><span class="sxs-lookup"><span data-stu-id="bae7c-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="bae7c-111">Przykład 2 Utwórz nowy IotHub z MaxDeliveryCount kolejki CloudToDevice o wartości 20</span><span class="sxs-lookup"><span data-stu-id="bae7c-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="bae7c-112">Tworzy nowy IotHub o nazwie "myiothub" w wersji SKU "S1", wydajności 1 i lokalizacji "northeurope" z zaawansowanymi właściwościami wejściowymi przedstawionymi przez $properties.</span><span class="sxs-lookup"><span data-stu-id="bae7c-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="bae7c-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. MODELES. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "Moja resourceName"-name-myiothub</span><span class="sxs-lookup"><span data-stu-id="bae7c-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="bae7c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bae7c-114">PARAMETERS</span></span>

### <span data-ttu-id="bae7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bae7c-115">-DefaultProfile</span></span>
<span data-ttu-id="bae7c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bae7c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bae7c-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bae7c-117">-Location</span></span>
<span data-ttu-id="bae7c-118">Lokalizacja, w której należy utworzyć Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="bae7c-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="bae7c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bae7c-119">-Name</span></span>
<span data-ttu-id="bae7c-120">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="bae7c-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="bae7c-121">-Properties</span><span class="sxs-lookup"><span data-stu-id="bae7c-121">-Properties</span></span>
<span data-ttu-id="bae7c-122">Właściwości Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="bae7c-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="bae7c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bae7c-123">-ResourceGroupName</span></span>
<span data-ttu-id="bae7c-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bae7c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="bae7c-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bae7c-125">-SkuName</span></span>
<span data-ttu-id="bae7c-126">Nazwa jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="bae7c-126">Name of the sku</span></span>

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

### <span data-ttu-id="bae7c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="bae7c-127">-Tag</span></span>
<span data-ttu-id="bae7c-128">Znaczniki wystąpienia Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="bae7c-128">IoT hub instance tags.</span></span> <span data-ttu-id="bae7c-129">Zbiór właściwości w postaci par klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="bae7c-129">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bae7c-130">-Jednostki</span><span class="sxs-lookup"><span data-stu-id="bae7c-130">-Units</span></span>
<span data-ttu-id="bae7c-131">Liczba jednostek</span><span class="sxs-lookup"><span data-stu-id="bae7c-131">Number of units</span></span>

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

### <span data-ttu-id="bae7c-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bae7c-132">-Confirm</span></span>
<span data-ttu-id="bae7c-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bae7c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bae7c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bae7c-134">-WhatIf</span></span>
<span data-ttu-id="bae7c-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bae7c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bae7c-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bae7c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bae7c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bae7c-137">CommonParameters</span></span>
<span data-ttu-id="bae7c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bae7c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bae7c-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bae7c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bae7c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bae7c-140">INPUTS</span></span>

### <span data-ttu-id="bae7c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bae7c-141">System.String</span></span>

## <span data-ttu-id="bae7c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bae7c-142">OUTPUTS</span></span>

### <span data-ttu-id="bae7c-143">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bae7c-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="bae7c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bae7c-144">NOTES</span></span>

## <span data-ttu-id="bae7c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bae7c-145">RELATED LINKS</span></span>
