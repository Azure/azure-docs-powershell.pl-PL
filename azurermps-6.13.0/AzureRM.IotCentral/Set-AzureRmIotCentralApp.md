---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/set-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
ms.openlocfilehash: a9b7dbc962809288979f5293c14fd875081f48bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719424"
---
# <span data-ttu-id="db234-101">Set-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="db234-101">Set-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="db234-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db234-102">SYNOPSIS</span></span>
<span data-ttu-id="db234-103">Aktualizuje metadane aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="db234-103">Updates the metadata for an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db234-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db234-104">SYNTAX</span></span>

### <span data-ttu-id="db234-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="db234-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db234-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db234-106">InputObjectParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db234-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="db234-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db234-108">Opis</span><span class="sxs-lookup"><span data-stu-id="db234-108">DESCRIPTION</span></span>
<span data-ttu-id="db234-109">Zaktualizuj metadane dla aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="db234-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="db234-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db234-110">EXAMPLES</span></span>

### <span data-ttu-id="db234-111">Przykład 1 aktualizacja nazwa wyświetlana</span><span class="sxs-lookup"><span data-stu-id="db234-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="db234-112">Zaktualizuj nazwę wyświetlaną w istniejącej aplikacji do centralnego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="db234-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="db234-113">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="db234-113">Example Output:</span></span>

<span data-ttu-id="db234-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Nowa niestandardowa nazwa wyświetlana: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db234-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="db234-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db234-115">PARAMETERS</span></span>

### <span data-ttu-id="db234-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db234-116">-AsJob</span></span>
<span data-ttu-id="db234-117">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="db234-117">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db234-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db234-118">-DefaultProfile</span></span>
<span data-ttu-id="db234-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db234-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db234-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db234-120">-DisplayName</span></span>
<span data-ttu-id="db234-121">Niestandardowa nazwa wyświetlana aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="db234-121">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db234-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="db234-122">-InputObject</span></span>
<span data-ttu-id="db234-123">Obiekt wejściowy aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="db234-123">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db234-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db234-124">-Name</span></span>
<span data-ttu-id="db234-125">Nazwa zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="db234-125">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="db234-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db234-126">-ResourceGroupName</span></span>
<span data-ttu-id="db234-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="db234-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="db234-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db234-128">-ResourceId</span></span>
<span data-ttu-id="db234-129">Identyfikator zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="db234-129">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="db234-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="db234-130">-Tag</span></span>
<span data-ttu-id="db234-131">Znaczniki zasobów aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="db234-131">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db234-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="db234-132">-Confirm</span></span>
<span data-ttu-id="db234-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db234-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db234-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db234-134">-WhatIf</span></span>
<span data-ttu-id="db234-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db234-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db234-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="db234-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db234-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db234-137">CommonParameters</span></span>
<span data-ttu-id="db234-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db234-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db234-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db234-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db234-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db234-140">INPUTS</span></span>

### <span data-ttu-id="db234-141">System. String</span><span class="sxs-lookup"><span data-stu-id="db234-141">System.String</span></span>
### <span data-ttu-id="db234-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="db234-142">System.Collections.Hashtable</span></span>
### <span data-ttu-id="db234-143">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="db234-143">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="db234-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db234-144">OUTPUTS</span></span>

### <span data-ttu-id="db234-145">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="db234-145">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="db234-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db234-146">NOTES</span></span>

## <span data-ttu-id="db234-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db234-147">RELATED LINKS</span></span>
