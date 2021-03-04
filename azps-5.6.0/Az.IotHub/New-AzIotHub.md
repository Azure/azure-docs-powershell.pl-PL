---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 71f5e9805467bc285b991a9aa4ee289b3d807729
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987841"
---
# <span data-ttu-id="4ed17-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="4ed17-101">New-AzIotHub</span></span>

## <span data-ttu-id="4ed17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed17-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed17-103">Tworzy nową iotHub.</span><span class="sxs-lookup"><span data-stu-id="4ed17-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="4ed17-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4ed17-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed17-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4ed17-105">DESCRIPTION</span></span>
<span data-ttu-id="4ed17-106">Tworzy nową iotHub.</span><span class="sxs-lookup"><span data-stu-id="4ed17-106">Creates a new IotHub.</span></span>
<span data-ttu-id="4ed17-107">Możesz utworzyć usługę IotHub przy użyciu właściwości domyślnych lub określić właściwości wprowadzania.</span><span class="sxs-lookup"><span data-stu-id="4ed17-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="4ed17-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4ed17-108">EXAMPLES</span></span>

### <span data-ttu-id="4ed17-109">Przykład 1. Tworzenie nowej aplikacji IotHub z właściwościami domyślnymi</span><span class="sxs-lookup"><span data-stu-id="4ed17-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="4ed17-110">Tworzy nową iotHub o nazwie "myiothub" z sku "S1", pojemności 1 i lokalizacji "northeurope" dołączonej do tagów.</span><span class="sxs-lookup"><span data-stu-id="4ed17-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="4ed17-111">Przykład 2. Tworzenie nowej aplikacji IotHub z ustawieniem MaxDeliveryCount kolejki CloudToDevice na wartość 20</span><span class="sxs-lookup"><span data-stu-id="4ed17-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="4ed17-112">Tworzy nową usługę IotHub o nazwie "myiothub" z sku "S1", wydajności 1 i lokalizacji "northeurope" z zaawansowanymi właściwościami wejściowymi reprezentowanymi przez $properties.</span><span class="sxs-lookup"><span data-stu-id="4ed17-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="4ed17-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span><span class="sxs-lookup"><span data-stu-id="4ed17-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="4ed17-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ed17-114">PARAMETERS</span></span>

### <span data-ttu-id="4ed17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed17-115">-DefaultProfile</span></span>
<span data-ttu-id="4ed17-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4ed17-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ed17-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4ed17-117">-Location</span></span>
<span data-ttu-id="4ed17-118">Lokalizacja, w której należy utworzyć centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="4ed17-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="4ed17-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4ed17-119">-Name</span></span>
<span data-ttu-id="4ed17-120">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="4ed17-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="4ed17-121">— Properties</span><span class="sxs-lookup"><span data-stu-id="4ed17-121">-Properties</span></span>
<span data-ttu-id="4ed17-122">Właściwości centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="4ed17-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="4ed17-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed17-123">-ResourceGroupName</span></span>
<span data-ttu-id="4ed17-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4ed17-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4ed17-125">-SKUName</span><span class="sxs-lookup"><span data-stu-id="4ed17-125">-SkuName</span></span>
<span data-ttu-id="4ed17-126">Nazwa sKU</span><span class="sxs-lookup"><span data-stu-id="4ed17-126">Name of the sku</span></span>

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

### <span data-ttu-id="4ed17-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="4ed17-127">-Tag</span></span>
<span data-ttu-id="4ed17-128">Tagi wystąpień centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="4ed17-128">IoT hub instance tags.</span></span> <span data-ttu-id="4ed17-129">Work property bag in key-value pairs in the form of a hash table.</span><span class="sxs-lookup"><span data-stu-id="4ed17-129">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="4ed17-130">— Jednostki</span><span class="sxs-lookup"><span data-stu-id="4ed17-130">-Units</span></span>
<span data-ttu-id="4ed17-131">Liczba jednostek</span><span class="sxs-lookup"><span data-stu-id="4ed17-131">Number of units</span></span>

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

### <span data-ttu-id="4ed17-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ed17-132">-Confirm</span></span>
<span data-ttu-id="4ed17-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4ed17-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed17-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed17-134">-WhatIf</span></span>
<span data-ttu-id="4ed17-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed17-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed17-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4ed17-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed17-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed17-137">CommonParameters</span></span>
<span data-ttu-id="4ed17-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed17-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed17-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed17-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed17-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ed17-140">INPUTS</span></span>

### <span data-ttu-id="4ed17-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4ed17-141">System.String</span></span>

## <span data-ttu-id="4ed17-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ed17-142">OUTPUTS</span></span>

### <span data-ttu-id="4ed17-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4ed17-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="4ed17-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4ed17-144">NOTES</span></span>

## <span data-ttu-id="4ed17-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ed17-145">RELATED LINKS</span></span>
