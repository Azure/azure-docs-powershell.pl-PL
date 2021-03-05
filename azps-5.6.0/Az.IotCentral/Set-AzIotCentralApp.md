---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: f99faf1ce7420212e87c894c8f5aadeb16578334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997963"
---
# <span data-ttu-id="8ee26-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="8ee26-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="8ee26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee26-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee26-103">Aktualizuje metadane dla aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="8ee26-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="8ee26-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ee26-104">SYNTAX</span></span>

### <span data-ttu-id="8ee26-105">ResourceIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8ee26-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ee26-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ee26-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ee26-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ee26-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ee26-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ee26-108">DESCRIPTION</span></span>
<span data-ttu-id="8ee26-109">Aktualizowanie metadanych aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="8ee26-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="8ee26-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ee26-110">EXAMPLES</span></span>

### <span data-ttu-id="8ee26-111">Przykład 1. Aktualizowanie nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="8ee26-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="8ee26-112">Aktualizowanie nazwy wyświetlanej w istniejącej aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="8ee26-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="8ee26-113">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="8ee26-113">Example Output:</span></span>

<span data-ttu-id="8ee26-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My New Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee26-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="8ee26-115">Przykład 2. Poddomena aktualizacji</span><span class="sxs-lookup"><span data-stu-id="8ee26-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="8ee26-116">Aktualizowanie nazwy wyświetlanej w istniejącej aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="8ee26-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="8ee26-117">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="8ee26-117">Example Output:</span></span>

<span data-ttu-id="8ee26-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Display Name Subdomain : new-subdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee26-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="8ee26-119">Przykład 3. Zaktualizuj informacje o wersji SKU aplikacji</span><span class="sxs-lookup"><span data-stu-id="8ee26-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="8ee26-120">Zaktualizuj sku w istniejącej aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="8ee26-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="8ee26-121">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="8ee26-121">Example Output:</span></span>

<span data-ttu-id="8ee26-122">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee26-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="8ee26-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ee26-123">PARAMETERS</span></span>

### <span data-ttu-id="8ee26-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8ee26-124">-AsJob</span></span>
<span data-ttu-id="8ee26-125">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="8ee26-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="8ee26-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee26-126">-DefaultProfile</span></span>
<span data-ttu-id="8ee26-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ee26-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ee26-128">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="8ee26-128">-DisplayName</span></span>
<span data-ttu-id="8ee26-129">Niestandardowa nazwa wyświetlana aplikacji centralnej systemu Iot.</span><span class="sxs-lookup"><span data-stu-id="8ee26-129">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee26-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ee26-130">-InputObject</span></span>
<span data-ttu-id="8ee26-131">Iot Central Application Input Object.</span><span class="sxs-lookup"><span data-stu-id="8ee26-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee26-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8ee26-132">-Name</span></span>
<span data-ttu-id="8ee26-133">Nazwa centralnego zasobu aplikacji IOT.</span><span class="sxs-lookup"><span data-stu-id="8ee26-133">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee26-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee26-134">-ResourceGroupName</span></span>
<span data-ttu-id="8ee26-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8ee26-135">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee26-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ee26-136">-ResourceId</span></span>
<span data-ttu-id="8ee26-137">Identyfikator zasobu aplikacji centralnej.</span><span class="sxs-lookup"><span data-stu-id="8ee26-137">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee26-138">- SKU</span><span class="sxs-lookup"><span data-stu-id="8ee26-138">-Sku</span></span>
<span data-ttu-id="8ee26-139">Warstwa cenowa aplikacji IoT Central.</span><span class="sxs-lookup"><span data-stu-id="8ee26-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="8ee26-140">Wartość domyślna to ST2.</span><span class="sxs-lookup"><span data-stu-id="8ee26-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="8ee26-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="8ee26-141">-Subdomain</span></span>
<span data-ttu-id="8ee26-142">Poddomena aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="8ee26-142">Subdomain of the IoT Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee26-143">— Tag</span><span class="sxs-lookup"><span data-stu-id="8ee26-143">-Tag</span></span>
<span data-ttu-id="8ee26-144">Tagi zasobów aplikacji centralnej.</span><span class="sxs-lookup"><span data-stu-id="8ee26-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="8ee26-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ee26-145">-Confirm</span></span>
<span data-ttu-id="8ee26-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8ee26-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ee26-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ee26-147">-WhatIf</span></span>
<span data-ttu-id="8ee26-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ee26-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ee26-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8ee26-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ee26-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee26-150">CommonParameters</span></span>
<span data-ttu-id="8ee26-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee26-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee26-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ee26-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee26-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ee26-153">INPUTS</span></span>

### <span data-ttu-id="8ee26-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8ee26-154">System.String</span></span>

### <span data-ttu-id="8ee26-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="8ee26-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="8ee26-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ee26-156">OUTPUTS</span></span>

### <span data-ttu-id="8ee26-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="8ee26-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="8ee26-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ee26-158">NOTES</span></span>

## <span data-ttu-id="8ee26-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ee26-159">RELATED LINKS</span></span>
