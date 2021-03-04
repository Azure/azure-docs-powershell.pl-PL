---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 6fff4be5fb4d0c8b76643e215dfda6d2f3d34ab8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975802"
---
# <span data-ttu-id="9de9d-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9de9d-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="9de9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9de9d-102">SYNOPSIS</span></span>
<span data-ttu-id="9de9d-103">Wyświetl wszystkie lub pokaż szczegóły zasad dostępu udostępnionego w usłudze inicjowania obsługi urządzeń w Centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="9de9d-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9de9d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9de9d-104">SYNTAX</span></span>

### <span data-ttu-id="9de9d-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9de9d-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9de9d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9de9d-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9de9d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9de9d-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9de9d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9de9d-108">DESCRIPTION</span></span>
<span data-ttu-id="9de9d-109">Aby uzyskać wprowadzenie do usługi inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/azure/iot-dps/about-iot-dps zobacz.</span><span class="sxs-lookup"><span data-stu-id="9de9d-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="9de9d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9de9d-110">EXAMPLES</span></span>

### <span data-ttu-id="9de9d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9de9d-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="9de9d-112">Lista wszystkich zasad dostępu udostępnionego w folderze "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="9de9d-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="9de9d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9de9d-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="9de9d-114">Pokaż szczegóły zasad dostępu udostępnionego "mojapolicy" w usłudze inicjowania obsługi urządzeń w Centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="9de9d-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9de9d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9de9d-115">PARAMETERS</span></span>

### <span data-ttu-id="9de9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de9d-116">-DefaultProfile</span></span>
<span data-ttu-id="9de9d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9de9d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de9d-118">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="9de9d-118">-DpsObject</span></span>
<span data-ttu-id="9de9d-119">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="9de9d-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9de9d-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9de9d-120">-KeyName</span></span>
<span data-ttu-id="9de9d-121">Nazwa klucza dostępu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="9de9d-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="9de9d-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9de9d-122">-Name</span></span>
<span data-ttu-id="9de9d-123">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="9de9d-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9de9d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de9d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9de9d-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9de9d-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9de9d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9de9d-126">-ResourceId</span></span>
<span data-ttu-id="9de9d-127">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="9de9d-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9de9d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de9d-128">CommonParameters</span></span>
<span data-ttu-id="9de9d-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de9d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de9d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de9d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de9d-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9de9d-131">INPUTS</span></span>

### <span data-ttu-id="9de9d-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9de9d-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9de9d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9de9d-133">System.String</span></span>

## <span data-ttu-id="9de9d-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9de9d-134">OUTPUTS</span></span>

### <span data-ttu-id="9de9d-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="9de9d-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="9de9d-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9de9d-136">NOTES</span></span>

## <span data-ttu-id="9de9d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9de9d-137">RELATED LINKS</span></span>
