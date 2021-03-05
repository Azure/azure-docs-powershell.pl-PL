---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 05c275448ffecb006c8a23de36fcd7f33397af4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010490"
---
# <span data-ttu-id="847c9-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="847c9-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="847c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="847c9-102">SYNOPSIS</span></span>
<span data-ttu-id="847c9-103">Utwórz/zaktualizuj certyfikat usługi inicjowania obsługi urządzeń w centrum Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="847c9-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="847c9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="847c9-104">SYNTAX</span></span>

### <span data-ttu-id="847c9-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="847c9-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="847c9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="847c9-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="847c9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="847c9-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="847c9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="847c9-108">DESCRIPTION</span></span>
<span data-ttu-id="847c9-109">Przekazanie nowego certyfikatu lub zastąpienie istniejącego certyfikatu taką samą nazwą.</span><span class="sxs-lookup"><span data-stu-id="847c9-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="847c9-110">Aby uzyskać szczegółowe objaśnienie certyfikatów urzędu certyfikacji w usłudze inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates zobacz.</span><span class="sxs-lookup"><span data-stu-id="847c9-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="847c9-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="847c9-111">EXAMPLES</span></span>

### <span data-ttu-id="847c9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="847c9-112">Example 1</span></span>
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

<span data-ttu-id="847c9-113">Przekaż plik CER certyfikatu urzędu certyfikacji do usługi inicjowania obsługi administracyjnej urządzeń w centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="847c9-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="847c9-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="847c9-114">Example 2</span></span>
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

<span data-ttu-id="847c9-115">Aktualizuje certyfikat urzędu certyfikacji w usłudze inicjowania obsługi urządzeń centrum IoT, przesyłając nowy plik CER.</span><span class="sxs-lookup"><span data-stu-id="847c9-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="847c9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="847c9-116">PARAMETERS</span></span>

### <span data-ttu-id="847c9-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="847c9-117">-CertificateName</span></span>
<span data-ttu-id="847c9-118">Nazwa certyfikatu usługi inicjowania obsługi administracyjnej urządzenia Iot</span><span class="sxs-lookup"><span data-stu-id="847c9-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="847c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="847c9-119">-DefaultProfile</span></span>
<span data-ttu-id="847c9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="847c9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="847c9-121">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="847c9-121">-Etag</span></span>
<span data-ttu-id="847c9-122">Etag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="847c9-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="847c9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="847c9-123">-InputObject</span></span>
<span data-ttu-id="847c9-124">Obiekt certyfikatu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="847c9-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="847c9-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="847c9-125">-Name</span></span>
<span data-ttu-id="847c9-126">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="847c9-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="847c9-127">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="847c9-127">-Path</span></span>
<span data-ttu-id="847c9-128">Base-64 representation of X509 certificate .cer file or .pem file path</span><span class="sxs-lookup"><span data-stu-id="847c9-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="847c9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="847c9-129">-ResourceGroupName</span></span>
<span data-ttu-id="847c9-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="847c9-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="847c9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="847c9-131">-ResourceId</span></span>
<span data-ttu-id="847c9-132">Identyfikator zasobu certyfikatu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="847c9-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="847c9-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="847c9-133">-Confirm</span></span>
<span data-ttu-id="847c9-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="847c9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="847c9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="847c9-135">-WhatIf</span></span>
<span data-ttu-id="847c9-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="847c9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="847c9-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="847c9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="847c9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="847c9-138">CommonParameters</span></span>
<span data-ttu-id="847c9-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="847c9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="847c9-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="847c9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="847c9-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="847c9-141">INPUTS</span></span>

### <span data-ttu-id="847c9-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="847c9-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="847c9-143">System.String</span><span class="sxs-lookup"><span data-stu-id="847c9-143">System.String</span></span>

## <span data-ttu-id="847c9-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="847c9-144">OUTPUTS</span></span>

### <span data-ttu-id="847c9-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="847c9-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="847c9-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="847c9-146">NOTES</span></span>

## <span data-ttu-id="847c9-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="847c9-147">RELATED LINKS</span></span>
