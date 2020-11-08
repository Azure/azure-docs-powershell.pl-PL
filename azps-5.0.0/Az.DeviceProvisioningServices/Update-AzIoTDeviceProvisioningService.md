---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 411d4594c94fe1eb031f60d6abbff35f5060d4e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224453"
---
# <span data-ttu-id="09221-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="09221-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="09221-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09221-102">SYNOPSIS</span></span>
<span data-ttu-id="09221-103">Aktualizowanie usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="09221-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="09221-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09221-104">SYNTAX</span></span>

### <span data-ttu-id="09221-105">ResourceUpdateSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="09221-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09221-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="09221-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09221-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="09221-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09221-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="09221-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09221-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="09221-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09221-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="09221-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09221-111">Opis</span><span class="sxs-lookup"><span data-stu-id="09221-111">DESCRIPTION</span></span>
<span data-ttu-id="09221-112">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="09221-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="09221-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09221-113">EXAMPLES</span></span>

### <span data-ttu-id="09221-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09221-114">Example 1</span></span>
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

<span data-ttu-id="09221-115">Zaktualizuj zasadę alokacji na "geoopóźnienie" usługi dostarczania urządzeń centrum usług Azure IoT "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="09221-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="09221-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="09221-116">Example 2</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

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

<span data-ttu-id="09221-117">Dodaj " @tags " do znacznika usługi inicjowania obsługi administracyjnej urządzenia centrum usług Azure IoT "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="09221-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="09221-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="09221-118">Example 3</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag @tags -Reset

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

<span data-ttu-id="09221-119">Usuń tag i Dodaj nowy " @tags " do znacznika usługi dostarczania urządzeń centrum usług Azure IoT "myiotdps" przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="09221-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="09221-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09221-120">PARAMETERS</span></span>

### <span data-ttu-id="09221-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="09221-121">-AllocationPolicy</span></span>
<span data-ttu-id="09221-122">Zasady alokacji usług dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="09221-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="09221-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09221-123">-DefaultProfile</span></span>
<span data-ttu-id="09221-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09221-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09221-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="09221-125">-InputObject</span></span>
<span data-ttu-id="09221-126">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="09221-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="09221-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09221-127">-Name</span></span>
<span data-ttu-id="09221-128">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="09221-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="09221-129">-Resetowanie</span><span class="sxs-lookup"><span data-stu-id="09221-129">-Reset</span></span>
<span data-ttu-id="09221-130">Resetowanie numerów seryjnych usług obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="09221-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="09221-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09221-131">-ResourceGroupName</span></span>
<span data-ttu-id="09221-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="09221-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="09221-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09221-133">-ResourceId</span></span>
<span data-ttu-id="09221-134">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="09221-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="09221-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="09221-135">-Tag</span></span>
<span data-ttu-id="09221-136">Kolekcja znaczników usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="09221-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="09221-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09221-137">-Confirm</span></span>
<span data-ttu-id="09221-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09221-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09221-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09221-139">-WhatIf</span></span>
<span data-ttu-id="09221-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09221-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09221-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="09221-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09221-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09221-142">CommonParameters</span></span>
<span data-ttu-id="09221-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09221-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09221-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09221-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09221-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09221-145">INPUTS</span></span>

### <span data-ttu-id="09221-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="09221-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="09221-147">System. String</span><span class="sxs-lookup"><span data-stu-id="09221-147">System.String</span></span>

## <span data-ttu-id="09221-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09221-148">OUTPUTS</span></span>

### <span data-ttu-id="09221-149">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="09221-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="09221-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09221-150">NOTES</span></span>

## <span data-ttu-id="09221-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09221-151">RELATED LINKS</span></span>
