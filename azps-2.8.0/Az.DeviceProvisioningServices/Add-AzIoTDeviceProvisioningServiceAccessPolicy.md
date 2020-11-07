---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 8465a9b86d701ef4ec21058d39734098f91f2a7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705565"
---
# <span data-ttu-id="5fccd-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5fccd-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="5fccd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fccd-102">SYNOPSIS</span></span>
<span data-ttu-id="5fccd-103">Dodaj nowe zasady dostępu współdzielonego do usługi dostarczania urządzeń centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5fccd-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5fccd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fccd-104">SYNTAX</span></span>

### <span data-ttu-id="5fccd-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5fccd-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fccd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5fccd-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fccd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5fccd-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fccd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5fccd-108">DESCRIPTION</span></span>
<span data-ttu-id="5fccd-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5fccd-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5fccd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fccd-110">EXAMPLES</span></span>

### <span data-ttu-id="5fccd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5fccd-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="5fccd-112">Dodaj nowe zasady dostępu współdzielonego do usługi dostarczania urządzeń centrum usług Azure IoT, korzystając z praw EnrollmentWrite i ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="5fccd-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="5fccd-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5fccd-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="5fccd-114">Dodaj nowe zasady dostępu współdzielonego do usługi dostarczania urządzeń centrum usługi Azure IoT, korzystając z EnrollmentRead prawej.</span><span class="sxs-lookup"><span data-stu-id="5fccd-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="5fccd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fccd-115">PARAMETERS</span></span>

### <span data-ttu-id="5fccd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fccd-116">-DefaultProfile</span></span>
<span data-ttu-id="5fccd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fccd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fccd-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5fccd-118">-DpsObject</span></span>
<span data-ttu-id="5fccd-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5fccd-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5fccd-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="5fccd-120">-KeyName</span></span>
<span data-ttu-id="5fccd-121">Nazwa klucza zasad dostępu do usługi dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5fccd-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="5fccd-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5fccd-122">-Name</span></span>
<span data-ttu-id="5fccd-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5fccd-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5fccd-124">-Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="5fccd-124">-Permissions</span></span>
<span data-ttu-id="5fccd-125">Uprawnienia zasad dostępu do usługi dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5fccd-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="5fccd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fccd-126">-ResourceGroupName</span></span>
<span data-ttu-id="5fccd-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5fccd-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5fccd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fccd-128">-ResourceId</span></span>
<span data-ttu-id="5fccd-129">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="5fccd-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5fccd-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5fccd-130">-Confirm</span></span>
<span data-ttu-id="5fccd-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fccd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fccd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fccd-132">-WhatIf</span></span>
<span data-ttu-id="5fccd-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fccd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fccd-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5fccd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fccd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fccd-135">CommonParameters</span></span>
<span data-ttu-id="5fccd-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fccd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fccd-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fccd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fccd-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fccd-138">INPUTS</span></span>

### <span data-ttu-id="5fccd-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5fccd-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5fccd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5fccd-140">System.String</span></span>

## <span data-ttu-id="5fccd-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fccd-141">OUTPUTS</span></span>

### <span data-ttu-id="5fccd-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="5fccd-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="5fccd-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fccd-143">NOTES</span></span>

## <span data-ttu-id="5fccd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fccd-144">RELATED LINKS</span></span>