---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: aa51001163e4559dd0d3ef7edfb48abd3448c0b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894293"
---
# <span data-ttu-id="bff48-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="bff48-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="bff48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bff48-102">SYNOPSIS</span></span>
<span data-ttu-id="bff48-103">Wyświetla listę wszystkich certyfikatów lub określony certyfikat zawarty w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="bff48-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="bff48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bff48-104">SYNTAX</span></span>

### <span data-ttu-id="bff48-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bff48-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bff48-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bff48-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bff48-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bff48-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bff48-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bff48-108">DESCRIPTION</span></span>
<span data-ttu-id="bff48-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="bff48-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="bff48-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bff48-110">EXAMPLES</span></span>

### <span data-ttu-id="bff48-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bff48-111">Example 1</span></span>
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

<span data-ttu-id="bff48-112">Pokazywanie szczegółów dotyczących "elementu webcertificate" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="bff48-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="bff48-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bff48-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="bff48-114">Lista wszystkich certyfikatów w "myiotdps" przy użyciu rurociągu.</span><span class="sxs-lookup"><span data-stu-id="bff48-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="bff48-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bff48-115">PARAMETERS</span></span>

### <span data-ttu-id="bff48-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="bff48-116">-CertificateName</span></span>
<span data-ttu-id="bff48-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="bff48-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="bff48-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff48-118">-DefaultProfile</span></span>
<span data-ttu-id="bff48-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bff48-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bff48-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="bff48-120">-DpsObject</span></span>
<span data-ttu-id="bff48-121">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="bff48-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="bff48-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bff48-122">-Name</span></span>
<span data-ttu-id="bff48-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="bff48-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="bff48-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff48-124">-ResourceGroupName</span></span>
<span data-ttu-id="bff48-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bff48-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bff48-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bff48-126">-ResourceId</span></span>
<span data-ttu-id="bff48-127">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="bff48-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="bff48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff48-128">CommonParameters</span></span>
<span data-ttu-id="bff48-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff48-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff48-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff48-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bff48-131">INPUTS</span></span>

### <span data-ttu-id="bff48-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="bff48-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="bff48-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bff48-133">System.String</span></span>

## <span data-ttu-id="bff48-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bff48-134">OUTPUTS</span></span>

### <span data-ttu-id="bff48-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="bff48-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="bff48-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bff48-136">NOTES</span></span>

## <span data-ttu-id="bff48-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bff48-137">RELATED LINKS</span></span>
