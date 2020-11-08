---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223517"
---
# <span data-ttu-id="ecfb0-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="ecfb0-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="ecfb0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ecfb0-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfb0-103">Uzyskaj grupę rejestracji urządzeń.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="ecfb0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ecfb0-104">SYNTAX</span></span>

### <span data-ttu-id="ecfb0-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ecfb0-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecfb0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ecfb0-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecfb0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ecfb0-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecfb0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ecfb0-108">DESCRIPTION</span></span>
<span data-ttu-id="ecfb0-109">Zapoznaj się z informacjami na temat grupy rejestracji lub listy wszystkich grup rejestracji w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="ecfb0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ecfb0-110">EXAMPLES</span></span>

### <span data-ttu-id="ecfb0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ecfb0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="ecfb0-112">Pobierz grupę rejestracji urządzeń w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="ecfb0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ecfb0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="ecfb0-114">Lista wszystkich grup rejestracji urządzeń w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="ecfb0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ecfb0-115">PARAMETERS</span></span>

### <span data-ttu-id="ecfb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfb0-116">-DefaultProfile</span></span>
<span data-ttu-id="ecfb0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecfb0-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="ecfb0-118">-DpsName</span></span>
<span data-ttu-id="ecfb0-119">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="ecfb0-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ecfb0-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="ecfb0-120">-DpsObject</span></span>
<span data-ttu-id="ecfb0-121">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="ecfb0-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ecfb0-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ecfb0-122">-Name</span></span>
<span data-ttu-id="ecfb0-123">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="ecfb0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfb0-124">-ResourceGroupName</span></span>
<span data-ttu-id="ecfb0-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ecfb0-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ecfb0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecfb0-126">-ResourceId</span></span>
<span data-ttu-id="ecfb0-127">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="ecfb0-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ecfb0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfb0-128">CommonParameters</span></span>
<span data-ttu-id="ecfb0-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfb0-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfb0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfb0-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecfb0-131">INPUTS</span></span>

### <span data-ttu-id="ecfb0-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ecfb0-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="ecfb0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ecfb0-133">System.String</span></span>

## <span data-ttu-id="ecfb0-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ecfb0-134">OUTPUTS</span></span>

### <span data-ttu-id="ecfb0-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="ecfb0-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="ecfb0-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSEnrollmentGroups []</span><span class="sxs-lookup"><span data-stu-id="ecfb0-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="ecfb0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ecfb0-137">NOTES</span></span>

## <span data-ttu-id="ecfb0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecfb0-138">RELATED LINKS</span></span>
