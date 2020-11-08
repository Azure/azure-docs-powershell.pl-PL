---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224480"
---
# <span data-ttu-id="53bdf-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="53bdf-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="53bdf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="53bdf-103">Pobiera stan rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="53bdf-103">Gets the device registration state.</span></span>

## <span data-ttu-id="53bdf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53bdf-104">SYNTAX</span></span>

### <span data-ttu-id="53bdf-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="53bdf-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53bdf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="53bdf-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53bdf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="53bdf-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53bdf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="53bdf-108">DESCRIPTION</span></span>
<span data-ttu-id="53bdf-109">Uzyskaj stan rejestracji urządzenia lub stan rejestracji urządzeń w grupie rejestrowanie w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="53bdf-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="53bdf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53bdf-110">EXAMPLES</span></span>

### <span data-ttu-id="53bdf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53bdf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="53bdf-112">Uzyskaj szczegółowe informacje o stanie rejestracji urządzenia w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="53bdf-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="53bdf-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="53bdf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="53bdf-114">Wyświetlanie listy wszystkich stanów rejestracji urządzeń w tej usłudze rejestracji.</span><span class="sxs-lookup"><span data-stu-id="53bdf-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="53bdf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53bdf-115">PARAMETERS</span></span>

### <span data-ttu-id="53bdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bdf-116">-DefaultProfile</span></span>
<span data-ttu-id="53bdf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53bdf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53bdf-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="53bdf-118">-DpsName</span></span>
<span data-ttu-id="53bdf-119">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="53bdf-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="53bdf-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="53bdf-120">-DpsObject</span></span>
<span data-ttu-id="53bdf-121">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="53bdf-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="53bdf-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="53bdf-122">-EnrollmentId</span></span>
<span data-ttu-id="53bdf-123">Identyfikator grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="53bdf-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="53bdf-124">-Query</span><span class="sxs-lookup"><span data-stu-id="53bdf-124">-Query</span></span>
<span data-ttu-id="53bdf-125">Kwerenda SQL.</span><span class="sxs-lookup"><span data-stu-id="53bdf-125">Sql query.</span></span>

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

### <span data-ttu-id="53bdf-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="53bdf-126">-RegistrationId</span></span>
<span data-ttu-id="53bdf-127">Identyfikator rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="53bdf-127">ID of device registration.</span></span>

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

### <span data-ttu-id="53bdf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53bdf-128">-ResourceGroupName</span></span>
<span data-ttu-id="53bdf-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="53bdf-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="53bdf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53bdf-130">-ResourceId</span></span>
<span data-ttu-id="53bdf-131">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="53bdf-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="53bdf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bdf-132">CommonParameters</span></span>
<span data-ttu-id="53bdf-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53bdf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bdf-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53bdf-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bdf-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53bdf-135">INPUTS</span></span>

### <span data-ttu-id="53bdf-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="53bdf-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="53bdf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="53bdf-137">System.String</span></span>

## <span data-ttu-id="53bdf-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53bdf-138">OUTPUTS</span></span>

### <span data-ttu-id="53bdf-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="53bdf-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="53bdf-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="53bdf-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="53bdf-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53bdf-141">NOTES</span></span>

## <span data-ttu-id="53bdf-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53bdf-142">RELATED LINKS</span></span>
