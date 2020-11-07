---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 78fdf68ecb8c50d0eebf4611b51a2fad14c66e5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705273"
---
# <span data-ttu-id="7f678-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7f678-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="7f678-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f678-102">SYNOPSIS</span></span>
<span data-ttu-id="7f678-103">Aktualizuje metadane aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="7f678-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="7f678-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f678-104">SYNTAX</span></span>

### <span data-ttu-id="7f678-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7f678-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f678-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f678-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f678-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f678-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f678-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7f678-108">DESCRIPTION</span></span>
<span data-ttu-id="7f678-109">Zaktualizuj metadane dla aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="7f678-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="7f678-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f678-110">EXAMPLES</span></span>

### <span data-ttu-id="7f678-111">Przykład 1 aktualizacja nazwa wyświetlana</span><span class="sxs-lookup"><span data-stu-id="7f678-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="7f678-112">Zaktualizuj nazwę wyświetlaną w istniejącej aplikacji do centralnego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="7f678-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="7f678-113">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="7f678-113">Example Output:</span></span>

<span data-ttu-id="7f678-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Nowa niestandardowa nazwa wyświetlana: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f678-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="7f678-115">Przykład 2 Aktualizacja poddomeny</span><span class="sxs-lookup"><span data-stu-id="7f678-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="7f678-116">Zaktualizuj nazwę wyświetlaną w istniejącej aplikacji do centralnego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="7f678-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="7f678-117">Przykładowe dane wyjściowe:</span><span class="sxs-lookup"><span data-stu-id="7f678-117">Example Output:</span></span>

<span data-ttu-id="7f678-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: SKU: Microsoft. Azure. Commands. IoTCentral. modele. PSIotCentralAppSkuInfo, identyfikator: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx DisplayName: "Display Name subdomain": szablon: iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="7f678-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="7f678-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f678-119">PARAMETERS</span></span>

### <span data-ttu-id="7f678-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f678-120">-AsJob</span></span>
<span data-ttu-id="7f678-121">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="7f678-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="7f678-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f678-122">-DefaultProfile</span></span>
<span data-ttu-id="7f678-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f678-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f678-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7f678-124">-DisplayName</span></span>
<span data-ttu-id="7f678-125">Niestandardowa nazwa wyświetlana aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="7f678-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="7f678-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f678-126">-InputObject</span></span>
<span data-ttu-id="7f678-127">Obiekt wejściowy aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="7f678-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="7f678-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f678-128">-Name</span></span>
<span data-ttu-id="7f678-129">Nazwa zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="7f678-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="7f678-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f678-130">-ResourceGroupName</span></span>
<span data-ttu-id="7f678-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f678-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="7f678-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f678-132">-ResourceId</span></span>
<span data-ttu-id="7f678-133">Identyfikator zasobu aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="7f678-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="7f678-134">-Poddomena</span><span class="sxs-lookup"><span data-stu-id="7f678-134">-Subdomain</span></span>
<span data-ttu-id="7f678-135">Poddomena aplikacji Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="7f678-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="7f678-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f678-136">-Tag</span></span>
<span data-ttu-id="7f678-137">Znaczniki zasobów aplikacji centralnej IoT.</span><span class="sxs-lookup"><span data-stu-id="7f678-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="7f678-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f678-138">-Confirm</span></span>
<span data-ttu-id="7f678-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f678-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f678-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f678-140">-WhatIf</span></span>
<span data-ttu-id="7f678-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f678-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f678-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f678-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f678-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f678-143">CommonParameters</span></span>
<span data-ttu-id="7f678-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f678-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f678-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f678-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f678-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f678-146">INPUTS</span></span>

### <span data-ttu-id="7f678-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7f678-147">System.String</span></span>

### <span data-ttu-id="7f678-148">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7f678-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="7f678-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f678-149">OUTPUTS</span></span>

### <span data-ttu-id="7f678-150">Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7f678-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="7f678-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f678-151">NOTES</span></span>

## <span data-ttu-id="7f678-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f678-152">RELATED LINKS</span></span>
