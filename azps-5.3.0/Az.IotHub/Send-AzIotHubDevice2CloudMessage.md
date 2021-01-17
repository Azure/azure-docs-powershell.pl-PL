---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386612"
---
# <span data-ttu-id="2d4ce-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="2d4ce-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="2d4ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4ce-103">Wyślij wiadomość od urządzenia do chmury.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="2d4ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d4ce-104">SYNTAX</span></span>

### <span data-ttu-id="2d4ce-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2d4ce-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d4ce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2d4ce-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d4ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2d4ce-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d4ce-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2d4ce-108">DESCRIPTION</span></span>
<span data-ttu-id="2d4ce-109">Polecenie obsługuje wysyłanie wiadomości przy użyciu właściwości aplikacji i systemu.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="2d4ce-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d4ce-110">EXAMPLES</span></span>

### <span data-ttu-id="2d4ce-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d4ce-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="2d4ce-112">Wysyłanie urządzenia do wiadomości w chmurze przy użyciu domyślnego typu transportu.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="2d4ce-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2d4ce-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="2d4ce-114">Wysyłanie do wiadomości w chmurze urządzenia MQTT.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="2d4ce-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d4ce-115">PARAMETERS</span></span>

### <span data-ttu-id="2d4ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4ce-116">-DefaultProfile</span></span>
<span data-ttu-id="2d4ce-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d4ce-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2d4ce-118">-DeviceId</span></span>
<span data-ttu-id="2d4ce-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ce-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2d4ce-120">-InputObject</span></span>
<span data-ttu-id="2d4ce-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="2d4ce-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ce-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2d4ce-122">-IotHubName</span></span>
<span data-ttu-id="2d4ce-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="2d4ce-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ce-124">-Message</span><span class="sxs-lookup"><span data-stu-id="2d4ce-124">-Message</span></span>
<span data-ttu-id="2d4ce-125">Treść wiadomości do wysłania do centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-125">Message body to send to IoT Hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ce-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d4ce-126">-PassThru</span></span>
<span data-ttu-id="2d4ce-127">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-127">Allows to return the boolean object.</span></span> <span data-ttu-id="2d4ce-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d4ce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d4ce-129">-ResourceGroupName</span></span>
<span data-ttu-id="2d4ce-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2d4ce-130">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ce-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d4ce-131">-ResourceId</span></span>
<span data-ttu-id="2d4ce-132">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="2d4ce-132">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ce-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="2d4ce-133">-TransportType</span></span>
<span data-ttu-id="2d4ce-134">Typ transportu do użycia.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-134">Transport type to use.</span></span>
<span data-ttu-id="2d4ce-135">Domyślna to AMQP.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-135">Default is Amqp.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ce-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d4ce-136">-Confirm</span></span>
<span data-ttu-id="2d4ce-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d4ce-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4ce-138">-WhatIf</span></span>
<span data-ttu-id="2d4ce-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d4ce-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d4ce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4ce-141">CommonParameters</span></span>
<span data-ttu-id="2d4ce-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4ce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4ce-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4ce-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4ce-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d4ce-144">INPUTS</span></span>

### <span data-ttu-id="2d4ce-145">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2d4ce-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2d4ce-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2d4ce-146">System.String</span></span>

## <span data-ttu-id="2d4ce-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d4ce-147">OUTPUTS</span></span>

### <span data-ttu-id="2d4ce-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d4ce-148">System.Boolean</span></span>

## <span data-ttu-id="2d4ce-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d4ce-149">NOTES</span></span>

## <span data-ttu-id="2d4ce-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d4ce-150">RELATED LINKS</span></span>
