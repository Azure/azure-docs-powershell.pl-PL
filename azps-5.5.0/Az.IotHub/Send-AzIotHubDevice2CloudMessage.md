---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192411"
---
# <span data-ttu-id="f242b-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="f242b-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="f242b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f242b-102">SYNOPSIS</span></span>
<span data-ttu-id="f242b-103">Wysyłanie wiadomości z urządzenia do chmury.</span><span class="sxs-lookup"><span data-stu-id="f242b-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="f242b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f242b-104">SYNTAX</span></span>

### <span data-ttu-id="f242b-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="f242b-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f242b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f242b-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f242b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f242b-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f242b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f242b-108">DESCRIPTION</span></span>
<span data-ttu-id="f242b-109">To polecenie obsługuje wysyłanie wiadomości z właściwościami aplikacji i systemu.</span><span class="sxs-lookup"><span data-stu-id="f242b-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="f242b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f242b-110">EXAMPLES</span></span>

### <span data-ttu-id="f242b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f242b-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="f242b-112">Wysyłanie wiadomości urządzenia do chmury przy użyciu domyślnego typu transportu.</span><span class="sxs-lookup"><span data-stu-id="f242b-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="f242b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f242b-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="f242b-114">Wysyłanie wiadomości z urządzenia mqtt do chmury.</span><span class="sxs-lookup"><span data-stu-id="f242b-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="f242b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f242b-115">PARAMETERS</span></span>

### <span data-ttu-id="f242b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f242b-116">-DefaultProfile</span></span>
<span data-ttu-id="f242b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f242b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f242b-118">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="f242b-118">-DeviceId</span></span>
<span data-ttu-id="f242b-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="f242b-119">Target Device Id.</span></span>

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

### <span data-ttu-id="f242b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f242b-120">-InputObject</span></span>
<span data-ttu-id="f242b-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="f242b-121">IotHub object</span></span>

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

### <span data-ttu-id="f242b-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f242b-122">-IotHubName</span></span>
<span data-ttu-id="f242b-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="f242b-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f242b-124">— Wiadomość</span><span class="sxs-lookup"><span data-stu-id="f242b-124">-Message</span></span>
<span data-ttu-id="f242b-125">Treść wiadomości do wysłania do Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="f242b-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="f242b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f242b-126">-PassThru</span></span>
<span data-ttu-id="f242b-127">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="f242b-127">Allows to return the boolean object.</span></span> <span data-ttu-id="f242b-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f242b-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f242b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f242b-129">-ResourceGroupName</span></span>
<span data-ttu-id="f242b-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f242b-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f242b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f242b-131">-ResourceId</span></span>
<span data-ttu-id="f242b-132">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="f242b-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f242b-133">- TransportType</span><span class="sxs-lookup"><span data-stu-id="f242b-133">-TransportType</span></span>
<span data-ttu-id="f242b-134">Typ transportu do użycia.</span><span class="sxs-lookup"><span data-stu-id="f242b-134">Transport type to use.</span></span>
<span data-ttu-id="f242b-135">Wartością domyślną jest Amqp.</span><span class="sxs-lookup"><span data-stu-id="f242b-135">Default is Amqp.</span></span>

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

### <span data-ttu-id="f242b-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f242b-136">-Confirm</span></span>
<span data-ttu-id="f242b-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f242b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f242b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f242b-138">-WhatIf</span></span>
<span data-ttu-id="f242b-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f242b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f242b-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f242b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f242b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f242b-141">CommonParameters</span></span>
<span data-ttu-id="f242b-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f242b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f242b-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f242b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f242b-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f242b-144">INPUTS</span></span>

### <span data-ttu-id="f242b-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f242b-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f242b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f242b-146">System.String</span></span>

## <span data-ttu-id="f242b-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f242b-147">OUTPUTS</span></span>

### <span data-ttu-id="f242b-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f242b-148">System.Boolean</span></span>

## <span data-ttu-id="f242b-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f242b-149">NOTES</span></span>

## <span data-ttu-id="f242b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f242b-150">RELATED LINKS</span></span>
