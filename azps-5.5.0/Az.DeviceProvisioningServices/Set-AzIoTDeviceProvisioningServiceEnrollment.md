---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194490"
---
# <span data-ttu-id="22357-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="22357-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="22357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22357-102">SYNOPSIS</span></span>
<span data-ttu-id="22357-103">Aktualizowanie rekordu rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="22357-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="22357-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="22357-104">SYNTAX</span></span>

### <span data-ttu-id="22357-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22357-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22357-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="22357-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22357-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="22357-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22357-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="22357-108">DESCRIPTION</span></span>
<span data-ttu-id="22357-109">Zaktualizuj rejestrację urządzenia w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="22357-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="22357-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="22357-110">EXAMPLES</span></span>

### <span data-ttu-id="22357-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22357-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="22357-112">Zaktualizuj zasady i koncentratory alokacji dla rekordu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="22357-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="22357-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="22357-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="22357-114">Zaktualizuj początkowy stan rejestracji.</span><span class="sxs-lookup"><span data-stu-id="22357-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="22357-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22357-115">PARAMETERS</span></span>

### <span data-ttu-id="22357-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="22357-116">-AllocationPolicy</span></span>
<span data-ttu-id="22357-117">Typ alokacji dla urządzenia przypisanego do Centrum.</span><span class="sxs-lookup"><span data-stu-id="22357-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="22357-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22357-118">-ApiVersion</span></span>
<span data-ttu-id="22357-119">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="22357-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="22357-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22357-120">-DefaultProfile</span></span>
<span data-ttu-id="22357-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="22357-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22357-122">— Żądane</span><span class="sxs-lookup"><span data-stu-id="22357-122">-Desired</span></span>
<span data-ttu-id="22357-123">Początkowe żądane właściwości.</span><span class="sxs-lookup"><span data-stu-id="22357-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="22357-124">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="22357-124">-DeviceId</span></span>
<span data-ttu-id="22357-125">Identyfikator urządzenia centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="22357-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="22357-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="22357-126">-DpsName</span></span>
<span data-ttu-id="22357-127">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="22357-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="22357-128">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="22357-128">-DpsObject</span></span>
<span data-ttu-id="22357-129">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="22357-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="22357-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="22357-130">-EdgeEnabled</span></span>
<span data-ttu-id="22357-131">Flaga wskazująca włączenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="22357-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="22357-132">- IotHub</span><span class="sxs-lookup"><span data-stu-id="22357-132">-IotHub</span></span>
<span data-ttu-id="22357-133">Nazwa hosta docelowego centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="22357-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="22357-134">W przypadku wielu centrum IoT użyj listy rozdzielonych spacjami.</span><span class="sxs-lookup"><span data-stu-id="22357-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="22357-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="22357-135">-IotHubHostName</span></span>
<span data-ttu-id="22357-136">Host name of the target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="22357-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="22357-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="22357-137">-ProvisioningStatus</span></span>
<span data-ttu-id="22357-138">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="22357-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="22357-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="22357-139">-RegistrationId</span></span>
<span data-ttu-id="22357-140">Identyfikator rejestracji indywidualnej.</span><span class="sxs-lookup"><span data-stu-id="22357-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="22357-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="22357-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="22357-142">Dane urządzenia do obsługi przy ponownej obsłudze administracyjnej do innego centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="22357-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="22357-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22357-143">-ResourceGroupName</span></span>
<span data-ttu-id="22357-144">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="22357-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="22357-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22357-145">-ResourceId</span></span>
<span data-ttu-id="22357-146">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="22357-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="22357-147">— Tag</span><span class="sxs-lookup"><span data-stu-id="22357-147">-Tag</span></span>
<span data-ttu-id="22357-148">Początkowe tagi tagi tagów.</span><span class="sxs-lookup"><span data-stu-id="22357-148">Initial twin tags.</span></span>

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

### <span data-ttu-id="22357-149">- WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="22357-149">-WebhookUrl</span></span>
<span data-ttu-id="22357-150">Adres URL webhook używany dla niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="22357-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="22357-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22357-151">-Confirm</span></span>
<span data-ttu-id="22357-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="22357-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22357-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22357-153">-WhatIf</span></span>
<span data-ttu-id="22357-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22357-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22357-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="22357-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22357-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22357-156">CommonParameters</span></span>
<span data-ttu-id="22357-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22357-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22357-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22357-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22357-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22357-159">INPUTS</span></span>

### <span data-ttu-id="22357-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="22357-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="22357-161">System.String</span><span class="sxs-lookup"><span data-stu-id="22357-161">System.String</span></span>

## <span data-ttu-id="22357-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22357-162">OUTPUTS</span></span>

### <span data-ttu-id="22357-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="22357-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="22357-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="22357-164">NOTES</span></span>

## <span data-ttu-id="22357-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22357-165">RELATED LINKS</span></span>
