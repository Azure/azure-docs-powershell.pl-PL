---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187650"
---
# <span data-ttu-id="2de34-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="2de34-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="2de34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2de34-102">SYNOPSIS</span></span>
<span data-ttu-id="2de34-103">Tworzy nową aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="2de34-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="2de34-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2de34-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2de34-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2de34-105">DESCRIPTION</span></span>
<span data-ttu-id="2de34-106">Tworzy nową aplikację centralną IoT z dostarczonymi właściwościami i metadanymi.</span><span class="sxs-lookup"><span data-stu-id="2de34-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="2de34-107">Aby uzyskać wprowadzenie do aplikacji IoT Central, zobacz https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="2de34-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="2de34-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2de34-108">EXAMPLES</span></span>

### <span data-ttu-id="2de34-109">Przykład 1. Tworzenie prostej aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="2de34-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="2de34-110">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="2de34-110">Example Output:</span></span>

<span data-ttu-id="2de34-111">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Poddomena MyAppResourceName: Szablon MyAppSubdomain iotc-default@1.0.0 : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de34-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="2de34-112">Utwórz aplikację centralną IoT w standardowej warstwie cenowej ST2 w regionie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2de34-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="2de34-113">Przykład 2. Tworzenie prostej aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="2de34-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="2de34-114">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="2de34-114">Example Output:</span></span>

<span data-ttu-id="2de34-115">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de34-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="2de34-116">Utwórz aplikację centralną IoT ze standardową warstwą cenOWĄ ST2 w regionie "zachód", z niestandardową nazwą wyświetlaną opartą na szablonie domyślnym iotc.</span><span class="sxs-lookup"><span data-stu-id="2de34-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="2de34-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2de34-117">PARAMETERS</span></span>

### <span data-ttu-id="2de34-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2de34-118">-AsJob</span></span>
<span data-ttu-id="2de34-119">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="2de34-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de34-120">-DefaultProfile</span></span>
<span data-ttu-id="2de34-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2de34-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2de34-122">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="2de34-122">-DisplayName</span></span>
<span data-ttu-id="2de34-123">Niestandardowa nazwa wyświetlana aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="2de34-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="2de34-124">Wartością domyślną jest nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="2de34-124">Default is resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de34-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2de34-125">-Location</span></span>
<span data-ttu-id="2de34-126">Lokalizacja aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="2de34-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="2de34-127">Domyślną lokalizacją jest docelowa grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="2de34-127">Default is the location of target resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de34-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2de34-128">-Name</span></span>
<span data-ttu-id="2de34-129">Nazwa centralnego zasobu aplikacji IOT.</span><span class="sxs-lookup"><span data-stu-id="2de34-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de34-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de34-130">-ResourceGroupName</span></span>
<span data-ttu-id="2de34-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2de34-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de34-132">- SKU</span><span class="sxs-lookup"><span data-stu-id="2de34-132">-Sku</span></span>
<span data-ttu-id="2de34-133">Warstwa cenowa aplikacji IoT Central.</span><span class="sxs-lookup"><span data-stu-id="2de34-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="2de34-134">Wartość domyślna to ST2.</span><span class="sxs-lookup"><span data-stu-id="2de34-134">Default value is ST2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de34-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="2de34-135">-Subdomain</span></span>
<span data-ttu-id="2de34-136">Poddomena centralnego adresu URL usługi IoT.</span><span class="sxs-lookup"><span data-stu-id="2de34-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="2de34-137">Każda aplikacja musi mieć unikatową poddomenę.</span><span class="sxs-lookup"><span data-stu-id="2de34-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de34-138">— Tag</span><span class="sxs-lookup"><span data-stu-id="2de34-138">-Tag</span></span>
<span data-ttu-id="2de34-139">Tagi zasobów aplikacji centralnej.</span><span class="sxs-lookup"><span data-stu-id="2de34-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de34-140">— Szablon</span><span class="sxs-lookup"><span data-stu-id="2de34-140">-Template</span></span>
<span data-ttu-id="2de34-141">Nazwa szablonu aplikacji IoT Central.</span><span class="sxs-lookup"><span data-stu-id="2de34-141">IoT Central application template name.</span></span>
<span data-ttu-id="2de34-142">Ustawieniem domyślnym jest aplikacja niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="2de34-142">Default is a custom application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de34-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2de34-143">-Confirm</span></span>
<span data-ttu-id="2de34-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2de34-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de34-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de34-145">-WhatIf</span></span>
<span data-ttu-id="2de34-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2de34-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2de34-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2de34-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de34-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de34-148">CommonParameters</span></span>
<span data-ttu-id="2de34-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de34-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de34-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2de34-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de34-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2de34-151">INPUTS</span></span>

### <span data-ttu-id="2de34-152">System.String</span><span class="sxs-lookup"><span data-stu-id="2de34-152">System.String</span></span>

### <span data-ttu-id="2de34-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2de34-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2de34-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2de34-154">OUTPUTS</span></span>

### <span data-ttu-id="2de34-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="2de34-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="2de34-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2de34-156">NOTES</span></span>

## <span data-ttu-id="2de34-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2de34-157">RELATED LINKS</span></span>
