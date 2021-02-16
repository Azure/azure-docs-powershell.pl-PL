---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194475"
---
# <span data-ttu-id="44423-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="44423-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="44423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44423-102">SYNOPSIS</span></span>
<span data-ttu-id="44423-103">Zaktualizuj grupę rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="44423-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="44423-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="44423-104">SYNTAX</span></span>

### <span data-ttu-id="44423-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="44423-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44423-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44423-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44423-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="44423-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44423-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="44423-108">DESCRIPTION</span></span>
<span data-ttu-id="44423-109">Zaktualizuj grupę rejestracji w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="44423-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="44423-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="44423-110">EXAMPLES</span></span>

### <span data-ttu-id="44423-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44423-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="44423-112">Zaktualizuj zasady i centra alokacji dla grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="44423-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="44423-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="44423-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="44423-114">Zaktualizuj początkowy stan rejestracji grupy.</span><span class="sxs-lookup"><span data-stu-id="44423-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="44423-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44423-115">PARAMETERS</span></span>

### <span data-ttu-id="44423-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="44423-116">-AllocationPolicy</span></span>
<span data-ttu-id="44423-117">Typ alokacji dla urządzenia przypisanego do Centrum.</span><span class="sxs-lookup"><span data-stu-id="44423-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="44423-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="44423-118">-ApiVersion</span></span>
<span data-ttu-id="44423-119">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="44423-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="44423-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44423-120">-DefaultProfile</span></span>
<span data-ttu-id="44423-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="44423-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44423-122">— Żądane</span><span class="sxs-lookup"><span data-stu-id="44423-122">-Desired</span></span>
<span data-ttu-id="44423-123">Początkowe żądane właściwości.</span><span class="sxs-lookup"><span data-stu-id="44423-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="44423-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="44423-124">-DpsName</span></span>
<span data-ttu-id="44423-125">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="44423-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="44423-126">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="44423-126">-DpsObject</span></span>
<span data-ttu-id="44423-127">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="44423-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="44423-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="44423-128">-EdgeEnabled</span></span>
<span data-ttu-id="44423-129">Flaga wskazująca włączenie krawędzi.</span><span class="sxs-lookup"><span data-stu-id="44423-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="44423-130">- IotHub</span><span class="sxs-lookup"><span data-stu-id="44423-130">-IotHub</span></span>
<span data-ttu-id="44423-131">Nazwa hosta docelowego centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="44423-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="44423-132">W przypadku wielu centrum IoT użyj listy rozdzielonych spacjami.</span><span class="sxs-lookup"><span data-stu-id="44423-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="44423-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="44423-133">-IotHubHostName</span></span>
<span data-ttu-id="44423-134">Host name of the target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="44423-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="44423-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="44423-135">-Name</span></span>
<span data-ttu-id="44423-136">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="44423-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="44423-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="44423-137">-ProvisioningStatus</span></span>
<span data-ttu-id="44423-138">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="44423-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="44423-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="44423-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="44423-140">Dane urządzenia do obsługi przy ponownej obsłudze administracyjnej do innego centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="44423-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="44423-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44423-141">-ResourceGroupName</span></span>
<span data-ttu-id="44423-142">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="44423-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="44423-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44423-143">-ResourceId</span></span>
<span data-ttu-id="44423-144">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="44423-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="44423-145">— Tag</span><span class="sxs-lookup"><span data-stu-id="44423-145">-Tag</span></span>
<span data-ttu-id="44423-146">Początkowe tagi tagi tagów.</span><span class="sxs-lookup"><span data-stu-id="44423-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="44423-147">- WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="44423-147">-WebhookUrl</span></span>
<span data-ttu-id="44423-148">Adres URL webhook używany dla niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="44423-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="44423-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44423-149">-Confirm</span></span>
<span data-ttu-id="44423-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44423-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44423-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44423-151">-WhatIf</span></span>
<span data-ttu-id="44423-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44423-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44423-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="44423-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44423-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44423-154">CommonParameters</span></span>
<span data-ttu-id="44423-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44423-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44423-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44423-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44423-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44423-157">INPUTS</span></span>

### <span data-ttu-id="44423-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="44423-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="44423-159">System.String</span><span class="sxs-lookup"><span data-stu-id="44423-159">System.String</span></span>

## <span data-ttu-id="44423-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44423-160">OUTPUTS</span></span>

### <span data-ttu-id="44423-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="44423-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="44423-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="44423-162">NOTES</span></span>

## <span data-ttu-id="44423-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44423-163">RELATED LINKS</span></span>
