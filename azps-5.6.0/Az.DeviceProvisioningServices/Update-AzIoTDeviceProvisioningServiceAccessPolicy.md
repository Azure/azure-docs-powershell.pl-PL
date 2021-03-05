---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: d88d764bc45c4ad767448979348000fbbcec3989
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985062"
---
# <span data-ttu-id="04809-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04809-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="04809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04809-102">SYNOPSIS</span></span>
<span data-ttu-id="04809-103">Zaktualizuj zasady dostępu udostępnionego w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="04809-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="04809-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04809-104">SYNTAX</span></span>

### <span data-ttu-id="04809-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="04809-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04809-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="04809-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04809-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="04809-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04809-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="04809-108">DESCRIPTION</span></span>
<span data-ttu-id="04809-109">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="04809-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="04809-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04809-110">EXAMPLES</span></span>

### <span data-ttu-id="04809-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04809-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="04809-112">Zaktualizuj zasady dostępu "mypolicy" w usłudze inicjowania obsługi urządzeń w centrum IoT Azure za pomocą strony EnrollmentWrite.</span><span class="sxs-lookup"><span data-stu-id="04809-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="04809-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04809-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="04809-114">Zaktualizuj zasady dostępu "mypolicy" w usłudze inicjowania obsługi urządzeń w centrum IoT Azure za pomocą funkcji EnrollmentWrite bezpośrednio przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="04809-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="04809-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04809-115">PARAMETERS</span></span>

### <span data-ttu-id="04809-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04809-116">-DefaultProfile</span></span>
<span data-ttu-id="04809-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="04809-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04809-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04809-118">-InputObject</span></span>
<span data-ttu-id="04809-119">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="04809-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="04809-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="04809-120">-KeyName</span></span>
<span data-ttu-id="04809-121">Nazwa klucza dostępu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="04809-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="04809-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="04809-122">-Name</span></span>
<span data-ttu-id="04809-123">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="04809-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="04809-124">— Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="04809-124">-Permissions</span></span>
<span data-ttu-id="04809-125">Uprawnienia dostępu do usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="04809-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="04809-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04809-126">-ResourceGroupName</span></span>
<span data-ttu-id="04809-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="04809-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="04809-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04809-128">-ResourceId</span></span>
<span data-ttu-id="04809-129">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="04809-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="04809-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04809-130">-Confirm</span></span>
<span data-ttu-id="04809-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="04809-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04809-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04809-132">-WhatIf</span></span>
<span data-ttu-id="04809-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04809-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04809-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="04809-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04809-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04809-135">CommonParameters</span></span>
<span data-ttu-id="04809-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04809-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04809-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04809-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04809-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04809-138">INPUTS</span></span>

### <span data-ttu-id="04809-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="04809-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="04809-140">System.String</span><span class="sxs-lookup"><span data-stu-id="04809-140">System.String</span></span>

## <span data-ttu-id="04809-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04809-141">OUTPUTS</span></span>

### <span data-ttu-id="04809-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="04809-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="04809-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04809-143">NOTES</span></span>

## <span data-ttu-id="04809-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04809-144">RELATED LINKS</span></span>
