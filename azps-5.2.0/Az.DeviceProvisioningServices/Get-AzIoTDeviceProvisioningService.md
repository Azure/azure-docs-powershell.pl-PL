---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338329"
---
# <span data-ttu-id="8d07c-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="8d07c-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="8d07c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d07c-102">SYNOPSIS</span></span>
<span data-ttu-id="8d07c-103">Wyświetl wszystkie lub Pokaż szczegóły usług udostępniania urządzeń centrum danych platformy Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8d07c-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="8d07c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d07c-104">SYNTAX</span></span>

### <span data-ttu-id="8d07c-105">ListIotDpsByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8d07c-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d07c-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="8d07c-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d07c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8d07c-107">DESCRIPTION</span></span>
<span data-ttu-id="8d07c-108">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="8d07c-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="8d07c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d07c-109">EXAMPLES</span></span>

### <span data-ttu-id="8d07c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8d07c-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="8d07c-111">Lista wszystkich usług dostarczania urządzeń centrum usługi Azure IoT w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="8d07c-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="8d07c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8d07c-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="8d07c-113">Lista wszystkich usług dostarczania urządzeń centrum usługi Azure IoT w grupie zasobów "Moja zasobów".</span><span class="sxs-lookup"><span data-stu-id="8d07c-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="8d07c-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8d07c-114">Example 3</span></span>
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

<span data-ttu-id="8d07c-115">Pokaż szczegóły usługi inicjowania obsługi myiotdps ' urządzenia centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8d07c-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="8d07c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d07c-116">PARAMETERS</span></span>

### <span data-ttu-id="8d07c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d07c-117">-DefaultProfile</span></span>
<span data-ttu-id="8d07c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d07c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d07c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8d07c-119">-Name</span></span>
<span data-ttu-id="8d07c-120">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="8d07c-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8d07c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d07c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d07c-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8d07c-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8d07c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d07c-123">CommonParameters</span></span>
<span data-ttu-id="8d07c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d07c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d07c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d07c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d07c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d07c-126">INPUTS</span></span>

### <span data-ttu-id="8d07c-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8d07c-127">None</span></span>

## <span data-ttu-id="8d07c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d07c-128">OUTPUTS</span></span>

### <span data-ttu-id="8d07c-129">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8d07c-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="8d07c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d07c-130">NOTES</span></span>

## <span data-ttu-id="8d07c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d07c-131">RELATED LINKS</span></span>
