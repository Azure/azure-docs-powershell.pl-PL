---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186018"
---
# <span data-ttu-id="07f2b-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="07f2b-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="07f2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="07f2b-103">Uzyskaj grupę rejestracji urządzenia.</span><span class="sxs-lookup"><span data-stu-id="07f2b-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="07f2b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="07f2b-104">SYNTAX</span></span>

### <span data-ttu-id="07f2b-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="07f2b-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07f2b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="07f2b-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07f2b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="07f2b-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07f2b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="07f2b-108">DESCRIPTION</span></span>
<span data-ttu-id="07f2b-109">Uzyskaj szczegółowe informacje dotyczące grupy rejestracji lub listy wszystkich grup rejestracji w usłudze inicjowania obsługi administracyjnej urządzenia w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="07f2b-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="07f2b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="07f2b-110">EXAMPLES</span></span>

### <span data-ttu-id="07f2b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="07f2b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="07f2b-112">Uzyskaj grupę rejestracji urządzeń w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="07f2b-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="07f2b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="07f2b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="07f2b-114">Lista wszystkich grup rejestracji urządzeń w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="07f2b-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="07f2b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07f2b-115">PARAMETERS</span></span>

### <span data-ttu-id="07f2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f2b-116">-DefaultProfile</span></span>
<span data-ttu-id="07f2b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="07f2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f2b-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="07f2b-118">-DpsName</span></span>
<span data-ttu-id="07f2b-119">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="07f2b-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="07f2b-120">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="07f2b-120">-DpsObject</span></span>
<span data-ttu-id="07f2b-121">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="07f2b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="07f2b-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="07f2b-122">-Name</span></span>
<span data-ttu-id="07f2b-123">Nazwa grupy rejestracji.</span><span class="sxs-lookup"><span data-stu-id="07f2b-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="07f2b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f2b-124">-ResourceGroupName</span></span>
<span data-ttu-id="07f2b-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="07f2b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="07f2b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f2b-126">-ResourceId</span></span>
<span data-ttu-id="07f2b-127">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="07f2b-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="07f2b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f2b-128">CommonParameters</span></span>
<span data-ttu-id="07f2b-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f2b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f2b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f2b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f2b-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07f2b-131">INPUTS</span></span>

### <span data-ttu-id="07f2b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="07f2b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="07f2b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="07f2b-133">System.String</span></span>

## <span data-ttu-id="07f2b-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07f2b-134">OUTPUTS</span></span>

### <span data-ttu-id="07f2b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="07f2b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="07f2b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span><span class="sxs-lookup"><span data-stu-id="07f2b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="07f2b-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="07f2b-137">NOTES</span></span>

## <span data-ttu-id="07f2b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07f2b-138">RELATED LINKS</span></span>
