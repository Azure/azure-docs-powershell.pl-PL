---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 659998a6a82c08ab57697767276e2357002a4182
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709876"
---
# <span data-ttu-id="a3007-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="a3007-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="a3007-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3007-102">SYNOPSIS</span></span>
<span data-ttu-id="a3007-103">Sprawdź certyfikat usługi dostarczania urządzeń centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="a3007-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="a3007-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3007-104">SYNTAX</span></span>

### <span data-ttu-id="a3007-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a3007-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3007-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a3007-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3007-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a3007-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3007-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a3007-108">DESCRIPTION</span></span>
<span data-ttu-id="a3007-109">Zweryfikuj certyfikat, przekazując certyfikat weryfikacji zawierający kod weryfikacyjny uzyskany przez połączenie z kodem generowania-weryfikacji.</span><span class="sxs-lookup"><span data-stu-id="a3007-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="a3007-110">Jest to ostatni krok w celu poświadczania procesu posiadania.</span><span class="sxs-lookup"><span data-stu-id="a3007-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="a3007-111">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="a3007-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="a3007-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3007-112">EXAMPLES</span></span>

### <span data-ttu-id="a3007-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3007-113">Example 1</span></span>
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

<span data-ttu-id="a3007-114">Sprawdź własność klucza prywatnego "mój certyfikat".</span><span class="sxs-lookup"><span data-stu-id="a3007-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="a3007-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a3007-115">Example 2</span></span>
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

<span data-ttu-id="a3007-116">Sprawdź własność klucza prywatnego "mój certyfikat" przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="a3007-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="a3007-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3007-117">PARAMETERS</span></span>

### <span data-ttu-id="a3007-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a3007-118">-CertificateName</span></span>
<span data-ttu-id="a3007-119">Nazwa certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a3007-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="a3007-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3007-120">-DefaultProfile</span></span>
<span data-ttu-id="a3007-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3007-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3007-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="a3007-122">-Etag</span></span>
<span data-ttu-id="a3007-123">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="a3007-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="a3007-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3007-124">-InputObject</span></span>
<span data-ttu-id="a3007-125">Obiekt certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a3007-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="a3007-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3007-126">-Name</span></span>
<span data-ttu-id="a3007-127">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a3007-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a3007-128">-Path</span><span class="sxs-lookup"><span data-stu-id="a3007-128">-Path</span></span>
<span data-ttu-id="a3007-129">Reprezentacja Base-64 — ścieżka pliku lub pliku PEM z certyfikatem x509. cer</span><span class="sxs-lookup"><span data-stu-id="a3007-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="a3007-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3007-130">-ResourceGroupName</span></span>
<span data-ttu-id="a3007-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a3007-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a3007-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3007-132">-ResourceId</span></span>
<span data-ttu-id="a3007-133">Identyfikator zasobu certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="a3007-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="a3007-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3007-134">-Confirm</span></span>
<span data-ttu-id="a3007-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3007-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3007-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3007-136">-WhatIf</span></span>
<span data-ttu-id="a3007-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3007-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3007-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3007-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3007-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3007-139">CommonParameters</span></span>
<span data-ttu-id="a3007-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3007-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3007-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3007-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3007-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3007-142">INPUTS</span></span>

### <span data-ttu-id="a3007-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="a3007-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="a3007-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a3007-144">System.String</span></span>

## <span data-ttu-id="a3007-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3007-145">OUTPUTS</span></span>

### <span data-ttu-id="a3007-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="a3007-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="a3007-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3007-147">NOTES</span></span>

## <span data-ttu-id="a3007-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3007-148">RELATED LINKS</span></span>
