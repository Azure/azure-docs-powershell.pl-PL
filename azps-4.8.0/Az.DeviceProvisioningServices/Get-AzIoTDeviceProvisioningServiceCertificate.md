---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: aa51001163e4559dd0d3ef7edfb48abd3448c0b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062768"
---
# <span data-ttu-id="3ded0-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="3ded0-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="3ded0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ded0-102">SYNOPSIS</span></span>
<span data-ttu-id="3ded0-103">Wyświetla listę wszystkich certyfikatów lub określony certyfikat zawarty w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="3ded0-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="3ded0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ded0-104">SYNTAX</span></span>

### <span data-ttu-id="3ded0-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3ded0-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ded0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3ded0-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ded0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3ded0-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ded0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3ded0-108">DESCRIPTION</span></span>
<span data-ttu-id="3ded0-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="3ded0-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="3ded0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ded0-110">EXAMPLES</span></span>

### <span data-ttu-id="3ded0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ded0-111">Example 1</span></span>
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

<span data-ttu-id="3ded0-112">Pokazywanie szczegółów dotyczących "elementu webcertificate" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="3ded0-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="3ded0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3ded0-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="3ded0-114">Lista wszystkich certyfikatów w "myiotdps" przy użyciu rurociągu.</span><span class="sxs-lookup"><span data-stu-id="3ded0-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="3ded0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ded0-115">PARAMETERS</span></span>

### <span data-ttu-id="3ded0-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="3ded0-116">-CertificateName</span></span>
<span data-ttu-id="3ded0-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="3ded0-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="3ded0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ded0-118">-DefaultProfile</span></span>
<span data-ttu-id="3ded0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ded0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ded0-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="3ded0-120">-DpsObject</span></span>
<span data-ttu-id="3ded0-121">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3ded0-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="3ded0-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3ded0-122">-Name</span></span>
<span data-ttu-id="3ded0-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3ded0-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3ded0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ded0-124">-ResourceGroupName</span></span>
<span data-ttu-id="3ded0-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3ded0-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3ded0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ded0-126">-ResourceId</span></span>
<span data-ttu-id="3ded0-127">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="3ded0-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3ded0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ded0-128">CommonParameters</span></span>
<span data-ttu-id="3ded0-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ded0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ded0-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ded0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ded0-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ded0-131">INPUTS</span></span>

### <span data-ttu-id="3ded0-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3ded0-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="3ded0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3ded0-133">System.String</span></span>

## <span data-ttu-id="3ded0-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ded0-134">OUTPUTS</span></span>

### <span data-ttu-id="3ded0-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="3ded0-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="3ded0-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ded0-136">NOTES</span></span>

## <span data-ttu-id="3ded0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ded0-137">RELATED LINKS</span></span>
