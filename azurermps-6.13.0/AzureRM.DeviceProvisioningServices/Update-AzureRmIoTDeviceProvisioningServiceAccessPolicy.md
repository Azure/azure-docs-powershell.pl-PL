---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f5d750dc795619f32f6c4f16a5fe1e3b5e111106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719130"
---
# <span data-ttu-id="a00cf-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a00cf-101">Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="a00cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a00cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a00cf-103">Zaktualizuj zasady dostępu współużytkowane w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="a00cf-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a00cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a00cf-104">SYNTAX</span></span>

### <span data-ttu-id="a00cf-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a00cf-105">ResourceSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a00cf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a00cf-106">InputObjectSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a00cf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a00cf-107">ResourceIdSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a00cf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a00cf-108">DESCRIPTION</span></span>
<span data-ttu-id="a00cf-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="a00cf-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a00cf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a00cf-110">EXAMPLES</span></span>

### <span data-ttu-id="a00cf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a00cf-111">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="a00cf-112">Aktualizowanie zasad dostępu "Moja zasada" w usłudze dostarczania urządzeń centrum usług Azure IoT z EnrollmentWrite prawem.</span><span class="sxs-lookup"><span data-stu-id="a00cf-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="a00cf-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a00cf-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzureRmIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="a00cf-114">Aktualizowanie zasad dostępu "Moja zasada" w usłudze dostarczania urządzeń centrum usług Azure IoT z EnrollmentWrite bezpośrednio przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="a00cf-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="a00cf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a00cf-115">PARAMETERS</span></span>

### <span data-ttu-id="a00cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a00cf-116">-DefaultProfile</span></span>
<span data-ttu-id="a00cf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a00cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00cf-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a00cf-118">-InputObject</span></span>
<span data-ttu-id="a00cf-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a00cf-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a00cf-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="a00cf-120">-KeyName</span></span>
<span data-ttu-id="a00cf-121">Nazwa klucza zasad dostępu do usługi dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a00cf-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="a00cf-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a00cf-122">-Name</span></span>
<span data-ttu-id="a00cf-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a00cf-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a00cf-124">-Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="a00cf-124">-Permissions</span></span>
<span data-ttu-id="a00cf-125">Uprawnienia zasad dostępu do usługi dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a00cf-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="a00cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a00cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="a00cf-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a00cf-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a00cf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a00cf-128">-ResourceId</span></span>
<span data-ttu-id="a00cf-129">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a00cf-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a00cf-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a00cf-130">-Confirm</span></span>
<span data-ttu-id="a00cf-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a00cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a00cf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a00cf-132">-WhatIf</span></span>
<span data-ttu-id="a00cf-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a00cf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a00cf-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a00cf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a00cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00cf-135">CommonParameters</span></span>
<span data-ttu-id="a00cf-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a00cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00cf-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a00cf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00cf-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a00cf-138">INPUTS</span></span>

### <span data-ttu-id="a00cf-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="a00cf-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="a00cf-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a00cf-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a00cf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a00cf-141">System.String</span></span>

## <span data-ttu-id="a00cf-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a00cf-142">OUTPUTS</span></span>

### <span data-ttu-id="a00cf-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="a00cf-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="a00cf-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a00cf-144">NOTES</span></span>

## <span data-ttu-id="a00cf-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a00cf-145">RELATED LINKS</span></span>
