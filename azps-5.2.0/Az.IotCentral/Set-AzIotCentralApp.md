---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348133"
---
# <span data-ttu-id="fa0cd-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="fa0cd-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="fa0cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0cd-103">Aktualizuje metadane aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="fa0cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa0cd-104">SYNTAX</span></span>

### <span data-ttu-id="fa0cd-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fa0cd-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa0cd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa0cd-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa0cd-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa0cd-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa0cd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fa0cd-108">DESCRIPTION</span></span>
<span data-ttu-id="fa0cd-109">Zaktualizuj metadane dla aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="fa0cd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa0cd-110">EXAMPLES</span></span>

### <span data-ttu-id="fa0cd-111">Przykład 1 aktualizacja nazwa wyświetlana</span><span class="sxs-lookup"><span data-stu-id="fa0cd-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="fa0cd-112">Zaktualizuj nazwę wyświetlaną w istniejącej aplikacji do centralnego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="fa0cd-113">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="fa0cd-113">Example Output:</span></span>

<span data-ttu-id="fa0cd-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Nowa niestandardowa nazwa wyświetlana: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa0cd-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="fa0cd-115">Przykład 2 Aktualizacja poddomeny</span><span class="sxs-lookup"><span data-stu-id="fa0cd-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="fa0cd-116">Zaktualizuj nazwę wyświetlaną w istniejącej aplikacji do centralnego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="fa0cd-117">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="fa0cd-117">Example Output:</span></span>

<span data-ttu-id="fa0cd-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: SKU: Microsoft. Azure. Commands. IoTCentral. modele. PSIotCentralAppSkuInfo, identyfikator: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: "Display Name subdomain": szablon: iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="fa0cd-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="fa0cd-119">Przykład 3 aktualizacja informacji o wersji SKU aplikacji</span><span class="sxs-lookup"><span data-stu-id="fa0cd-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="fa0cd-120">Zaktualizuj jednostkę SKU w istniejącej aplikacji dla usługi IoT Central.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="fa0cd-121">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="fa0cd-121">Example Output:</span></span>

<span data-ttu-id="fa0cd-122">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Nazwa wyświetlana poddomena: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa0cd-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="fa0cd-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa0cd-123">PARAMETERS</span></span>

### <span data-ttu-id="fa0cd-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa0cd-124">-AsJob</span></span>
<span data-ttu-id="fa0cd-125">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="fa0cd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa0cd-126">-DefaultProfile</span></span>
<span data-ttu-id="fa0cd-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa0cd-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fa0cd-128">-DisplayName</span></span>
<span data-ttu-id="fa0cd-129">Niestandardowa nazwa wyświetlana aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="fa0cd-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fa0cd-130">-InputObject</span></span>
<span data-ttu-id="fa0cd-131">Obiekt wejściowy aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-131">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="fa0cd-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa0cd-132">-Name</span></span>
<span data-ttu-id="fa0cd-133">Nazwa zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="fa0cd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa0cd-134">-ResourceGroupName</span></span>
<span data-ttu-id="fa0cd-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="fa0cd-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa0cd-136">-ResourceId</span></span>
<span data-ttu-id="fa0cd-137">Identyfikator zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="fa0cd-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="fa0cd-138">-Sku</span></span>
<span data-ttu-id="fa0cd-139">Warstwa cenowa dla aplikacji centralnych IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="fa0cd-140">Wartość domyślna to ST2.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="fa0cd-141">-Poddomena</span><span class="sxs-lookup"><span data-stu-id="fa0cd-141">-Subdomain</span></span>
<span data-ttu-id="fa0cd-142">Poddomena aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="fa0cd-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="fa0cd-143">-Tag</span></span>
<span data-ttu-id="fa0cd-144">Znaczniki zasobów aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="fa0cd-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa0cd-145">-Confirm</span></span>
<span data-ttu-id="fa0cd-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa0cd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa0cd-147">-WhatIf</span></span>
<span data-ttu-id="fa0cd-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa0cd-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa0cd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0cd-150">CommonParameters</span></span>
<span data-ttu-id="fa0cd-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa0cd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0cd-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa0cd-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0cd-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa0cd-153">INPUTS</span></span>

### <span data-ttu-id="fa0cd-154">System. String</span><span class="sxs-lookup"><span data-stu-id="fa0cd-154">System.String</span></span>

### <span data-ttu-id="fa0cd-155">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="fa0cd-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="fa0cd-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa0cd-156">OUTPUTS</span></span>

### <span data-ttu-id="fa0cd-157">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="fa0cd-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="fa0cd-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa0cd-158">NOTES</span></span>

## <span data-ttu-id="fa0cd-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa0cd-159">RELATED LINKS</span></span>
