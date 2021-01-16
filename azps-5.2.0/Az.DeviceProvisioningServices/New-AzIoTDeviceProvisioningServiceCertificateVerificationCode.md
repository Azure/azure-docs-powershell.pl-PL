---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328739"
---
# <span data-ttu-id="2a0a4-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="2a0a4-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="2a0a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0a4-103">Generuj kod weryfikacyjny certyfikatu usługi inicjowania obsługi urządzenia centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="2a0a4-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="2a0a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a0a4-104">SYNTAX</span></span>

### <span data-ttu-id="2a0a4-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2a0a4-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a0a4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2a0a4-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a0a4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2a0a4-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a0a4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2a0a4-108">DESCRIPTION</span></span>
<span data-ttu-id="2a0a4-109">Ten kod weryfikacyjny służy do dokończenia etapu posiadania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="2a0a4-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="2a0a4-110">Użyj tego kodu weryfikacyjnego jako CN nowego certyfikatu podpisanego kluczem prywatnym certyfikaty główne.</span><span class="sxs-lookup"><span data-stu-id="2a0a4-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="2a0a4-111">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="2a0a4-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="2a0a4-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a0a4-112">EXAMPLES</span></span>

### <span data-ttu-id="2a0a4-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a0a4-113">Example 1</span></span>
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

<span data-ttu-id="2a0a4-114">Wygeneruj kod weryfikacyjny dla "moje świadectwo".</span><span class="sxs-lookup"><span data-stu-id="2a0a4-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="2a0a4-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2a0a4-115">Example 2</span></span>
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

<span data-ttu-id="2a0a4-116">Wygeneruj kod weryfikacyjny dla "mój certyfikat" przy użyciu rurociągu.</span><span class="sxs-lookup"><span data-stu-id="2a0a4-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="2a0a4-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a0a4-117">PARAMETERS</span></span>

### <span data-ttu-id="2a0a4-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2a0a4-118">-CertificateName</span></span>
<span data-ttu-id="2a0a4-119">Nazwa certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="2a0a4-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="2a0a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a0a4-120">-DefaultProfile</span></span>
<span data-ttu-id="2a0a4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0a4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a0a4-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="2a0a4-122">-Etag</span></span>
<span data-ttu-id="2a0a4-123">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="2a0a4-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="2a0a4-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2a0a4-124">-InputObject</span></span>
<span data-ttu-id="2a0a4-125">Obiekt certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="2a0a4-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="2a0a4-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a0a4-126">-Name</span></span>
<span data-ttu-id="2a0a4-127">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="2a0a4-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2a0a4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a0a4-128">-ResourceGroupName</span></span>
<span data-ttu-id="2a0a4-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2a0a4-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2a0a4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a0a4-130">-ResourceId</span></span>
<span data-ttu-id="2a0a4-131">Identyfikator zasobu certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="2a0a4-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="2a0a4-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a0a4-132">-Confirm</span></span>
<span data-ttu-id="2a0a4-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0a4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a0a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a0a4-134">-WhatIf</span></span>
<span data-ttu-id="2a0a4-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0a4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a0a4-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a0a4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a0a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0a4-137">CommonParameters</span></span>
<span data-ttu-id="2a0a4-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a0a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0a4-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a0a4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0a4-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a0a4-140">INPUTS</span></span>

### <span data-ttu-id="2a0a4-141">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="2a0a4-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="2a0a4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2a0a4-142">System.String</span></span>

## <span data-ttu-id="2a0a4-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a0a4-143">OUTPUTS</span></span>

### <span data-ttu-id="2a0a4-144">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="2a0a4-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="2a0a4-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a0a4-145">NOTES</span></span>

## <span data-ttu-id="2a0a4-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a0a4-146">RELATED LINKS</span></span>
