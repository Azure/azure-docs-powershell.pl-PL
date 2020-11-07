---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 2da931326b9f900dbf3af3cfcb2e504b413cef33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709870"
---
# <span data-ttu-id="e64d3-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e64d3-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="e64d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e64d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e64d3-103">Zaktualizuj zasady dostępu współużytkowane w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e64d3-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="e64d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e64d3-104">SYNTAX</span></span>

### <span data-ttu-id="e64d3-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e64d3-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e64d3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e64d3-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e64d3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e64d3-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e64d3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e64d3-108">DESCRIPTION</span></span>
<span data-ttu-id="e64d3-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="e64d3-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="e64d3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e64d3-110">EXAMPLES</span></span>

### <span data-ttu-id="e64d3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e64d3-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="e64d3-112">Aktualizowanie zasad dostępu "Moja zasada" w usłudze dostarczania urządzeń centrum usług Azure IoT z EnrollmentWrite prawem.</span><span class="sxs-lookup"><span data-stu-id="e64d3-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="e64d3-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e64d3-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="e64d3-114">Aktualizowanie zasad dostępu "Moja zasada" w usłudze dostarczania urządzeń centrum usług Azure IoT z EnrollmentWrite bezpośrednio przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="e64d3-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="e64d3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e64d3-115">PARAMETERS</span></span>

### <span data-ttu-id="e64d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e64d3-116">-DefaultProfile</span></span>
<span data-ttu-id="e64d3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e64d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e64d3-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e64d3-118">-InputObject</span></span>
<span data-ttu-id="e64d3-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="e64d3-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e64d3-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="e64d3-120">-KeyName</span></span>
<span data-ttu-id="e64d3-121">Nazwa klucza zasad dostępu do usługi dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="e64d3-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="e64d3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e64d3-122">-Name</span></span>
<span data-ttu-id="e64d3-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="e64d3-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e64d3-124">-Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="e64d3-124">-Permissions</span></span>
<span data-ttu-id="e64d3-125">Uprawnienia zasad dostępu do usługi dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="e64d3-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="e64d3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e64d3-126">-ResourceGroupName</span></span>
<span data-ttu-id="e64d3-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e64d3-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e64d3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e64d3-128">-ResourceId</span></span>
<span data-ttu-id="e64d3-129">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="e64d3-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e64d3-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e64d3-130">-Confirm</span></span>
<span data-ttu-id="e64d3-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e64d3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e64d3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e64d3-132">-WhatIf</span></span>
<span data-ttu-id="e64d3-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e64d3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e64d3-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e64d3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e64d3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e64d3-135">CommonParameters</span></span>
<span data-ttu-id="e64d3-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e64d3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e64d3-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e64d3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e64d3-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e64d3-138">INPUTS</span></span>

### <span data-ttu-id="e64d3-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="e64d3-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="e64d3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e64d3-140">System.String</span></span>

## <span data-ttu-id="e64d3-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e64d3-141">OUTPUTS</span></span>

### <span data-ttu-id="e64d3-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="e64d3-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="e64d3-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e64d3-143">NOTES</span></span>

## <span data-ttu-id="e64d3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e64d3-144">RELATED LINKS</span></span>