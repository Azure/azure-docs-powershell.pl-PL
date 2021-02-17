---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 9b995a0ed80bf32b770fe6b157a283534d01f743
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196371"
---
# <span data-ttu-id="09f9c-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="09f9c-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="09f9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="09f9c-103">Zweryfikuj certyfikat usługi inicjowania obsługi urządzeń w centrum Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="09f9c-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="09f9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09f9c-104">SYNTAX</span></span>

### <span data-ttu-id="09f9c-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="09f9c-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09f9c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="09f9c-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09f9c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="09f9c-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09f9c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="09f9c-108">DESCRIPTION</span></span>
<span data-ttu-id="09f9c-109">Zweryfikuj certyfikat, przesyłając certyfikat weryfikacji zawierający kod weryfikacyjny uzyskany przez wywoływanie kodu weryfikacji wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="09f9c-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="09f9c-110">Jest to ostatni krok w procesie dowodu posiadania.</span><span class="sxs-lookup"><span data-stu-id="09f9c-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="09f9c-111">Aby uzyskać szczegółowe objaśnienie certyfikatów urzędu certyfikacji w usłudze inicjowania obsługi urządzeń w centrum Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="09f9c-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="09f9c-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09f9c-112">EXAMPLES</span></span>

### <span data-ttu-id="09f9c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09f9c-113">Example 1</span></span>
```
PS C:\> Set-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="09f9c-114">Weryfikuj własność klucza prywatnego "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="09f9c-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="09f9c-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="09f9c-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="09f9c-116">Weryfikuj własność klucza prywatnego "mycertificate" przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="09f9c-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="09f9c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09f9c-117">PARAMETERS</span></span>

### <span data-ttu-id="09f9c-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="09f9c-118">-CertificateName</span></span>
<span data-ttu-id="09f9c-119">Nazwa certyfikatu usługi inicjowania obsługi administracyjnej urządzenia Iot</span><span class="sxs-lookup"><span data-stu-id="09f9c-119">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f9c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f9c-120">-DefaultProfile</span></span>
<span data-ttu-id="09f9c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="09f9c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09f9c-122">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="09f9c-122">-Etag</span></span>
<span data-ttu-id="09f9c-123">Etag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="09f9c-123">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f9c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09f9c-124">-InputObject</span></span>
<span data-ttu-id="09f9c-125">Obiekt certyfikatu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="09f9c-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="09f9c-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="09f9c-126">-Name</span></span>
<span data-ttu-id="09f9c-127">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="09f9c-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="09f9c-128">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="09f9c-128">-Path</span></span>
<span data-ttu-id="09f9c-129">Base-64 representation of X509 certificate .cer file or .pem file path</span><span class="sxs-lookup"><span data-stu-id="09f9c-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="09f9c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f9c-130">-ResourceGroupName</span></span>
<span data-ttu-id="09f9c-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="09f9c-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="09f9c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09f9c-132">-ResourceId</span></span>
<span data-ttu-id="09f9c-133">Identyfikator zasobu certyfikatu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="09f9c-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="09f9c-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09f9c-134">-Confirm</span></span>
<span data-ttu-id="09f9c-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09f9c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09f9c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09f9c-136">-WhatIf</span></span>
<span data-ttu-id="09f9c-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09f9c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09f9c-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="09f9c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09f9c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f9c-139">CommonParameters</span></span>
<span data-ttu-id="09f9c-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f9c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f9c-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f9c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f9c-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09f9c-142">INPUTS</span></span>

### <span data-ttu-id="09f9c-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="09f9c-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="09f9c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="09f9c-144">System.String</span></span>

## <span data-ttu-id="09f9c-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09f9c-145">OUTPUTS</span></span>

### <span data-ttu-id="09f9c-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="09f9c-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="09f9c-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09f9c-147">NOTES</span></span>

## <span data-ttu-id="09f9c-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09f9c-148">RELATED LINKS</span></span>
