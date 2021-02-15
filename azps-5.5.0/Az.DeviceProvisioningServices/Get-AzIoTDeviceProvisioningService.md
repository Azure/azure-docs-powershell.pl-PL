---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238009"
---
# <span data-ttu-id="85f62-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="85f62-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="85f62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85f62-102">SYNOPSIS</span></span>
<span data-ttu-id="85f62-103">Wyświetl wszystkie lub pokaż szczegóły usług inicjowania obsługi urządzeń w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="85f62-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="85f62-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="85f62-104">SYNTAX</span></span>

### <span data-ttu-id="85f62-105">ListIotDpsByResourceGroup (domyślna)</span><span class="sxs-lookup"><span data-stu-id="85f62-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85f62-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="85f62-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85f62-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="85f62-107">DESCRIPTION</span></span>
<span data-ttu-id="85f62-108">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="85f62-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="85f62-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="85f62-109">EXAMPLES</span></span>

### <span data-ttu-id="85f62-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85f62-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="85f62-111">Lista wszystkich usług inicjowania obsługi urządzeń w centrum Azure IoT Hub w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="85f62-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="85f62-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="85f62-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="85f62-113">W grupie zasobów "myresourcegroup" (grupa zasobów) należy wyświetlić listę wszystkich usług inicjowania obsługi urządzeń w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="85f62-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="85f62-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="85f62-114">Example 3</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="85f62-115">Pokaż szczegóły dotyczące usługi inicjowania obsługi urządzeń w centrum IoT Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="85f62-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="85f62-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85f62-116">PARAMETERS</span></span>

### <span data-ttu-id="85f62-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f62-117">-DefaultProfile</span></span>
<span data-ttu-id="85f62-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="85f62-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85f62-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="85f62-119">-Name</span></span>
<span data-ttu-id="85f62-120">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="85f62-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f62-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85f62-121">-ResourceGroupName</span></span>
<span data-ttu-id="85f62-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="85f62-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotDpsByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f62-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f62-123">CommonParameters</span></span>
<span data-ttu-id="85f62-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f62-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f62-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85f62-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f62-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85f62-126">INPUTS</span></span>

### <span data-ttu-id="85f62-127">Brak</span><span class="sxs-lookup"><span data-stu-id="85f62-127">None</span></span>

## <span data-ttu-id="85f62-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85f62-128">OUTPUTS</span></span>

### <span data-ttu-id="85f62-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="85f62-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="85f62-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="85f62-130">NOTES</span></span>

## <span data-ttu-id="85f62-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85f62-131">RELATED LINKS</span></span>
