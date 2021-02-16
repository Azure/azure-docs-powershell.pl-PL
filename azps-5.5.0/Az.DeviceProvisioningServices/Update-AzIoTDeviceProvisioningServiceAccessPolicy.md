---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194467"
---
# <span data-ttu-id="dabe6-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dabe6-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="dabe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dabe6-102">SYNOPSIS</span></span>
<span data-ttu-id="dabe6-103">Zaktualizuj zasady dostępu udostępnionego w usłudze inicjowania obsługi urządzeń w Centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="dabe6-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="dabe6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dabe6-104">SYNTAX</span></span>

### <span data-ttu-id="dabe6-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="dabe6-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dabe6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dabe6-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dabe6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dabe6-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dabe6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="dabe6-108">DESCRIPTION</span></span>
<span data-ttu-id="dabe6-109">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="dabe6-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="dabe6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dabe6-110">EXAMPLES</span></span>

### <span data-ttu-id="dabe6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dabe6-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="dabe6-112">Zaktualizuj zasady dostępu "mojapolicja" w usłudze inicjowania obsługi urządzeń w Centrum IoT Azure za pomocą strony RejestracjaWrite.</span><span class="sxs-lookup"><span data-stu-id="dabe6-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="dabe6-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dabe6-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="dabe6-114">Zaktualizuj zasady dostępu "mypolicy" w usłudze inicjowania obsługi urządzeń w centrum IoT Azure za pomocą funkcji EnrollmentWrite bezpośrednio przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="dabe6-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="dabe6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dabe6-115">PARAMETERS</span></span>

### <span data-ttu-id="dabe6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabe6-116">-DefaultProfile</span></span>
<span data-ttu-id="dabe6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dabe6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dabe6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dabe6-118">-InputObject</span></span>
<span data-ttu-id="dabe6-119">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="dabe6-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dabe6-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="dabe6-120">-KeyName</span></span>
<span data-ttu-id="dabe6-121">Nazwa klucza dostępu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="dabe6-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabe6-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dabe6-122">-Name</span></span>
<span data-ttu-id="dabe6-123">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="dabe6-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="dabe6-124">— Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="dabe6-124">-Permissions</span></span>
<span data-ttu-id="dabe6-125">Uprawnienia dostępu do usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="dabe6-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="dabe6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabe6-126">-ResourceGroupName</span></span>
<span data-ttu-id="dabe6-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dabe6-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dabe6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dabe6-128">-ResourceId</span></span>
<span data-ttu-id="dabe6-129">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="dabe6-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="dabe6-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dabe6-130">-Confirm</span></span>
<span data-ttu-id="dabe6-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dabe6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dabe6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dabe6-132">-WhatIf</span></span>
<span data-ttu-id="dabe6-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dabe6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dabe6-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dabe6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dabe6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabe6-135">CommonParameters</span></span>
<span data-ttu-id="dabe6-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dabe6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabe6-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabe6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabe6-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dabe6-138">INPUTS</span></span>

### <span data-ttu-id="dabe6-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="dabe6-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="dabe6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="dabe6-140">System.String</span></span>

## <span data-ttu-id="dabe6-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dabe6-141">OUTPUTS</span></span>

### <span data-ttu-id="dabe6-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="dabe6-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="dabe6-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dabe6-143">NOTES</span></span>

## <span data-ttu-id="dabe6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dabe6-144">RELATED LINKS</span></span>
