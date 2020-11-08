---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8a81df2081420f8d218e094ff43f22e8dd9cc5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222577"
---
# <span data-ttu-id="44ff3-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="44ff3-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="44ff3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="44ff3-103">Aktualizowanie rekordu rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="44ff3-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="44ff3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44ff3-104">SYNTAX</span></span>

### <span data-ttu-id="44ff3-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="44ff3-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44ff3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44ff3-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44ff3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="44ff3-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44ff3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="44ff3-108">DESCRIPTION</span></span>
<span data-ttu-id="44ff3-109">Aktualizowanie rejestracji urządzenia w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="44ff3-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="44ff3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44ff3-110">EXAMPLES</span></span>

### <span data-ttu-id="44ff3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44ff3-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="44ff3-112">Aktualizowanie zasad alokacji i koncentratorów dla rekordu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="44ff3-112">Update allocation policy and hubs for an enrollment record.</span></span>

## <span data-ttu-id="44ff3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44ff3-113">PARAMETERS</span></span>

### <span data-ttu-id="44ff3-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="44ff3-114">-AllocationPolicy</span></span>
<span data-ttu-id="44ff3-115">Typ alokacji urządzenia przypisanego do koncentratora.</span><span class="sxs-lookup"><span data-stu-id="44ff3-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="44ff3-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="44ff3-116">-ApiVersion</span></span>
<span data-ttu-id="44ff3-117">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="44ff3-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="44ff3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ff3-118">-DefaultProfile</span></span>
<span data-ttu-id="44ff3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44ff3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ff3-120">— Wymagane</span><span class="sxs-lookup"><span data-stu-id="44ff3-120">-Desired</span></span>
<span data-ttu-id="44ff3-121">Początkowe sznurki — wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="44ff3-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="44ff3-122">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="44ff3-122">-DeviceId</span></span>
<span data-ttu-id="44ff3-123">Identyfikator urządzenia Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="44ff3-123">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="44ff3-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="44ff3-124">-DpsName</span></span>
<span data-ttu-id="44ff3-125">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="44ff3-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="44ff3-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="44ff3-126">-DpsObject</span></span>
<span data-ttu-id="44ff3-127">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="44ff3-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="44ff3-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="44ff3-128">-EdgeEnabled</span></span>
<span data-ttu-id="44ff3-129">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="44ff3-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="44ff3-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="44ff3-130">-IotHub</span></span>
<span data-ttu-id="44ff3-131">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="44ff3-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="44ff3-132">Użyj listy rozdzielanej spacjami dla wielu koncentratorów IoT.</span><span class="sxs-lookup"><span data-stu-id="44ff3-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="44ff3-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="44ff3-133">-IotHubHostName</span></span>
<span data-ttu-id="44ff3-134">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="44ff3-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="44ff3-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="44ff3-135">-ProvisioningStatus</span></span>
<span data-ttu-id="44ff3-136">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="44ff3-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="44ff3-137">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="44ff3-137">-RegistrationId</span></span>
<span data-ttu-id="44ff3-138">Indywidualny Identyfikator rejestracji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="44ff3-138">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="44ff3-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="44ff3-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="44ff3-140">Dane urządzenia, które mają być obsługiwane na ponownym zaopatrzeniu w inne Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="44ff3-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="44ff3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ff3-141">-ResourceGroupName</span></span>
<span data-ttu-id="44ff3-142">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="44ff3-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="44ff3-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44ff3-143">-ResourceId</span></span>
<span data-ttu-id="44ff3-144">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="44ff3-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="44ff3-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="44ff3-145">-Tag</span></span>
<span data-ttu-id="44ff3-146">Początkowe znaczniki sznurka.</span><span class="sxs-lookup"><span data-stu-id="44ff3-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="44ff3-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="44ff3-147">-WebhookUrl</span></span>
<span data-ttu-id="44ff3-148">Adres URL elementu webhook służący do niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="44ff3-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="44ff3-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44ff3-149">-Confirm</span></span>
<span data-ttu-id="44ff3-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44ff3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44ff3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44ff3-151">-WhatIf</span></span>
<span data-ttu-id="44ff3-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44ff3-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44ff3-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="44ff3-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44ff3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ff3-154">CommonParameters</span></span>
<span data-ttu-id="44ff3-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44ff3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ff3-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ff3-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ff3-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44ff3-157">INPUTS</span></span>

### <span data-ttu-id="44ff3-158">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="44ff3-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="44ff3-159">System. String</span><span class="sxs-lookup"><span data-stu-id="44ff3-159">System.String</span></span>

## <span data-ttu-id="44ff3-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44ff3-160">OUTPUTS</span></span>

### <span data-ttu-id="44ff3-161">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="44ff3-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="44ff3-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44ff3-162">NOTES</span></span>

## <span data-ttu-id="44ff3-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44ff3-163">RELATED LINKS</span></span>
