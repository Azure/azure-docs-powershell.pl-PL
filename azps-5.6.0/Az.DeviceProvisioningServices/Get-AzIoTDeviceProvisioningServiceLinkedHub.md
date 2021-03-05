---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 5aff957c16fa6fefb52706f70016092a37cdcb3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980442"
---
# <span data-ttu-id="9bc4f-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="9bc4f-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="9bc4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bc4f-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc4f-103">Wyświetl wszystkie lub pokaż szczegóły połączonych centrum IoT w usłudze inicjowania obsługi urządzeń w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="9bc4f-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9bc4f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9bc4f-104">SYNTAX</span></span>

### <span data-ttu-id="9bc4f-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9bc4f-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc4f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9bc4f-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc4f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9bc4f-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bc4f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9bc4f-108">DESCRIPTION</span></span>
<span data-ttu-id="9bc4f-109">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="9bc4f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="9bc4f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9bc4f-110">EXAMPLES</span></span>

### <span data-ttu-id="9bc4f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9bc4f-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="9bc4f-112">Lista wszystkich połączonych koncentratorów IoT w sekcji "mojeiotdps".</span><span class="sxs-lookup"><span data-stu-id="9bc4f-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="9bc4f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9bc4f-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="9bc4f-114">Pokaż szczegóły połączonego centrum IoT "myiothub1" w usłudze inicjowania obsługi urządzeń w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="9bc4f-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9bc4f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bc4f-115">PARAMETERS</span></span>

### <span data-ttu-id="9bc4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc4f-116">-DefaultProfile</span></span>
<span data-ttu-id="9bc4f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bc4f-118">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="9bc4f-118">-DpsObject</span></span>
<span data-ttu-id="9bc4f-119">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="9bc4f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9bc4f-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="9bc4f-120">-LinkedHubName</span></span>
<span data-ttu-id="9bc4f-121">Nazwa hosta połączonego centrum IoT</span><span class="sxs-lookup"><span data-stu-id="9bc4f-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="9bc4f-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9bc4f-122">-Name</span></span>
<span data-ttu-id="9bc4f-123">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="9bc4f-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9bc4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bc4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="9bc4f-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9bc4f-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9bc4f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bc4f-126">-ResourceId</span></span>
<span data-ttu-id="9bc4f-127">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="9bc4f-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9bc4f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc4f-128">CommonParameters</span></span>
<span data-ttu-id="9bc4f-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc4f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc4f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc4f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc4f-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bc4f-131">INPUTS</span></span>

### <span data-ttu-id="9bc4f-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9bc4f-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9bc4f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9bc4f-133">System.String</span></span>

## <span data-ttu-id="9bc4f-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bc4f-134">OUTPUTS</span></span>

### <span data-ttu-id="9bc4f-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="9bc4f-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="9bc4f-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="9bc4f-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="9bc4f-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9bc4f-137">NOTES</span></span>

## <span data-ttu-id="9bc4f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bc4f-138">RELATED LINKS</span></span>
