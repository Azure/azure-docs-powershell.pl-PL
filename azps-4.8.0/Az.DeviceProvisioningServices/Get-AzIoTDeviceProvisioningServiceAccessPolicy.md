---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 87c6bdd72229baec8e65c40d4e2e4309bde59aba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222587"
---
# <span data-ttu-id="b1119-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b1119-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="b1119-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1119-102">SYNOPSIS</span></span>
<span data-ttu-id="b1119-103">Wyświetl wszystkie lub Pokaż szczegóły zasad dostępu współdzielonego w usłudze dostarczania urządzeń centrum danych platformy Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="b1119-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b1119-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1119-104">SYNTAX</span></span>

### <span data-ttu-id="b1119-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b1119-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1119-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1119-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1119-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b1119-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1119-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b1119-108">DESCRIPTION</span></span>
<span data-ttu-id="b1119-109">Aby uzyskać wprowadzenie do usługi dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="b1119-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b1119-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1119-110">EXAMPLES</span></span>

### <span data-ttu-id="b1119-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b1119-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="b1119-112">Lista wszystkich zasad dostępu współdzielonego: "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="b1119-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="b1119-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b1119-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="b1119-114">Pokazywanie szczegółów zasad dostępu współużytkowanych w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="b1119-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b1119-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1119-115">PARAMETERS</span></span>

### <span data-ttu-id="b1119-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1119-116">-DefaultProfile</span></span>
<span data-ttu-id="b1119-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1119-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1119-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="b1119-118">-DpsObject</span></span>
<span data-ttu-id="b1119-119">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="b1119-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="b1119-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="b1119-120">-KeyName</span></span>
<span data-ttu-id="b1119-121">Nazwa klucza zasad dostępu do usługi dla urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="b1119-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="b1119-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1119-122">-Name</span></span>
<span data-ttu-id="b1119-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="b1119-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b1119-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1119-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1119-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b1119-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b1119-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1119-126">-ResourceId</span></span>
<span data-ttu-id="b1119-127">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="b1119-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b1119-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1119-128">CommonParameters</span></span>
<span data-ttu-id="b1119-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1119-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1119-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1119-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1119-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1119-131">INPUTS</span></span>

### <span data-ttu-id="b1119-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b1119-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="b1119-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b1119-133">System.String</span></span>

## <span data-ttu-id="b1119-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1119-134">OUTPUTS</span></span>

### <span data-ttu-id="b1119-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="b1119-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="b1119-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1119-136">NOTES</span></span>

## <span data-ttu-id="b1119-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1119-137">RELATED LINKS</span></span>
