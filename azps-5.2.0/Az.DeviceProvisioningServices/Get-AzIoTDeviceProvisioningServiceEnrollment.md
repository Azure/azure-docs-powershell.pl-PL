---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328776"
---
# <span data-ttu-id="8ea8c-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="8ea8c-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="8ea8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ea8c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea8c-103">Pobierz rekord rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="8ea8c-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="8ea8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ea8c-104">SYNTAX</span></span>

### <span data-ttu-id="8ea8c-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8ea8c-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ea8c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8ea8c-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ea8c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8ea8c-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ea8c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8ea8c-108">DESCRIPTION</span></span>
<span data-ttu-id="8ea8c-109">Uzyskiwanie szczegółowych informacji o rejestracji urządzeń lub wyświetlanie rejestracji urządzeń w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8ea8c-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="8ea8c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ea8c-110">EXAMPLES</span></span>

### <span data-ttu-id="8ea8c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ea8c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="8ea8c-112">Uzyskiwanie szczegółowych informacji o rejestracji urządzeń w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8ea8c-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="8ea8c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8ea8c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="8ea8c-114">Wyświetlanie rejestracji urządzeń w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8ea8c-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="8ea8c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ea8c-115">PARAMETERS</span></span>

### <span data-ttu-id="8ea8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea8c-116">-DefaultProfile</span></span>
<span data-ttu-id="8ea8c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ea8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ea8c-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="8ea8c-118">-DpsName</span></span>
<span data-ttu-id="8ea8c-119">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="8ea8c-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8ea8c-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="8ea8c-120">-DpsObject</span></span>
<span data-ttu-id="8ea8c-121">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="8ea8c-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="8ea8c-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="8ea8c-122">-RegistrationId</span></span>
<span data-ttu-id="8ea8c-123">Indywidualny Identyfikator rejestracji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="8ea8c-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="8ea8c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ea8c-124">-ResourceGroupName</span></span>
<span data-ttu-id="8ea8c-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8ea8c-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8ea8c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ea8c-126">-ResourceId</span></span>
<span data-ttu-id="8ea8c-127">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="8ea8c-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="8ea8c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea8c-128">CommonParameters</span></span>
<span data-ttu-id="8ea8c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ea8c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea8c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea8c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea8c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ea8c-131">INPUTS</span></span>

### <span data-ttu-id="8ea8c-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8ea8c-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="8ea8c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8ea8c-133">System.String</span></span>

## <span data-ttu-id="8ea8c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ea8c-134">OUTPUTS</span></span>

### <span data-ttu-id="8ea8c-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="8ea8c-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="8ea8c-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIndividualEnrollments []</span><span class="sxs-lookup"><span data-stu-id="8ea8c-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="8ea8c-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ea8c-137">NOTES</span></span>

## <span data-ttu-id="8ea8c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ea8c-138">RELATED LINKS</span></span>
