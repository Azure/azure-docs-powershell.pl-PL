---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180755"
---
# <span data-ttu-id="bb8b3-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="bb8b3-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="bb8b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8b3-103">Wygeneruj kod weryfikacyjny dla certyfikatu usługi inicjowania obsługi urządzeń w centrum Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="bb8b3-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="bb8b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb8b3-104">SYNTAX</span></span>

### <span data-ttu-id="bb8b3-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bb8b3-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb8b3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb8b3-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb8b3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bb8b3-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb8b3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb8b3-108">DESCRIPTION</span></span>
<span data-ttu-id="bb8b3-109">Ten kod weryfikacyjny służy do ukończenia dowodu posiadania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bb8b3-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="bb8b3-110">Użyj tego kodu weryfikacyjnego jako kodu CN nowego certyfikatu podpisanego za pomocą klucza prywatnego certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="bb8b3-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="bb8b3-111">Aby uzyskać szczegółowe objaśnienie certyfikatów urzędu certyfikacji w usłudze inicjowania obsługi urządzeń w centrum IoT Azure, https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates zobacz.</span><span class="sxs-lookup"><span data-stu-id="bb8b3-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="bb8b3-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb8b3-112">EXAMPLES</span></span>

### <span data-ttu-id="bb8b3-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb8b3-113">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="bb8b3-114">Wygeneruj kod weryfikacyjny dla "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="bb8b3-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="bb8b3-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bb8b3-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="bb8b3-116">Wygeneruj kod weryfikacyjny dla "mycertificate" przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="bb8b3-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="bb8b3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb8b3-117">PARAMETERS</span></span>

### <span data-ttu-id="bb8b3-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="bb8b3-118">-CertificateName</span></span>
<span data-ttu-id="bb8b3-119">Nazwa certyfikatu usługi inicjowania obsługi administracyjnej urządzenia Iot</span><span class="sxs-lookup"><span data-stu-id="bb8b3-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="bb8b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8b3-120">-DefaultProfile</span></span>
<span data-ttu-id="bb8b3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb8b3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb8b3-122">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="bb8b3-122">-Etag</span></span>
<span data-ttu-id="bb8b3-123">Etag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="bb8b3-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="bb8b3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb8b3-124">-InputObject</span></span>
<span data-ttu-id="bb8b3-125">Obiekt certyfikatu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="bb8b3-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="bb8b3-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bb8b3-126">-Name</span></span>
<span data-ttu-id="bb8b3-127">Nazwa usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="bb8b3-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="bb8b3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb8b3-128">-ResourceGroupName</span></span>
<span data-ttu-id="bb8b3-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bb8b3-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bb8b3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb8b3-130">-ResourceId</span></span>
<span data-ttu-id="bb8b3-131">Identyfikator zasobu certyfikatu usługi inicjowania obsługi urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="bb8b3-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="bb8b3-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb8b3-132">-Confirm</span></span>
<span data-ttu-id="bb8b3-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb8b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb8b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb8b3-134">-WhatIf</span></span>
<span data-ttu-id="bb8b3-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb8b3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb8b3-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb8b3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb8b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8b3-137">CommonParameters</span></span>
<span data-ttu-id="bb8b3-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb8b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8b3-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb8b3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8b3-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb8b3-140">INPUTS</span></span>

### <span data-ttu-id="bb8b3-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="bb8b3-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="bb8b3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="bb8b3-142">System.String</span></span>

## <span data-ttu-id="bb8b3-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb8b3-143">OUTPUTS</span></span>

### <span data-ttu-id="bb8b3-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="bb8b3-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="bb8b3-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb8b3-145">NOTES</span></span>

## <span data-ttu-id="bb8b3-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb8b3-146">RELATED LINKS</span></span>
