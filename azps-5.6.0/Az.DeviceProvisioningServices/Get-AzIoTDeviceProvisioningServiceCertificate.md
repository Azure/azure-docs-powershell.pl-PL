---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 788759abe543d3bddf3c67abe2ed37aafca6be3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978545"
---
# <span data-ttu-id="add05-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="add05-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="add05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="add05-102">SYNOPSIS</span></span>
<span data-ttu-id="add05-103">Lista wszystkich certyfikatów lub określonego certyfikatu zawartego w usłudze inicjowania obsługi urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="add05-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="add05-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="add05-104">SYNTAX</span></span>

### <span data-ttu-id="add05-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="add05-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add05-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="add05-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add05-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="add05-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="add05-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="add05-108">DESCRIPTION</span></span>
<span data-ttu-id="add05-109">Aby uzyskać szczegółowe objaśnienie certyfikatów urzędu certyfikacji w usłudze inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates zobacz.</span><span class="sxs-lookup"><span data-stu-id="add05-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="add05-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="add05-110">EXAMPLES</span></span>

### <span data-ttu-id="add05-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="add05-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="add05-112">Pokaż szczegóły dotyczące "mycertificate" w usłudze inicjowania obsługi urządzeń w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="add05-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="add05-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="add05-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="add05-114">Lista wszystkich certyfikatów w "myiotdps" przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="add05-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="add05-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="add05-115">PARAMETERS</span></span>

### <span data-ttu-id="add05-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="add05-116">-CertificateName</span></span>
<span data-ttu-id="add05-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="add05-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="add05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add05-118">-DefaultProfile</span></span>
<span data-ttu-id="add05-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="add05-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="add05-120">- DpsObject</span><span class="sxs-lookup"><span data-stu-id="add05-120">-DpsObject</span></span>
<span data-ttu-id="add05-121">Obiekt usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="add05-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="add05-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="add05-122">-Name</span></span>
<span data-ttu-id="add05-123">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="add05-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="add05-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add05-124">-ResourceGroupName</span></span>
<span data-ttu-id="add05-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="add05-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="add05-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="add05-126">-ResourceId</span></span>
<span data-ttu-id="add05-127">Identyfikator zasobu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="add05-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="add05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add05-128">CommonParameters</span></span>
<span data-ttu-id="add05-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add05-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add05-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add05-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="add05-131">INPUTS</span></span>

### <span data-ttu-id="add05-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="add05-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="add05-133">System.String</span><span class="sxs-lookup"><span data-stu-id="add05-133">System.String</span></span>

## <span data-ttu-id="add05-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="add05-134">OUTPUTS</span></span>

### <span data-ttu-id="add05-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="add05-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="add05-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="add05-136">NOTES</span></span>

## <span data-ttu-id="add05-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="add05-137">RELATED LINKS</span></span>
