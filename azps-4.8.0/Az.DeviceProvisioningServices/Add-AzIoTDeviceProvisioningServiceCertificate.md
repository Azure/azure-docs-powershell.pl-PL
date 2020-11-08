---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062775"
---
# <span data-ttu-id="6aaaf-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="6aaaf-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="6aaaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aaaf-102">SYNOPSIS</span></span>
<span data-ttu-id="6aaaf-103">Tworzenie/aktualizowanie certyfikatu usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6aaaf-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="6aaaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aaaf-104">SYNTAX</span></span>

### <span data-ttu-id="6aaaf-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6aaaf-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aaaf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6aaaf-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aaaf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6aaaf-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6aaaf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6aaaf-108">DESCRIPTION</span></span>
<span data-ttu-id="6aaaf-109">Wysyła nowy certyfikat lub zamienia istniejący certyfikat na taką samą nazwę.</span><span class="sxs-lookup"><span data-stu-id="6aaaf-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="6aaaf-110">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="6aaaf-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="6aaaf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aaaf-111">EXAMPLES</span></span>

### <span data-ttu-id="6aaaf-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6aaaf-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="6aaaf-113">Przekazywanie pliku CER certyfikatu urzędu certyfikacji do usługi dostarczania urządzeń centrum usługi Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="6aaaf-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="6aaaf-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6aaaf-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

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

<span data-ttu-id="6aaaf-115">Aktualizuje certyfikat urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług IoT, przekazując nowy plik CER.</span><span class="sxs-lookup"><span data-stu-id="6aaaf-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="6aaaf-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aaaf-116">PARAMETERS</span></span>

### <span data-ttu-id="6aaaf-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="6aaaf-117">-CertificateName</span></span>
<span data-ttu-id="6aaaf-118">Nazwa certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="6aaaf-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="6aaaf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aaaf-119">-DefaultProfile</span></span>
<span data-ttu-id="6aaaf-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6aaaf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aaaf-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="6aaaf-121">-Etag</span></span>
<span data-ttu-id="6aaaf-122">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="6aaaf-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="6aaaf-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6aaaf-123">-InputObject</span></span>
<span data-ttu-id="6aaaf-124">Obiekt certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="6aaaf-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="6aaaf-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6aaaf-125">-Name</span></span>
<span data-ttu-id="6aaaf-126">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="6aaaf-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6aaaf-127">-Path</span><span class="sxs-lookup"><span data-stu-id="6aaaf-127">-Path</span></span>
<span data-ttu-id="6aaaf-128">Reprezentacja Base-64 — ścieżka pliku lub pliku PEM z certyfikatem x509. cer</span><span class="sxs-lookup"><span data-stu-id="6aaaf-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="6aaaf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aaaf-129">-ResourceGroupName</span></span>
<span data-ttu-id="6aaaf-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6aaaf-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6aaaf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6aaaf-131">-ResourceId</span></span>
<span data-ttu-id="6aaaf-132">Identyfikator zasobu certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="6aaaf-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="6aaaf-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6aaaf-133">-Confirm</span></span>
<span data-ttu-id="6aaaf-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aaaf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aaaf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aaaf-135">-WhatIf</span></span>
<span data-ttu-id="6aaaf-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aaaf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aaaf-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6aaaf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aaaf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aaaf-138">CommonParameters</span></span>
<span data-ttu-id="6aaaf-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aaaf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aaaf-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aaaf-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aaaf-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aaaf-141">INPUTS</span></span>

### <span data-ttu-id="6aaaf-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="6aaaf-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="6aaaf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6aaaf-143">System.String</span></span>

## <span data-ttu-id="6aaaf-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aaaf-144">OUTPUTS</span></span>

### <span data-ttu-id="6aaaf-145">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="6aaaf-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="6aaaf-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aaaf-146">NOTES</span></span>

## <span data-ttu-id="6aaaf-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aaaf-147">RELATED LINKS</span></span>
