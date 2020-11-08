---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 6d77bcc6d940c5891b4fc06875dc353af5f75939
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053224"
---
# <span data-ttu-id="800cf-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="800cf-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="800cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="800cf-102">SYNOPSIS</span></span>
<span data-ttu-id="800cf-103">Utwórz/zaktualizuj certyfikat centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="800cf-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="800cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="800cf-104">SYNTAX</span></span>

### <span data-ttu-id="800cf-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="800cf-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="800cf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="800cf-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="800cf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="800cf-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="800cf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="800cf-108">DESCRIPTION</span></span>
<span data-ttu-id="800cf-109">Wysyła nowy certyfikat lub zamienia istniejący certyfikat na taką samą nazwę.</span><span class="sxs-lookup"><span data-stu-id="800cf-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="800cf-110">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="800cf-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="800cf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="800cf-111">EXAMPLES</span></span>

### <span data-ttu-id="800cf-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="800cf-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="800cf-113">Umożliwia przekazywanie pliku CER certyfikatu urzędu certyfikacji do centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="800cf-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="800cf-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="800cf-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="800cf-115">Aktualizuje certyfikat urzędu certyfikacji w centrum IoT, przekazując nowy plik CER.</span><span class="sxs-lookup"><span data-stu-id="800cf-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="800cf-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="800cf-116">PARAMETERS</span></span>

### <span data-ttu-id="800cf-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="800cf-117">-CertificateName</span></span>
<span data-ttu-id="800cf-118">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="800cf-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="800cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800cf-119">-DefaultProfile</span></span>
<span data-ttu-id="800cf-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="800cf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="800cf-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="800cf-121">-Etag</span></span>
<span data-ttu-id="800cf-122">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="800cf-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="800cf-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="800cf-123">-InputObject</span></span>
<span data-ttu-id="800cf-124">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="800cf-124">Certificate Object</span></span>

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

### <span data-ttu-id="800cf-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="800cf-125">-Name</span></span>
<span data-ttu-id="800cf-126">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="800cf-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="800cf-127">-Path</span><span class="sxs-lookup"><span data-stu-id="800cf-127">-Path</span></span>
<span data-ttu-id="800cf-128">Reprezentacja Base-64 — ścieżka pliku certyfikatu x509. cer lub plik PEM.</span><span class="sxs-lookup"><span data-stu-id="800cf-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="800cf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="800cf-129">-ResourceGroupName</span></span>
<span data-ttu-id="800cf-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="800cf-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="800cf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="800cf-131">-ResourceId</span></span>
<span data-ttu-id="800cf-132">Identyfikator zasobu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="800cf-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="800cf-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="800cf-133">-Confirm</span></span>
<span data-ttu-id="800cf-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="800cf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="800cf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="800cf-135">-WhatIf</span></span>
<span data-ttu-id="800cf-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="800cf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="800cf-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="800cf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="800cf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800cf-138">CommonParameters</span></span>
<span data-ttu-id="800cf-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="800cf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800cf-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="800cf-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800cf-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="800cf-141">INPUTS</span></span>

### <span data-ttu-id="800cf-142">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="800cf-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="800cf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="800cf-143">System.String</span></span>

## <span data-ttu-id="800cf-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="800cf-144">OUTPUTS</span></span>

### <span data-ttu-id="800cf-145">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="800cf-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="800cf-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="800cf-146">NOTES</span></span>

## <span data-ttu-id="800cf-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="800cf-147">RELATED LINKS</span></span>
