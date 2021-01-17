---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376929"
---
# <span data-ttu-id="49bd8-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="49bd8-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="49bd8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="49bd8-103">Aktualizowanie rekordu rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="49bd8-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="49bd8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49bd8-104">SYNTAX</span></span>

### <span data-ttu-id="49bd8-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49bd8-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49bd8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="49bd8-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49bd8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="49bd8-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49bd8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="49bd8-108">DESCRIPTION</span></span>
<span data-ttu-id="49bd8-109">Aktualizowanie rejestracji urządzenia w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="49bd8-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="49bd8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49bd8-110">EXAMPLES</span></span>

### <span data-ttu-id="49bd8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49bd8-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="49bd8-112">Aktualizowanie zasad alokacji i koncentratorów dla rekordu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="49bd8-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="49bd8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="49bd8-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="49bd8-114">Aktualizowanie początkowego stanu rejestracji sznurka.</span><span class="sxs-lookup"><span data-stu-id="49bd8-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="49bd8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49bd8-115">PARAMETERS</span></span>

### <span data-ttu-id="49bd8-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="49bd8-116">-AllocationPolicy</span></span>
<span data-ttu-id="49bd8-117">Typ alokacji urządzenia przypisanego do koncentratora.</span><span class="sxs-lookup"><span data-stu-id="49bd8-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="49bd8-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="49bd8-118">-ApiVersion</span></span>
<span data-ttu-id="49bd8-119">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="49bd8-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="49bd8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49bd8-120">-DefaultProfile</span></span>
<span data-ttu-id="49bd8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49bd8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49bd8-122">— Wymagane</span><span class="sxs-lookup"><span data-stu-id="49bd8-122">-Desired</span></span>
<span data-ttu-id="49bd8-123">Początkowe sznurki — wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="49bd8-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="49bd8-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="49bd8-124">-DeviceId</span></span>
<span data-ttu-id="49bd8-125">Identyfikator urządzenia Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="49bd8-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="49bd8-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="49bd8-126">-DpsName</span></span>
<span data-ttu-id="49bd8-127">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="49bd8-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="49bd8-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="49bd8-128">-DpsObject</span></span>
<span data-ttu-id="49bd8-129">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="49bd8-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="49bd8-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="49bd8-130">-EdgeEnabled</span></span>
<span data-ttu-id="49bd8-131">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="49bd8-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="49bd8-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="49bd8-132">-IotHub</span></span>
<span data-ttu-id="49bd8-133">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="49bd8-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="49bd8-134">Użyj listy rozdzielanej spacjami dla wielu koncentratorów IoT.</span><span class="sxs-lookup"><span data-stu-id="49bd8-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="49bd8-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="49bd8-135">-IotHubHostName</span></span>
<span data-ttu-id="49bd8-136">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="49bd8-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="49bd8-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="49bd8-137">-ProvisioningStatus</span></span>
<span data-ttu-id="49bd8-138">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="49bd8-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="49bd8-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="49bd8-139">-RegistrationId</span></span>
<span data-ttu-id="49bd8-140">Indywidualny Identyfikator rejestracji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="49bd8-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="49bd8-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="49bd8-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="49bd8-142">Dane urządzenia, które mają być obsługiwane na ponownym zaopatrzeniu w inne Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="49bd8-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="49bd8-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49bd8-143">-ResourceGroupName</span></span>
<span data-ttu-id="49bd8-144">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="49bd8-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="49bd8-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49bd8-145">-ResourceId</span></span>
<span data-ttu-id="49bd8-146">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="49bd8-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="49bd8-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="49bd8-147">-Tag</span></span>
<span data-ttu-id="49bd8-148">Początkowe znaczniki sznurka.</span><span class="sxs-lookup"><span data-stu-id="49bd8-148">Initial twin tags.</span></span>

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

### <span data-ttu-id="49bd8-149">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="49bd8-149">-WebhookUrl</span></span>
<span data-ttu-id="49bd8-150">Adres URL elementu webhook służący do niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="49bd8-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="49bd8-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49bd8-151">-Confirm</span></span>
<span data-ttu-id="49bd8-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49bd8-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49bd8-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49bd8-153">-WhatIf</span></span>
<span data-ttu-id="49bd8-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49bd8-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49bd8-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49bd8-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49bd8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49bd8-156">CommonParameters</span></span>
<span data-ttu-id="49bd8-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49bd8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49bd8-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49bd8-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49bd8-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49bd8-159">INPUTS</span></span>

### <span data-ttu-id="49bd8-160">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="49bd8-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="49bd8-161">System. String</span><span class="sxs-lookup"><span data-stu-id="49bd8-161">System.String</span></span>

## <span data-ttu-id="49bd8-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49bd8-162">OUTPUTS</span></span>

### <span data-ttu-id="49bd8-163">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="49bd8-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="49bd8-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49bd8-164">NOTES</span></span>

## <span data-ttu-id="49bd8-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49bd8-165">RELATED LINKS</span></span>
