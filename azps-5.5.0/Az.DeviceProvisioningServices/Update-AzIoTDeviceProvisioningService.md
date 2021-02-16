---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: f533bd07d0c7b123f1d109e7abd933736093cd79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194474"
---
# <span data-ttu-id="c9593-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="c9593-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="c9593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9593-102">SYNOPSIS</span></span>
<span data-ttu-id="c9593-103">Zaktualizuj usługę inicjowania obsługi urządzeń w Centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="c9593-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c9593-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9593-104">SYNTAX</span></span>

### <span data-ttu-id="c9593-105">ResourceUpdateSet (Default)</span><span class="sxs-lookup"><span data-stu-id="c9593-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9593-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="c9593-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9593-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="c9593-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9593-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="c9593-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9593-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="c9593-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9593-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="c9593-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9593-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9593-111">DESCRIPTION</span></span>
<span data-ttu-id="c9593-112">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="c9593-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c9593-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9593-113">EXAMPLES</span></span>

### <span data-ttu-id="c9593-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9593-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="c9593-115">Zaktualizuj zasady alokacji do ustawienia "GeoLatency" usługi inicjowania obsługi urządzeń w centrum IoT Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="c9593-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="c9593-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c9593-116">Example 2</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tag

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="c9593-117">Dodaj tagi do usługi inicjowania obsługi urządzeń w centrum IoT Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="c9593-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="c9593-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c9593-118">Example 3</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag $tag -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="c9593-119">Usuń tag i dodaj nowe tagi do usługi inicjowania obsługi urządzeń w centrum Azure IoT Hub "myiotdps" przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="c9593-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="c9593-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9593-120">PARAMETERS</span></span>

### <span data-ttu-id="c9593-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="c9593-121">-AllocationPolicy</span></span>
<span data-ttu-id="c9593-122">Zasady alokacji usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9593-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9593-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9593-123">-DefaultProfile</span></span>
<span data-ttu-id="c9593-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9593-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9593-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9593-125">-InputObject</span></span>
<span data-ttu-id="c9593-126">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9593-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9593-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c9593-127">-Name</span></span>
<span data-ttu-id="c9593-128">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9593-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9593-129">— Resetowanie</span><span class="sxs-lookup"><span data-stu-id="c9593-129">-Reset</span></span>
<span data-ttu-id="c9593-130">Resetowanie tagów usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9593-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9593-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9593-131">-ResourceGroupName</span></span>
<span data-ttu-id="c9593-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c9593-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9593-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9593-133">-ResourceId</span></span>
<span data-ttu-id="c9593-134">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9593-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9593-135">— Tag</span><span class="sxs-lookup"><span data-stu-id="c9593-135">-Tag</span></span>
<span data-ttu-id="c9593-136">Kolekcja tagów usługi inicjowania obsługi administracyjnej urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9593-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9593-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9593-137">-Confirm</span></span>
<span data-ttu-id="c9593-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9593-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9593-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9593-139">-WhatIf</span></span>
<span data-ttu-id="c9593-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9593-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9593-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9593-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9593-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9593-142">CommonParameters</span></span>
<span data-ttu-id="c9593-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9593-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9593-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9593-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9593-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9593-145">INPUTS</span></span>

### <span data-ttu-id="c9593-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c9593-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c9593-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c9593-147">System.String</span></span>

## <span data-ttu-id="c9593-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9593-148">OUTPUTS</span></span>

### <span data-ttu-id="c9593-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c9593-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="c9593-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9593-150">NOTES</span></span>

## <span data-ttu-id="c9593-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9593-151">RELATED LINKS</span></span>
