---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ec7f6e6bd402086084bee387be6a0563a6bf0c5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705550"
---
# <span data-ttu-id="afe38-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="afe38-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="afe38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afe38-102">SYNOPSIS</span></span>
<span data-ttu-id="afe38-103">Wyświetl wszystkie lub Pokaż szczegóły połączonego koncentratora IoT w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="afe38-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="afe38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afe38-104">SYNTAX</span></span>

### <span data-ttu-id="afe38-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="afe38-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afe38-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="afe38-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afe38-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="afe38-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afe38-108">Opis</span><span class="sxs-lookup"><span data-stu-id="afe38-108">DESCRIPTION</span></span>
<span data-ttu-id="afe38-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="afe38-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="afe38-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afe38-110">EXAMPLES</span></span>

### <span data-ttu-id="afe38-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="afe38-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="afe38-112">Lista wszystkich połączonych koncentratorów IoT w "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="afe38-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="afe38-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="afe38-113">Example 2</span></span>
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

<span data-ttu-id="afe38-114">Pokaż szczegóły połączonego Centrum IoT "myiothub1" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="afe38-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="afe38-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afe38-115">PARAMETERS</span></span>

### <span data-ttu-id="afe38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe38-116">-DefaultProfile</span></span>
<span data-ttu-id="afe38-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="afe38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afe38-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="afe38-118">-DpsObject</span></span>
<span data-ttu-id="afe38-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="afe38-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="afe38-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="afe38-120">-LinkedHubName</span></span>
<span data-ttu-id="afe38-121">Nazwa hosta połączonego Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="afe38-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="afe38-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="afe38-122">-Name</span></span>
<span data-ttu-id="afe38-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="afe38-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="afe38-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afe38-124">-ResourceGroupName</span></span>
<span data-ttu-id="afe38-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="afe38-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="afe38-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afe38-126">-ResourceId</span></span>
<span data-ttu-id="afe38-127">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="afe38-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="afe38-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe38-128">CommonParameters</span></span>
<span data-ttu-id="afe38-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afe38-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe38-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afe38-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe38-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afe38-131">INPUTS</span></span>

### <span data-ttu-id="afe38-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="afe38-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="afe38-133">System. String</span><span class="sxs-lookup"><span data-stu-id="afe38-133">System.String</span></span>

## <span data-ttu-id="afe38-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afe38-134">OUTPUTS</span></span>

### <span data-ttu-id="afe38-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="afe38-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="afe38-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="afe38-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="afe38-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afe38-137">NOTES</span></span>

## <span data-ttu-id="afe38-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afe38-138">RELATED LINKS</span></span>