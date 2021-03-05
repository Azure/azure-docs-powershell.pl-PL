---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 5e887dc2f608dd7e26c05e3b7ca73036efe2595a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004097"
---
# <span data-ttu-id="8bc36-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="8bc36-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="8bc36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bc36-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc36-103">Sprawdza certyfikat usługi Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="8bc36-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="8bc36-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8bc36-104">SYNTAX</span></span>

### <span data-ttu-id="8bc36-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8bc36-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bc36-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8bc36-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc36-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8bc36-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bc36-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8bc36-108">DESCRIPTION</span></span>
<span data-ttu-id="8bc36-109">Weryfikuje certyfikat, przesyłając certyfikat weryfikacji zawierający kod weryfikacyjny uzyskany przez polecenie cmdlet Get-AzIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="8bc36-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="8bc36-110">Jest to ostatni krok w procesie dowodu posiadania.</span><span class="sxs-lookup"><span data-stu-id="8bc36-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="8bc36-111">Aby uzyskać szczegółowe objaśnienie certyfikatów urzędu certyfikacji w centrum Azure IoT Hub, zobacz https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="8bc36-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="8bc36-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8bc36-112">EXAMPLES</span></span>

### <span data-ttu-id="8bc36-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8bc36-113">Example 1</span></span>
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

<span data-ttu-id="8bc36-114">Weryfikuje własność klucza prywatnego MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="8bc36-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="8bc36-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bc36-115">PARAMETERS</span></span>

### <span data-ttu-id="8bc36-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="8bc36-116">-CertificateName</span></span>
<span data-ttu-id="8bc36-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="8bc36-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="8bc36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc36-118">-DefaultProfile</span></span>
<span data-ttu-id="8bc36-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc36-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bc36-120">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="8bc36-120">-Etag</span></span>
<span data-ttu-id="8bc36-121">Etag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="8bc36-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="8bc36-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bc36-122">-InputObject</span></span>
<span data-ttu-id="8bc36-123">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="8bc36-123">Certificate Object</span></span>

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

### <span data-ttu-id="8bc36-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8bc36-124">-Name</span></span>
<span data-ttu-id="8bc36-125">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="8bc36-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8bc36-126">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="8bc36-126">-Path</span></span>
<span data-ttu-id="8bc36-127">Base-64 representation of X509 certificate .cer file or .pem file path.</span><span class="sxs-lookup"><span data-stu-id="8bc36-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="8bc36-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc36-128">-ResourceGroupName</span></span>
<span data-ttu-id="8bc36-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8bc36-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8bc36-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bc36-130">-ResourceId</span></span>
<span data-ttu-id="8bc36-131">Identyfikator zasobu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="8bc36-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="8bc36-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bc36-132">-Confirm</span></span>
<span data-ttu-id="8bc36-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8bc36-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc36-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc36-134">-WhatIf</span></span>
<span data-ttu-id="8bc36-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc36-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bc36-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8bc36-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bc36-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc36-137">CommonParameters</span></span>
<span data-ttu-id="8bc36-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc36-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc36-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc36-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc36-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bc36-140">INPUTS</span></span>

### <span data-ttu-id="8bc36-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="8bc36-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="8bc36-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8bc36-142">System.String</span></span>

## <span data-ttu-id="8bc36-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bc36-143">OUTPUTS</span></span>

### <span data-ttu-id="8bc36-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="8bc36-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="8bc36-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8bc36-145">NOTES</span></span>

## <span data-ttu-id="8bc36-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bc36-146">RELATED LINKS</span></span>
