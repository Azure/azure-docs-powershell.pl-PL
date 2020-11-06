---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 59445c2e162a7cbfce5cff26bac91d133c8928a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527953"
---
# <span data-ttu-id="df9cf-101">New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="df9cf-101">New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="df9cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="df9cf-103">Generuj kod weryfikacyjny certyfikatu usługi inicjowania obsługi urządzenia centrum usług Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="df9cf-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df9cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df9cf-104">SYNTAX</span></span>

### <span data-ttu-id="df9cf-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df9cf-105">ResourceSet (Default)</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String>
 [-Name] <String> [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df9cf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="df9cf-106">InputObjectSet</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df9cf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df9cf-107">ResourceIdSet</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df9cf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="df9cf-108">DESCRIPTION</span></span>
<span data-ttu-id="df9cf-109">Ten kod weryfikacyjny służy do dokończenia etapu posiadania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="df9cf-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="df9cf-110">Użyj tego kodu weryfikacyjnego jako CN nowego certyfikatu podpisanego kluczem prywatnym certyfikaty główne.</span><span class="sxs-lookup"><span data-stu-id="df9cf-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="df9cf-111">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w usłudze dostarczania urządzeń centrum usług Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="df9cf-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="df9cf-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df9cf-112">EXAMPLES</span></span>

### <span data-ttu-id="df9cf-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df9cf-113">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="df9cf-114">Wygeneruj kod weryfikacyjny dla "moje świadectwo".</span><span class="sxs-lookup"><span data-stu-id="df9cf-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="df9cf-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="df9cf-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzureRmIoTDpsCVC

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

<span data-ttu-id="df9cf-116">Wygeneruj kod weryfikacyjny dla "mój certyfikat" przy użyciu rurociągu.</span><span class="sxs-lookup"><span data-stu-id="df9cf-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="df9cf-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df9cf-117">PARAMETERS</span></span>

### <span data-ttu-id="df9cf-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="df9cf-118">-CertificateName</span></span>
<span data-ttu-id="df9cf-119">Nazwa certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="df9cf-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="df9cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9cf-120">-DefaultProfile</span></span>
<span data-ttu-id="df9cf-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df9cf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df9cf-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="df9cf-122">-Etag</span></span>
<span data-ttu-id="df9cf-123">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="df9cf-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="df9cf-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="df9cf-124">-InputObject</span></span>
<span data-ttu-id="df9cf-125">Obiekt certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="df9cf-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="df9cf-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df9cf-126">-Name</span></span>
<span data-ttu-id="df9cf-127">Nazwa usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="df9cf-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="df9cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df9cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="df9cf-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="df9cf-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="df9cf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df9cf-130">-ResourceId</span></span>
<span data-ttu-id="df9cf-131">Identyfikator zasobu certyfikatu usługi dostarczania urządzeń IoT</span><span class="sxs-lookup"><span data-stu-id="df9cf-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="df9cf-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df9cf-132">-Confirm</span></span>
<span data-ttu-id="df9cf-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df9cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df9cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df9cf-134">-WhatIf</span></span>
<span data-ttu-id="df9cf-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df9cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df9cf-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="df9cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df9cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9cf-137">CommonParameters</span></span>
<span data-ttu-id="df9cf-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df9cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9cf-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df9cf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9cf-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df9cf-140">INPUTS</span></span>

### <span data-ttu-id="df9cf-141">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="df9cf-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="df9cf-142">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="df9cf-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="df9cf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="df9cf-143">System.String</span></span>

## <span data-ttu-id="df9cf-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df9cf-144">OUTPUTS</span></span>

### <span data-ttu-id="df9cf-145">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="df9cf-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="df9cf-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df9cf-146">NOTES</span></span>

## <span data-ttu-id="df9cf-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df9cf-147">RELATED LINKS</span></span>
