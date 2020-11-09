---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 78881a7bd82aedeed4dca2a7ee08ea40812a0b05
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304680"
---
# <span data-ttu-id="b8f11-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="b8f11-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="b8f11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8f11-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f11-103">Weryfikuje certyfikat centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="b8f11-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="b8f11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8f11-104">SYNTAX</span></span>

### <span data-ttu-id="b8f11-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b8f11-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8f11-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8f11-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8f11-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b8f11-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8f11-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b8f11-108">DESCRIPTION</span></span>
<span data-ttu-id="b8f11-109">Weryfikuje certyfikat, przekazując certyfikat weryfikacji zawierający kod weryfikacyjny otrzymany za pomocą polecenia cmdlet Get-AzIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="b8f11-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="b8f11-110">Jest to ostatni krok w celu poświadczania procesu posiadania.</span><span class="sxs-lookup"><span data-stu-id="b8f11-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="b8f11-111">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="b8f11-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="b8f11-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8f11-112">EXAMPLES</span></span>

### <span data-ttu-id="b8f11-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8f11-113">Example 1</span></span>
```
PS C:\> Set-AzIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="b8f11-114">Weryfikuje własność prywatnego klucza moja certyfikat.</span><span class="sxs-lookup"><span data-stu-id="b8f11-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="b8f11-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8f11-115">PARAMETERS</span></span>

### <span data-ttu-id="b8f11-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b8f11-116">-CertificateName</span></span>
<span data-ttu-id="b8f11-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b8f11-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="b8f11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8f11-118">-DefaultProfile</span></span>
<span data-ttu-id="b8f11-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8f11-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8f11-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="b8f11-120">-Etag</span></span>
<span data-ttu-id="b8f11-121">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b8f11-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="b8f11-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b8f11-122">-InputObject</span></span>
<span data-ttu-id="b8f11-123">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="b8f11-123">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8f11-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8f11-124">-Name</span></span>
<span data-ttu-id="b8f11-125">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="b8f11-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8f11-126">-Path</span><span class="sxs-lookup"><span data-stu-id="b8f11-126">-Path</span></span>
<span data-ttu-id="b8f11-127">Reprezentacja Base-64 — ścieżka pliku certyfikatu x509. cer lub plik PEM.</span><span class="sxs-lookup"><span data-stu-id="b8f11-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="b8f11-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8f11-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8f11-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b8f11-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8f11-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8f11-130">-ResourceId</span></span>
<span data-ttu-id="b8f11-131">Identyfikator zasobu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b8f11-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="b8f11-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8f11-132">-Confirm</span></span>
<span data-ttu-id="b8f11-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8f11-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8f11-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8f11-134">-WhatIf</span></span>
<span data-ttu-id="b8f11-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8f11-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8f11-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b8f11-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8f11-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f11-137">CommonParameters</span></span>
<span data-ttu-id="b8f11-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8f11-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f11-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8f11-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f11-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8f11-140">INPUTS</span></span>

### <span data-ttu-id="b8f11-141">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="b8f11-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="b8f11-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b8f11-142">System.String</span></span>

## <span data-ttu-id="b8f11-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8f11-143">OUTPUTS</span></span>

### <span data-ttu-id="b8f11-144">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="b8f11-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="b8f11-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8f11-145">NOTES</span></span>

## <span data-ttu-id="b8f11-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8f11-146">RELATED LINKS</span></span>
