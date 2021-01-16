---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342010"
---
# <span data-ttu-id="6e558-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="6e558-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="6e558-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e558-102">SYNOPSIS</span></span>
<span data-ttu-id="6e558-103">Tworzy nową aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="6e558-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="6e558-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e558-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e558-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e558-105">DESCRIPTION</span></span>
<span data-ttu-id="6e558-106">Tworzy nową aplikację centralną IoT z podanych właściwościami i metadanymi.</span><span class="sxs-lookup"><span data-stu-id="6e558-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="6e558-107">Aby uzyskać wprowadzenie do programu IoT Central, zobacz https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="6e558-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="6e558-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e558-108">EXAMPLES</span></span>

### <span data-ttu-id="6e558-109">Przykład 1 Utwórz prostą aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="6e558-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="6e558-110">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="6e558-110">Example Output:</span></span>

<span data-ttu-id="6e558-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo, identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName subdomain: MyAppSubdomain iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="6e558-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="6e558-112">Utwórz aplikację centralną IoT w ST2 standardowej warstwy cenowej w regionie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e558-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="6e558-113">Na przykład 2 Utwórz prostą aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="6e558-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="6e558-114">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="6e558-114">Example Output:</span></span>

<span data-ttu-id="6e558-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo, identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Moja Poddomena z niestandardową nazwą wyświetlaną: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e558-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="6e558-116">Utwórz aplikację centralną IoT z standardową warstwą cenową ST2 w regionie "zachód" z niestandardową nazwą wyświetlaną na podstawie domyślnego szablonu IOTC.</span><span class="sxs-lookup"><span data-stu-id="6e558-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="6e558-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e558-117">PARAMETERS</span></span>

### <span data-ttu-id="6e558-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e558-118">-AsJob</span></span>
<span data-ttu-id="6e558-119">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="6e558-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="6e558-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e558-120">-DefaultProfile</span></span>
<span data-ttu-id="6e558-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e558-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e558-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6e558-122">-DisplayName</span></span>
<span data-ttu-id="6e558-123">Niestandardowa nazwa wyświetlana aplikacji dla komputerów z Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="6e558-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="6e558-124">Domyślnie jest to nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6e558-124">Default is resource name.</span></span>

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

### <span data-ttu-id="6e558-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6e558-125">-Location</span></span>
<span data-ttu-id="6e558-126">Lokalizacja aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="6e558-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="6e558-127">Domyślnie jest to lokalizacja docelowej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e558-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="6e558-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e558-128">-Name</span></span>
<span data-ttu-id="6e558-129">Nazwa zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="6e558-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="6e558-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e558-130">-ResourceGroupName</span></span>
<span data-ttu-id="6e558-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e558-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="6e558-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="6e558-132">-Sku</span></span>
<span data-ttu-id="6e558-133">Warstwa cenowa dla aplikacji centralnych IoT.</span><span class="sxs-lookup"><span data-stu-id="6e558-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="6e558-134">Wartość domyślna to ST2.</span><span class="sxs-lookup"><span data-stu-id="6e558-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="6e558-135">-Poddomena</span><span class="sxs-lookup"><span data-stu-id="6e558-135">-Subdomain</span></span>
<span data-ttu-id="6e558-136">Poddomena dla centralnego adresu URL usługi IoT.</span><span class="sxs-lookup"><span data-stu-id="6e558-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="6e558-137">Każda aplikacja musi mieć unikatową poddomenę.</span><span class="sxs-lookup"><span data-stu-id="6e558-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="6e558-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="6e558-138">-Tag</span></span>
<span data-ttu-id="6e558-139">Znaczniki zasobów aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="6e558-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="6e558-140">— Szablon</span><span class="sxs-lookup"><span data-stu-id="6e558-140">-Template</span></span>
<span data-ttu-id="6e558-141">Nazwa szablonu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="6e558-141">IoT Central application template name.</span></span>
<span data-ttu-id="6e558-142">Domyślnie jest to aplikacja niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="6e558-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="6e558-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e558-143">-Confirm</span></span>
<span data-ttu-id="6e558-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e558-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e558-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e558-145">-WhatIf</span></span>
<span data-ttu-id="6e558-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e558-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e558-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e558-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e558-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e558-148">CommonParameters</span></span>
<span data-ttu-id="6e558-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e558-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e558-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e558-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e558-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e558-151">INPUTS</span></span>

### <span data-ttu-id="6e558-152">System. String</span><span class="sxs-lookup"><span data-stu-id="6e558-152">System.String</span></span>

### <span data-ttu-id="6e558-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6e558-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6e558-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e558-154">OUTPUTS</span></span>

### <span data-ttu-id="6e558-155">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="6e558-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="6e558-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e558-156">NOTES</span></span>

## <span data-ttu-id="6e558-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e558-157">RELATED LINKS</span></span>
