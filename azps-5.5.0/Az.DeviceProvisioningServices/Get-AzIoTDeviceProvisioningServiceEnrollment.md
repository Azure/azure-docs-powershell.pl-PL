---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237969"
---
# <span data-ttu-id="c7e3b-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="c7e3b-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="c7e3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e3b-103">Pobierz rekord rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="c7e3b-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="c7e3b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c7e3b-104">SYNTAX</span></span>

### <span data-ttu-id="c7e3b-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="c7e3b-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7e3b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c7e3b-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7e3b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c7e3b-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7e3b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c7e3b-108">DESCRIPTION</span></span>
<span data-ttu-id="c7e3b-109">Uzyskaj szczegółowe informacje dotyczące rejestrowania urządzeń lub uzyskaj listę rejestracji urządzeń w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e3b-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c7e3b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c7e3b-110">EXAMPLES</span></span>

### <span data-ttu-id="c7e3b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7e3b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="c7e3b-112">Uzyskaj szczegółowe informacje dotyczące rejestrowania urządzeń w usłudze inicjowania obsługi administracyjnej urządzenia w centrum Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="c7e3b-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="c7e3b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c7e3b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="c7e3b-114">Lista rejestracji urządzeń w usłudze inicjowania obsługi administracyjnej urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e3b-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c7e3b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7e3b-115">PARAMETERS</span></span>

### <span data-ttu-id="c7e3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e3b-116">-DefaultProfile</span></span>
<span data-ttu-id="c7e3b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e3b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7e3b-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="c7e3b-118">-DpsName</span></span>
<span data-ttu-id="c7e3b-119">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c7e3b-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c7e3b-120">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="c7e3b-120">-DpsObject</span></span>
<span data-ttu-id="c7e3b-121">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c7e3b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c7e3b-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="c7e3b-122">-RegistrationId</span></span>
<span data-ttu-id="c7e3b-123">Identyfikator rejestracji indywidualnej.</span><span class="sxs-lookup"><span data-stu-id="c7e3b-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="c7e3b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7e3b-124">-ResourceGroupName</span></span>
<span data-ttu-id="c7e3b-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c7e3b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c7e3b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7e3b-126">-ResourceId</span></span>
<span data-ttu-id="c7e3b-127">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="c7e3b-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c7e3b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e3b-128">CommonParameters</span></span>
<span data-ttu-id="c7e3b-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7e3b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e3b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7e3b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e3b-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7e3b-131">INPUTS</span></span>

### <span data-ttu-id="c7e3b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c7e3b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c7e3b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c7e3b-133">System.String</span></span>

## <span data-ttu-id="c7e3b-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7e3b-134">OUTPUTS</span></span>

### <span data-ttu-id="c7e3b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="c7e3b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="c7e3b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span><span class="sxs-lookup"><span data-stu-id="c7e3b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="c7e3b-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c7e3b-137">NOTES</span></span>

## <span data-ttu-id="c7e3b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7e3b-138">RELATED LINKS</span></span>
