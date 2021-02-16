---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243739"
---
# <span data-ttu-id="c9c5a-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c9c5a-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="c9c5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c5a-103">Dodaj nowe zasady dostępu udostępnionego w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c9c5a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9c5a-104">SYNTAX</span></span>

### <span data-ttu-id="c9c5a-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="c9c5a-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c5a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c9c5a-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c5a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c9c5a-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c5a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9c5a-108">DESCRIPTION</span></span>
<span data-ttu-id="c9c5a-109">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c9c5a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9c5a-110">EXAMPLES</span></span>

### <span data-ttu-id="c9c5a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9c5a-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="c9c5a-112">Dodaj nowe zasady dostępu udostępnionego w usłudze inicjowania obsługi administracyjnej urządzenia w centrum IoT Azure za pomocą praw EnrollmentWrite i ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="c9c5a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c9c5a-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="c9c5a-114">Dodaj nowe zasady dostępu udostępnionego w usłudze inicjowania obsługi urządzeń w centrum IoT Azure z prawej strony enrollmentread.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="c9c5a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9c5a-115">PARAMETERS</span></span>

### <span data-ttu-id="c9c5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c5a-116">-DefaultProfile</span></span>
<span data-ttu-id="c9c5a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c5a-118">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="c9c5a-118">-DpsObject</span></span>
<span data-ttu-id="c9c5a-119">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9c5a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c9c5a-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c9c5a-120">-KeyName</span></span>
<span data-ttu-id="c9c5a-121">Nazwa klucza dostępu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9c5a-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c5a-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c9c5a-122">-Name</span></span>
<span data-ttu-id="c9c5a-123">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9c5a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c9c5a-124">— Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="c9c5a-124">-Permissions</span></span>
<span data-ttu-id="c9c5a-125">Uprawnienia dostępu do usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9c5a-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c5a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c5a-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9c5a-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c9c5a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c9c5a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9c5a-128">-ResourceId</span></span>
<span data-ttu-id="c9c5a-129">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c9c5a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c9c5a-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9c5a-130">-Confirm</span></span>
<span data-ttu-id="c9c5a-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c5a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c5a-132">-WhatIf</span></span>
<span data-ttu-id="c9c5a-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9c5a-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c5a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c5a-135">CommonParameters</span></span>
<span data-ttu-id="c9c5a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c5a-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c5a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c5a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9c5a-138">INPUTS</span></span>

### <span data-ttu-id="c9c5a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c9c5a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c9c5a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c9c5a-140">System.String</span></span>

## <span data-ttu-id="c9c5a-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9c5a-141">OUTPUTS</span></span>

### <span data-ttu-id="c9c5a-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="c9c5a-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="c9c5a-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9c5a-143">NOTES</span></span>

## <span data-ttu-id="c9c5a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9c5a-144">RELATED LINKS</span></span>
