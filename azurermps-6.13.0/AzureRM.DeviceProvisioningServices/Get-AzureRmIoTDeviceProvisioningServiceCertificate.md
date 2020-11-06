---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: c44e36a0aa08daf7e4a9ae9822f8a4be85db5d57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524434"
---
# <span data-ttu-id="a9794-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="a9794-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="a9794-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9794-102">SYNOPSIS</span></span>
<span data-ttu-id="a9794-103">Wyświetla listę wszystkich certyfikatów lub określony certyfikat zawarty w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="a9794-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9794-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9794-104">SYNTAX</span></span>

### <span data-ttu-id="a9794-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9794-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9794-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9794-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9794-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9794-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9794-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9794-108">DESCRIPTION</span></span>
<span data-ttu-id="a9794-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="a9794-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="a9794-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9794-110">EXAMPLES</span></span>

### <span data-ttu-id="a9794-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9794-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="a9794-112">Pokazywanie szczegółów dotyczących "elementu webcertificate" w usłudze dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="a9794-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="a9794-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a9794-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzureRmIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="a9794-114">Lista wszystkich certyfikatów w "myiotdps" przy użyciu rurociągu.</span><span class="sxs-lookup"><span data-stu-id="a9794-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="a9794-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9794-115">PARAMETERS</span></span>

### <span data-ttu-id="a9794-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a9794-116">-CertificateName</span></span>
<span data-ttu-id="a9794-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="a9794-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="a9794-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9794-118">-DefaultProfile</span></span>
<span data-ttu-id="a9794-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9794-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9794-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a9794-120">-DpsObject</span></span>
<span data-ttu-id="a9794-121">Obiekt usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a9794-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a9794-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9794-122">-Name</span></span>
<span data-ttu-id="a9794-123">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a9794-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a9794-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9794-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9794-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9794-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a9794-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9794-126">-ResourceId</span></span>
<span data-ttu-id="a9794-127">Identyfikator zasobu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a9794-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a9794-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9794-128">CommonParameters</span></span>
<span data-ttu-id="a9794-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9794-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9794-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9794-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9794-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9794-131">INPUTS</span></span>

### <span data-ttu-id="a9794-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a9794-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="a9794-133">Parametry: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a9794-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="a9794-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a9794-134">System.String</span></span>

## <span data-ttu-id="a9794-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9794-135">OUTPUTS</span></span>

### <span data-ttu-id="a9794-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="a9794-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="a9794-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9794-137">NOTES</span></span>

## <span data-ttu-id="a9794-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9794-138">RELATED LINKS</span></span>
