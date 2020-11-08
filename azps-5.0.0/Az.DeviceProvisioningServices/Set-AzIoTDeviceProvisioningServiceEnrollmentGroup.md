---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224456"
---
# <span data-ttu-id="f8a8c-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="f8a8c-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="f8a8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a8c-103">Aktualizowanie grupy rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="f8a8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8a8c-104">SYNTAX</span></span>

### <span data-ttu-id="f8a8c-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a8c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f8a8c-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a8c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f8a8c-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8a8c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f8a8c-108">DESCRIPTION</span></span>
<span data-ttu-id="f8a8c-109">Aktualizowanie grupy rejestracji w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f8a8c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8a8c-110">EXAMPLES</span></span>

### <span data-ttu-id="f8a8c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f8a8c-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="f8a8c-112">Aktualizowanie zasad alokacji i koncentratorów dla grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="f8a8c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8a8c-113">PARAMETERS</span></span>

### <span data-ttu-id="f8a8c-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a8c-114">-AllocationPolicy</span></span>
<span data-ttu-id="f8a8c-115">Typ alokacji urządzenia przypisanego do koncentratora.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="f8a8c-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f8a8c-116">-ApiVersion</span></span>
<span data-ttu-id="f8a8c-117">Wersja interfejsu API usługi inicjowania obsługi w niestandardowym żądaniu alokacji.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="f8a8c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a8c-118">-DefaultProfile</span></span>
<span data-ttu-id="f8a8c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8a8c-120">— Wymagane</span><span class="sxs-lookup"><span data-stu-id="f8a8c-120">-Desired</span></span>
<span data-ttu-id="f8a8c-121">Początkowe sznurki — wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="f8a8c-122">-DpsName</span><span class="sxs-lookup"><span data-stu-id="f8a8c-122">-DpsName</span></span>
<span data-ttu-id="f8a8c-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f8a8c-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="f8a8c-124">-DpsObject</span></span>
<span data-ttu-id="f8a8c-125">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-125">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f8a8c-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="f8a8c-126">-EdgeEnabled</span></span>
<span data-ttu-id="f8a8c-127">Flaga wskazująca możliwość włączenia krawędzi.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-127">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="f8a8c-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="f8a8c-128">-IotHub</span></span>
<span data-ttu-id="f8a8c-129">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="f8a8c-130">Użyj listy rozdzielanej spacjami dla wielu koncentratorów IoT.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-130">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="f8a8c-131">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="f8a8c-131">-IotHubHostName</span></span>
<span data-ttu-id="f8a8c-132">Nazwa hosta docelowego Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="f8a8c-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8a8c-133">-Name</span></span>
<span data-ttu-id="f8a8c-134">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-134">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="f8a8c-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="f8a8c-135">-ProvisioningStatus</span></span>
<span data-ttu-id="f8a8c-136">Włączanie lub wyłączanie wpisu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="f8a8c-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="f8a8c-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="f8a8c-138">Dane urządzenia, które mają być obsługiwane na ponownym zaopatrzeniu w inne Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="f8a8c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a8c-139">-ResourceGroupName</span></span>
<span data-ttu-id="f8a8c-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f8a8c-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f8a8c-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8a8c-141">-ResourceId</span></span>
<span data-ttu-id="f8a8c-142">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="f8a8c-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f8a8c-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8a8c-143">-Tag</span></span>
<span data-ttu-id="f8a8c-144">Początkowe znaczniki sznurka.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="f8a8c-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="f8a8c-145">-WebhookUrl</span></span>
<span data-ttu-id="f8a8c-146">Adres URL elementu webhook służący do niestandardowych żądań alokacji.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="f8a8c-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8a8c-147">-Confirm</span></span>
<span data-ttu-id="f8a8c-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8a8c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8a8c-149">-WhatIf</span></span>
<span data-ttu-id="f8a8c-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8a8c-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8a8c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a8c-152">CommonParameters</span></span>
<span data-ttu-id="f8a8c-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8a8c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a8c-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8a8c-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a8c-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-155">INPUTS</span></span>

### <span data-ttu-id="f8a8c-156">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f8a8c-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="f8a8c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f8a8c-157">System.String</span></span>

## <span data-ttu-id="f8a8c-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8a8c-158">OUTPUTS</span></span>

### <span data-ttu-id="f8a8c-159">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="f8a8c-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="f8a8c-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8a8c-160">NOTES</span></span>

## <span data-ttu-id="f8a8c-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8a8c-161">RELATED LINKS</span></span>
