---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: af622bbbed98a897df1774303f1417723ebfb32c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894414"
---
# <span data-ttu-id="11cb7-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="11cb7-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="11cb7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="11cb7-103">Tworzy nową aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="11cb7-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="11cb7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11cb7-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11cb7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="11cb7-106">Tworzy nową aplikację centralną IoT z podanych właściwościami i metadanymi.</span><span class="sxs-lookup"><span data-stu-id="11cb7-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="11cb7-107">Aby uzyskać wprowadzenie do programu IoT Central, zobacz https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="11cb7-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="11cb7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11cb7-108">EXAMPLES</span></span>

### <span data-ttu-id="11cb7-109">Przykład 1 Utwórz prostą aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="11cb7-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="11cb7-110">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="11cb7-110">Example Output:</span></span>

<span data-ttu-id="11cb7-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo, identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName subdomain: MyAppSubdomain iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="11cb7-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="11cb7-112">Utwórz aplikację centralną IoT w ST2 standardowej warstwy cenowej w regionie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11cb7-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="11cb7-113">Na przykład 2 Utwórz prostą aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="11cb7-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="11cb7-114">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="11cb7-114">Example Output:</span></span>

<span data-ttu-id="11cb7-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo, identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Moja Poddomena z niestandardową nazwą wyświetlaną: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11cb7-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="11cb7-116">Utwórz aplikację centralną IoT z standardową warstwą cenową ST2 w regionie "zachód" z niestandardową nazwą wyświetlaną na podstawie domyślnego szablonu IOTC.</span><span class="sxs-lookup"><span data-stu-id="11cb7-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="11cb7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11cb7-117">PARAMETERS</span></span>

### <span data-ttu-id="11cb7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11cb7-118">-AsJob</span></span>
<span data-ttu-id="11cb7-119">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="11cb7-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="11cb7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cb7-120">-DefaultProfile</span></span>
<span data-ttu-id="11cb7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11cb7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11cb7-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="11cb7-122">-DisplayName</span></span>
<span data-ttu-id="11cb7-123">Niestandardowa nazwa wyświetlana aplikacji dla komputerów z Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="11cb7-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="11cb7-124">Domyślnie jest to nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="11cb7-124">Default is resource name.</span></span>

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

### <span data-ttu-id="11cb7-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="11cb7-125">-Location</span></span>
<span data-ttu-id="11cb7-126">Lokalizacja aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="11cb7-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="11cb7-127">Domyślnie jest to lokalizacja docelowej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11cb7-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="11cb7-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11cb7-128">-Name</span></span>
<span data-ttu-id="11cb7-129">Nazwa zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="11cb7-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="11cb7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11cb7-130">-ResourceGroupName</span></span>
<span data-ttu-id="11cb7-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11cb7-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="11cb7-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="11cb7-132">-Sku</span></span>
<span data-ttu-id="11cb7-133">Warstwa cenowa dla aplikacji centralnych IoT.</span><span class="sxs-lookup"><span data-stu-id="11cb7-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="11cb7-134">Wartość domyślna to ST2.</span><span class="sxs-lookup"><span data-stu-id="11cb7-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="11cb7-135">-Poddomena</span><span class="sxs-lookup"><span data-stu-id="11cb7-135">-Subdomain</span></span>
<span data-ttu-id="11cb7-136">Poddomena dla centralnego adresu URL usługi IoT.</span><span class="sxs-lookup"><span data-stu-id="11cb7-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="11cb7-137">Każda aplikacja musi mieć unikatową poddomenę.</span><span class="sxs-lookup"><span data-stu-id="11cb7-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="11cb7-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="11cb7-138">-Tag</span></span>
<span data-ttu-id="11cb7-139">Znaczniki zasobów aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="11cb7-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="11cb7-140">— Szablon</span><span class="sxs-lookup"><span data-stu-id="11cb7-140">-Template</span></span>
<span data-ttu-id="11cb7-141">Nazwa szablonu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="11cb7-141">IoT Central application template name.</span></span>
<span data-ttu-id="11cb7-142">Domyślnie jest to aplikacja niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="11cb7-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="11cb7-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11cb7-143">-Confirm</span></span>
<span data-ttu-id="11cb7-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11cb7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11cb7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11cb7-145">-WhatIf</span></span>
<span data-ttu-id="11cb7-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11cb7-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11cb7-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11cb7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11cb7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cb7-148">CommonParameters</span></span>
<span data-ttu-id="11cb7-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11cb7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cb7-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11cb7-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cb7-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11cb7-151">INPUTS</span></span>

### <span data-ttu-id="11cb7-152">System. String</span><span class="sxs-lookup"><span data-stu-id="11cb7-152">System.String</span></span>

### <span data-ttu-id="11cb7-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="11cb7-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="11cb7-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11cb7-154">OUTPUTS</span></span>

### <span data-ttu-id="11cb7-155">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="11cb7-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="11cb7-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11cb7-156">NOTES</span></span>

## <span data-ttu-id="11cb7-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11cb7-157">RELATED LINKS</span></span>
