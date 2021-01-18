---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499149"
---
# <span data-ttu-id="9263a-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="9263a-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="9263a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9263a-102">SYNOPSIS</span></span>
<span data-ttu-id="9263a-103">Aktualizowanie grupy rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="9263a-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="9263a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9263a-104">SYNTAX</span></span>

### <span data-ttu-id="9263a-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9263a-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9263a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9263a-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9263a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9263a-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9263a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9263a-108">DESCRIPTION</span></span>
<span data-ttu-id="9263a-109">Aktualizowanie grupy rejestracji w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="9263a-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="9263a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9263a-110">EXAMPLES</span></span>

### <span data-ttu-id="9263a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9263a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="9263a-112">Aktualizowanie zasad alokacji i koncentratorów dla grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="9263a-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="9263a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9263a-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="9263a-114">Zaktualizuj początkowy stan grupy rejestracyjnej z sznurem.</span><span class="sxs-lookup"><span data-stu-id="9263a-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="9263a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9263a-115">PARAMETERS</span></span>

### <span data-ttu-id="9263a-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="9263a-116">-AllocationPolicy</span></span>
<span data-ttu-id="9263a-117">Typ alokacji urządzenia przypisanego do koncentratora.</span><span class="sxs-lookup"><span data-stu-id="9263a-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="9263a-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9263a-118">-ApiVersion</span></span>
<span data-ttu-id="9263a-119">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="9263a-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="9263a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9263a-120">-DefaultProfile</span></span>
<span data-ttu-id="9263a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9263a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9263a-122">— Wymagane</span><span class="sxs-lookup"><span data-stu-id="9263a-122">-Desired</span></span>
<span data-ttu-id="9263a-123">Początkowe sznurki — wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="9263a-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="9263a-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="9263a-124">-DpsName</span></span>
<span data-ttu-id="9263a-125">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="9263a-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9263a-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="9263a-126">-DpsObject</span></span>
<span data-ttu-id="9263a-127">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="9263a-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9263a-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9263a-128">-EdgeEnabled</span></span>
<span data-ttu-id="9263a-129">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="9263a-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="9263a-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="9263a-130">-IotHub</span></span>
<span data-ttu-id="9263a-131">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="9263a-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="9263a-132">Użyj listy rozdzielanej spacjami dla wielu koncentratorów IoT.</span><span class="sxs-lookup"><span data-stu-id="9263a-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="9263a-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="9263a-133">-IotHubHostName</span></span>
<span data-ttu-id="9263a-134">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="9263a-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="9263a-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9263a-135">-Name</span></span>
<span data-ttu-id="9263a-136">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="9263a-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="9263a-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="9263a-137">-ProvisioningStatus</span></span>
<span data-ttu-id="9263a-138">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="9263a-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="9263a-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="9263a-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="9263a-140">Dane urządzenia, które mają być obsługiwane na ponownym zaopatrzeniu w inne Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="9263a-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="9263a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9263a-141">-ResourceGroupName</span></span>
<span data-ttu-id="9263a-142">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9263a-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9263a-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9263a-143">-ResourceId</span></span>
<span data-ttu-id="9263a-144">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="9263a-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9263a-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="9263a-145">-Tag</span></span>
<span data-ttu-id="9263a-146">Początkowe znaczniki sznurka.</span><span class="sxs-lookup"><span data-stu-id="9263a-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="9263a-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="9263a-147">-WebhookUrl</span></span>
<span data-ttu-id="9263a-148">Adres URL elementu webhook służący do niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="9263a-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="9263a-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9263a-149">-Confirm</span></span>
<span data-ttu-id="9263a-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9263a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9263a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9263a-151">-WhatIf</span></span>
<span data-ttu-id="9263a-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9263a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9263a-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9263a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9263a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9263a-154">CommonParameters</span></span>
<span data-ttu-id="9263a-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9263a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9263a-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9263a-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9263a-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9263a-157">INPUTS</span></span>

### <span data-ttu-id="9263a-158">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9263a-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9263a-159">System. String</span><span class="sxs-lookup"><span data-stu-id="9263a-159">System.String</span></span>

## <span data-ttu-id="9263a-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9263a-160">OUTPUTS</span></span>

### <span data-ttu-id="9263a-161">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="9263a-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="9263a-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9263a-162">NOTES</span></span>

## <span data-ttu-id="9263a-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9263a-163">RELATED LINKS</span></span>
