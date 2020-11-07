---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 098689074debe4b9cf5be4d682023186b123d504
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719131"
---
# <span data-ttu-id="d4a92-101">Add-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="d4a92-101">Add-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="d4a92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4a92-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a92-103">Tworzenie/aktualizowanie certyfikatu usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="d4a92-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4a92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4a92-104">SYNTAX</span></span>

### <span data-ttu-id="d4a92-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d4a92-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a92-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4a92-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a92-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d4a92-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4a92-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d4a92-108">DESCRIPTION</span></span>
<span data-ttu-id="d4a92-109">Wysyła nowy certyfikat lub zamienia istniejący certyfikat na taką samą nazwę.</span><span class="sxs-lookup"><span data-stu-id="d4a92-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="d4a92-110">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="d4a92-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="d4a92-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4a92-111">EXAMPLES</span></span>

### <span data-ttu-id="d4a92-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4a92-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="d4a92-113">Przekazywanie pliku CER certyfikatu urzędu certyfikacji do usługi dostarczania urządzeń centrum usługi Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="d4a92-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="d4a92-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d4a92-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="d4a92-115">Aktualizuje certyfikat urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług IoT, przekazując nowy plik CER.</span><span class="sxs-lookup"><span data-stu-id="d4a92-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="d4a92-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4a92-116">PARAMETERS</span></span>

### <span data-ttu-id="d4a92-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d4a92-117">-CertificateName</span></span>
<span data-ttu-id="d4a92-118">Nazwa certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d4a92-118">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a92-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a92-119">-DefaultProfile</span></span>
<span data-ttu-id="d4a92-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a92-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a92-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="d4a92-121">-Etag</span></span>
<span data-ttu-id="d4a92-122">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="d4a92-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="d4a92-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4a92-123">-InputObject</span></span>
<span data-ttu-id="d4a92-124">Obiekt certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d4a92-124">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a92-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4a92-125">-Name</span></span>
<span data-ttu-id="d4a92-126">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d4a92-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d4a92-127">-Path</span><span class="sxs-lookup"><span data-stu-id="d4a92-127">-Path</span></span>
<span data-ttu-id="d4a92-128">Reprezentacja Base-64 — ścieżka pliku lub pliku PEM z certyfikatem x509. cer</span><span class="sxs-lookup"><span data-stu-id="d4a92-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a92-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a92-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4a92-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d4a92-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d4a92-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4a92-131">-ResourceId</span></span>
<span data-ttu-id="d4a92-132">Identyfikator zasobu certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="d4a92-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="d4a92-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4a92-133">-Confirm</span></span>
<span data-ttu-id="d4a92-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a92-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a92-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a92-135">-WhatIf</span></span>
<span data-ttu-id="d4a92-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a92-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4a92-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4a92-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a92-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a92-138">CommonParameters</span></span>
<span data-ttu-id="d4a92-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a92-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a92-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a92-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a92-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4a92-141">INPUTS</span></span>

### <span data-ttu-id="d4a92-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d4a92-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="d4a92-143">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4a92-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d4a92-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d4a92-144">System.String</span></span>

## <span data-ttu-id="d4a92-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4a92-145">OUTPUTS</span></span>

### <span data-ttu-id="d4a92-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d4a92-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="d4a92-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4a92-147">NOTES</span></span>

## <span data-ttu-id="d4a92-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4a92-148">RELATED LINKS</span></span>
