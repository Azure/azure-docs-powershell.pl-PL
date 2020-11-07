---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/get-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
ms.openlocfilehash: fdf674b5ec2dfcefe8fcada92cfaf0fd1073f7f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719425"
---
# <span data-ttu-id="73034-101">Get-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="73034-101">Get-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="73034-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73034-102">SYNOPSIS</span></span>
<span data-ttu-id="73034-103">Pobiera właściwości jednego lub kilku aplikacji centralnych IoT.</span><span class="sxs-lookup"><span data-stu-id="73034-103">Gets properties for either one or several IoT Central Applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73034-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73034-104">SYNTAX</span></span>

### <span data-ttu-id="73034-105">ListIotCentralAppsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73034-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzureRmIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73034-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="73034-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzureRmIotCentralApp [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73034-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73034-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73034-108">Opis</span><span class="sxs-lookup"><span data-stu-id="73034-108">DESCRIPTION</span></span>
<span data-ttu-id="73034-109">Pobiera metadane dla konkretnej aplikacji centralnej usługi IoT albo wszystkie aplikacje w grupie zasobów lub subskrypcji, w zależności od zestawu parametrów.</span><span class="sxs-lookup"><span data-stu-id="73034-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="73034-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73034-110">EXAMPLES</span></span>

### <span data-ttu-id="73034-111">Przykład 1 Pobierz określoną aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="73034-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="73034-112">Pobiera metadane określonej aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="73034-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="73034-113">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="73034-113">Example Output:</span></span>

<span data-ttu-id="73034-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-xxxxxxxxxxxx DisplayName: Moja niestandardowa nazwa wyświetlana: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73034-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="73034-115">Przykład 2 Uzyskaj w ramach abonamentu aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="73034-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp
```

<span data-ttu-id="73034-116">Pobiera metadane wszystkich aplikacji centralnych IoT w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="73034-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="73034-117">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="73034-117">Example Output:</span></span>

<span data-ttu-id="73034-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-xxxxxxxxxxxx DisplayName: Moja niestandardowa nazwa wyświetlana: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73034-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="73034-119">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2: typ MyAppResourceName2: Microsoft. IoTCentral/IoTApps Location: tag zachód: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. MODELES. PSIotCentralAppSkuInfo: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Moja niestandardowa nazwa wyświetlana 2 poddomena: MyAppSubdomain2: iotc-default@1.0.0 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73034-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="73034-120">Przykład 3 Uzyskaj aplikacje centralne programu IoT w grupie zasób.</span><span class="sxs-lookup"><span data-stu-id="73034-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="73034-121">Pobiera metadane wszystkich aplikacji centralnych IoT w podanej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="73034-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="73034-122">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="73034-122">Example Output:</span></span>

<span data-ttu-id="73034-123">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-xxxxxxxxxxxx DisplayName: Moja niestandardowa nazwa wyświetlana: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73034-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="73034-124">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2: typ MyAppResourceName2: Microsoft. IoTCentral/IoTApps Location: tag zachód: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. MODELES. PSIotCentralAppSkuInfo: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Moja niestandardowa nazwa wyświetlana 2 poddomena: MyAppSubdomain2: iotc-default@1.0.0 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73034-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="73034-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73034-125">PARAMETERS</span></span>

### <span data-ttu-id="73034-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73034-126">-DefaultProfile</span></span>
<span data-ttu-id="73034-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73034-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73034-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73034-128">-Name</span></span>
<span data-ttu-id="73034-129">Nazwa zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="73034-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73034-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73034-130">-ResourceGroupName</span></span>
<span data-ttu-id="73034-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73034-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73034-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73034-132">-ResourceId</span></span>
<span data-ttu-id="73034-133">Identyfikator zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="73034-133">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73034-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73034-134">CommonParameters</span></span>
<span data-ttu-id="73034-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73034-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73034-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73034-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73034-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73034-137">INPUTS</span></span>

### <span data-ttu-id="73034-138">System. String</span><span class="sxs-lookup"><span data-stu-id="73034-138">System.String</span></span>
## <span data-ttu-id="73034-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73034-139">OUTPUTS</span></span>

### <span data-ttu-id="73034-140">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="73034-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="73034-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73034-141">NOTES</span></span>

## <span data-ttu-id="73034-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73034-142">RELATED LINKS</span></span>
