---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 6d3997e8a58ecab6a31e233d4ee3c0e2c66ae9ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994344"
---
# <span data-ttu-id="d662e-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="d662e-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="d662e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d662e-102">SYNOPSIS</span></span>
<span data-ttu-id="d662e-103">Pobiera stan rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="d662e-103">Gets the device registration state.</span></span>

## <span data-ttu-id="d662e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d662e-104">SYNTAX</span></span>

### <span data-ttu-id="d662e-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d662e-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d662e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d662e-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d662e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d662e-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d662e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d662e-108">DESCRIPTION</span></span>
<span data-ttu-id="d662e-109">Uzyskaj stan rejestracji urządzeń lub stan rejestracji urządzeń w ramach grupy rejestracji w usłudze inicjowania obsługi administracyjnej urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="d662e-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="d662e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d662e-110">EXAMPLES</span></span>

### <span data-ttu-id="d662e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d662e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="d662e-112">Uzyskaj szczegółowe informacje o stanie rejestracji urządzeń w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="d662e-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="d662e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d662e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="d662e-114">Lista wszystkich informacji o stanie rejestracji urządzeń w tej grupie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d662e-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="d662e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d662e-115">PARAMETERS</span></span>

### <span data-ttu-id="d662e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d662e-116">-DefaultProfile</span></span>
<span data-ttu-id="d662e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d662e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d662e-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="d662e-118">-DpsName</span></span>
<span data-ttu-id="d662e-119">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d662e-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d662e-120">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="d662e-120">-DpsObject</span></span>
<span data-ttu-id="d662e-121">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d662e-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d662e-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="d662e-122">-EnrollmentId</span></span>
<span data-ttu-id="d662e-123">Identyfikator grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d662e-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="d662e-124">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="d662e-124">-Query</span></span>
<span data-ttu-id="d662e-125">Zapytanie sql.</span><span class="sxs-lookup"><span data-stu-id="d662e-125">Sql query.</span></span>

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

### <span data-ttu-id="d662e-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="d662e-126">-RegistrationId</span></span>
<span data-ttu-id="d662e-127">Identyfikator rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="d662e-127">ID of device registration.</span></span>

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

### <span data-ttu-id="d662e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d662e-128">-ResourceGroupName</span></span>
<span data-ttu-id="d662e-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d662e-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d662e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d662e-130">-ResourceId</span></span>
<span data-ttu-id="d662e-131">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d662e-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d662e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d662e-132">CommonParameters</span></span>
<span data-ttu-id="d662e-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d662e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d662e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d662e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d662e-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d662e-135">INPUTS</span></span>

### <span data-ttu-id="d662e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d662e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d662e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d662e-137">System.String</span></span>

## <span data-ttu-id="d662e-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d662e-138">OUTPUTS</span></span>

### <span data-ttu-id="d662e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="d662e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="d662e-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span><span class="sxs-lookup"><span data-stu-id="d662e-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="d662e-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d662e-141">NOTES</span></span>

## <span data-ttu-id="d662e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d662e-142">RELATED LINKS</span></span>
