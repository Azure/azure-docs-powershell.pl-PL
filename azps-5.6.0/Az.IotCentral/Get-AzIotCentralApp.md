---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 2d79857df255bb960c51b87c536013921f3b1c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997991"
---
# <span data-ttu-id="f94b3-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="f94b3-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="f94b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f94b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f94b3-103">Pobiera właściwości jednej lub kilku aplikacji centralnych IoT.</span><span class="sxs-lookup"><span data-stu-id="f94b3-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="f94b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f94b3-104">SYNTAX</span></span>

### <span data-ttu-id="f94b3-105">ListIotCentralAppsParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f94b3-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f94b3-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="f94b3-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f94b3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f94b3-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f94b3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f94b3-108">DESCRIPTION</span></span>
<span data-ttu-id="f94b3-109">Pobiera metadane dla określonej aplikacji centralnej IoT lub wszystkich aplikacji w grupie zasobów lub subskrypcji, w zależności od zestawu parametrów.</span><span class="sxs-lookup"><span data-stu-id="f94b3-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="f94b3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f94b3-110">EXAMPLES</span></span>

### <span data-ttu-id="f94b3-111">Przykład 1. Uzyskiwanie konkretnej aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="f94b3-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="f94b3-112">Pobiera metadane dla określonej aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="f94b3-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="f94b3-113">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="f94b3-113">Example Output:</span></span>

<span data-ttu-id="f94b3-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa poddomena nazwa wyświetlana: Szablon MyAppSubDomain: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f94b3-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="f94b3-115">Przykład 2. Uzyskiwanie aplikacji centralnej aplikacji IoT w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f94b3-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="f94b3-116">Pobiera metadane dla wszystkich aplikacji centralnych IoT w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f94b3-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="f94b3-117">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="f94b3-117">Example Output:</span></span>

<span data-ttu-id="f94b3-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa poddomena nazwa wyświetlana: Szablon MyAppSubDomain: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f94b3-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="f94b3-119">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa nazwa wyświetlana 2 poddomena: Szablon MyAppSubDomain2: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="f94b3-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="f94b3-120">Przykład 3. Uzyskiwanie aplikacji centralnej aplikacji IoT w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f94b3-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="f94b3-121">Pobiera metadane dla wszystkich aplikacji centralnych IoT w podanej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f94b3-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="f94b3-122">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="f94b3-122">Example Output:</span></span>

<span data-ttu-id="f94b3-123">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa poddomena nazwa wyświetlana: Szablon MyAppSubDomain: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f94b3-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="f94b3-124">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa nazwa wyświetlana 2 poddomena: Szablon MyAppSubDomain2: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f94b3-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="f94b3-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f94b3-125">PARAMETERS</span></span>

### <span data-ttu-id="f94b3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f94b3-126">-DefaultProfile</span></span>
<span data-ttu-id="f94b3-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f94b3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f94b3-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f94b3-128">-Name</span></span>
<span data-ttu-id="f94b3-129">Nazwa centralnego zasobu aplikacji IOT.</span><span class="sxs-lookup"><span data-stu-id="f94b3-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="f94b3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f94b3-130">-ResourceGroupName</span></span>
<span data-ttu-id="f94b3-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f94b3-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="f94b3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f94b3-132">-ResourceId</span></span>
<span data-ttu-id="f94b3-133">Identyfikator zasobu aplikacji centralnej.</span><span class="sxs-lookup"><span data-stu-id="f94b3-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="f94b3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94b3-134">CommonParameters</span></span>
<span data-ttu-id="f94b3-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f94b3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94b3-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f94b3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94b3-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f94b3-137">INPUTS</span></span>

### <span data-ttu-id="f94b3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f94b3-138">System.String</span></span>

## <span data-ttu-id="f94b3-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f94b3-139">OUTPUTS</span></span>

### <span data-ttu-id="f94b3-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="f94b3-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="f94b3-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f94b3-141">NOTES</span></span>

## <span data-ttu-id="f94b3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f94b3-142">RELATED LINKS</span></span>
