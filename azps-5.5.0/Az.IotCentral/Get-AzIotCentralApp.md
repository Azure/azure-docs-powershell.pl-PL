---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203912"
---
# <span data-ttu-id="7faf5-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7faf5-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="7faf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7faf5-102">SYNOPSIS</span></span>
<span data-ttu-id="7faf5-103">Pobiera właściwości jednej lub kilku aplikacji centralnych IoT.</span><span class="sxs-lookup"><span data-stu-id="7faf5-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="7faf5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7faf5-104">SYNTAX</span></span>

### <span data-ttu-id="7faf5-105">ListIotCentralAppsParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7faf5-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7faf5-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="7faf5-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7faf5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7faf5-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7faf5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7faf5-108">DESCRIPTION</span></span>
<span data-ttu-id="7faf5-109">Pobiera metadane dla określonej aplikacji centralnej IoT lub wszystkich aplikacji w grupie zasobów lub subskrypcji, w zależności od zestawu parametrów.</span><span class="sxs-lookup"><span data-stu-id="7faf5-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="7faf5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7faf5-110">EXAMPLES</span></span>

### <span data-ttu-id="7faf5-111">Przykład 1. Uzyskiwanie konkretnej aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="7faf5-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="7faf5-112">Pobiera metadane dla określonej aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="7faf5-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="7faf5-113">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="7faf5-113">Example Output:</span></span>

<span data-ttu-id="7faf5-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa poddomena nazwa wyświetlana: Szablon MyAppSubDomain: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7faf5-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="7faf5-115">Przykład 2. Uzyskiwanie aplikacji centralnej aplikacji IoT w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7faf5-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="7faf5-116">Pobiera metadane dla wszystkich aplikacji centralnych IoT w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7faf5-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="7faf5-117">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="7faf5-117">Example Output:</span></span>

<span data-ttu-id="7faf5-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa poddomena nazwa wyświetlana: Szablon MyAppSubDomain: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7faf5-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="7faf5-119">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa nazwa wyświetlana 2 poddomeny: Szablon MyAppSubDomain2: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="7faf5-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="7faf5-120">Przykład 3. Uzyskiwanie aplikacji centralnej aplikacji IoT w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7faf5-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="7faf5-121">Pobiera metadane dla wszystkich aplikacji centralnych IoT w podanej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7faf5-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="7faf5-122">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="7faf5-122">Example Output:</span></span>

<span data-ttu-id="7faf5-123">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa poddomena nazwa wyświetlana: Szablon MyAppSubDomain: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7faf5-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="7faf5-124">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa nazwa wyświetlana 2 poddomena: Szablon MyAppSubDomain2: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7faf5-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="7faf5-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7faf5-125">PARAMETERS</span></span>

### <span data-ttu-id="7faf5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7faf5-126">-DefaultProfile</span></span>
<span data-ttu-id="7faf5-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7faf5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7faf5-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7faf5-128">-Name</span></span>
<span data-ttu-id="7faf5-129">Nazwa centralnego zasobu aplikacji IOT.</span><span class="sxs-lookup"><span data-stu-id="7faf5-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="7faf5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7faf5-130">-ResourceGroupName</span></span>
<span data-ttu-id="7faf5-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7faf5-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="7faf5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7faf5-132">-ResourceId</span></span>
<span data-ttu-id="7faf5-133">Identyfikator zasobu aplikacji centralnej.</span><span class="sxs-lookup"><span data-stu-id="7faf5-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="7faf5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7faf5-134">CommonParameters</span></span>
<span data-ttu-id="7faf5-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7faf5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7faf5-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7faf5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7faf5-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7faf5-137">INPUTS</span></span>

### <span data-ttu-id="7faf5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7faf5-138">System.String</span></span>

## <span data-ttu-id="7faf5-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7faf5-139">OUTPUTS</span></span>

### <span data-ttu-id="7faf5-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7faf5-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="7faf5-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7faf5-141">NOTES</span></span>

## <span data-ttu-id="7faf5-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7faf5-142">RELATED LINKS</span></span>
