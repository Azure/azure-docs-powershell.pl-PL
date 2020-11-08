---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062763"
---
# <span data-ttu-id="3bbd0-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="3bbd0-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="3bbd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bbd0-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbd0-103">Aktualizowanie grupy rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="3bbd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bbd0-104">SYNTAX</span></span>

### <span data-ttu-id="3bbd0-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3bbd0-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bbd0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3bbd0-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bbd0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3bbd0-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bbd0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3bbd0-108">DESCRIPTION</span></span>
<span data-ttu-id="3bbd0-109">Aktualizowanie grupy rejestracji w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="3bbd0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bbd0-110">EXAMPLES</span></span>

### <span data-ttu-id="3bbd0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3bbd0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="3bbd0-112">Aktualizowanie zasad alokacji i koncentratorów dla grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="3bbd0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bbd0-113">PARAMETERS</span></span>

### <span data-ttu-id="3bbd0-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3bbd0-114">-AllocationPolicy</span></span>
<span data-ttu-id="3bbd0-115">Typ alokacji urządzenia przypisanego do koncentratora.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-115">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd0-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3bbd0-116">-ApiVersion</span></span>
<span data-ttu-id="3bbd0-117">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="3bbd0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bbd0-118">-DefaultProfile</span></span>
<span data-ttu-id="3bbd0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bbd0-120">— Wymagane</span><span class="sxs-lookup"><span data-stu-id="3bbd0-120">-Desired</span></span>
<span data-ttu-id="3bbd0-121">Początkowe sznurki — wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="3bbd0-122">-DpsName</span><span class="sxs-lookup"><span data-stu-id="3bbd0-122">-DpsName</span></span>
<span data-ttu-id="3bbd0-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3bbd0-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3bbd0-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="3bbd0-124">-DpsObject</span></span>
<span data-ttu-id="3bbd0-125">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3bbd0-125">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd0-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="3bbd0-126">-EdgeEnabled</span></span>
<span data-ttu-id="3bbd0-127">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-127">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd0-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="3bbd0-128">-IotHub</span></span>
<span data-ttu-id="3bbd0-129">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="3bbd0-130">Użyj listy rozdzielanej spacjami dla wielu koncentratorów IoT.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-130">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd0-131">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="3bbd0-131">-IotHubHostName</span></span>
<span data-ttu-id="3bbd0-132">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="3bbd0-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3bbd0-133">-Name</span></span>
<span data-ttu-id="3bbd0-134">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-134">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="3bbd0-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="3bbd0-135">-ProvisioningStatus</span></span>
<span data-ttu-id="3bbd0-136">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-136">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd0-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="3bbd0-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="3bbd0-138">Dane urządzenia, które mają być obsługiwane na ponownym zaopatrzeniu w inne Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbd0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bbd0-139">-ResourceGroupName</span></span>
<span data-ttu-id="3bbd0-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3bbd0-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3bbd0-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bbd0-141">-ResourceId</span></span>
<span data-ttu-id="3bbd0-142">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3bbd0-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3bbd0-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="3bbd0-143">-Tag</span></span>
<span data-ttu-id="3bbd0-144">Początkowe znaczniki sznurka.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="3bbd0-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="3bbd0-145">-WebhookUrl</span></span>
<span data-ttu-id="3bbd0-146">Adres URL elementu webhook służący do niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="3bbd0-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3bbd0-147">-Confirm</span></span>
<span data-ttu-id="3bbd0-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bbd0-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bbd0-149">-WhatIf</span></span>
<span data-ttu-id="3bbd0-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bbd0-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bbd0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbd0-152">CommonParameters</span></span>
<span data-ttu-id="3bbd0-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bbd0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbd0-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bbd0-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbd0-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bbd0-155">INPUTS</span></span>

### <span data-ttu-id="3bbd0-156">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3bbd0-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="3bbd0-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3bbd0-157">System.String</span></span>

## <span data-ttu-id="3bbd0-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bbd0-158">OUTPUTS</span></span>

### <span data-ttu-id="3bbd0-159">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="3bbd0-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="3bbd0-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bbd0-160">NOTES</span></span>

## <span data-ttu-id="3bbd0-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bbd0-161">RELATED LINKS</span></span>
