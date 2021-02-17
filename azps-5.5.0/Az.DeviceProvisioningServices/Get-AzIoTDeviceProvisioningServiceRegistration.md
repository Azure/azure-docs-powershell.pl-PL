---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186010"
---
# <span data-ttu-id="c3e47-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="c3e47-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="c3e47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e47-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e47-103">Pobiera stan rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="c3e47-103">Gets the device registration state.</span></span>

## <span data-ttu-id="c3e47-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3e47-104">SYNTAX</span></span>

### <span data-ttu-id="c3e47-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="c3e47-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e47-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3e47-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e47-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c3e47-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e47-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3e47-108">DESCRIPTION</span></span>
<span data-ttu-id="c3e47-109">Uzyskaj stan rejestracji urządzenia lub stan rejestracji urządzeń w ramach grupy rejestracji w usłudze inicjowania obsługi administracyjnej urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e47-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c3e47-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3e47-110">EXAMPLES</span></span>

### <span data-ttu-id="c3e47-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3e47-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="c3e47-112">Uzyskaj szczegółowe informacje o stanie rejestracji urządzeń w usłudze inicjowania obsługi administracyjnej urządzenia w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e47-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="c3e47-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c3e47-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="c3e47-114">Lista wszystkich informacji o stanie rejestracji urządzeń w tej grupie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c3e47-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="c3e47-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3e47-115">PARAMETERS</span></span>

### <span data-ttu-id="c3e47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e47-116">-DefaultProfile</span></span>
<span data-ttu-id="c3e47-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e47-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e47-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="c3e47-118">-DpsName</span></span>
<span data-ttu-id="c3e47-119">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c3e47-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c3e47-120">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="c3e47-120">-DpsObject</span></span>
<span data-ttu-id="c3e47-121">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c3e47-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c3e47-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="c3e47-122">-EnrollmentId</span></span>
<span data-ttu-id="c3e47-123">Identyfikator grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c3e47-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="c3e47-124">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="c3e47-124">-Query</span></span>
<span data-ttu-id="c3e47-125">Zapytanie sql.</span><span class="sxs-lookup"><span data-stu-id="c3e47-125">Sql query.</span></span>

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

### <span data-ttu-id="c3e47-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="c3e47-126">-RegistrationId</span></span>
<span data-ttu-id="c3e47-127">Identyfikator rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="c3e47-127">ID of device registration.</span></span>

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

### <span data-ttu-id="c3e47-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e47-128">-ResourceGroupName</span></span>
<span data-ttu-id="c3e47-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c3e47-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c3e47-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3e47-130">-ResourceId</span></span>
<span data-ttu-id="c3e47-131">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c3e47-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c3e47-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e47-132">CommonParameters</span></span>
<span data-ttu-id="c3e47-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e47-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e47-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e47-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e47-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3e47-135">INPUTS</span></span>

### <span data-ttu-id="c3e47-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c3e47-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c3e47-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c3e47-137">System.String</span></span>

## <span data-ttu-id="c3e47-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3e47-138">OUTPUTS</span></span>

### <span data-ttu-id="c3e47-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="c3e47-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="c3e47-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span><span class="sxs-lookup"><span data-stu-id="c3e47-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="c3e47-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3e47-141">NOTES</span></span>

## <span data-ttu-id="c3e47-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3e47-142">RELATED LINKS</span></span>
