---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 6d77bcc6d940c5891b4fc06875dc353af5f75939
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188282"
---
# <span data-ttu-id="749eb-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="749eb-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="749eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="749eb-102">SYNOPSIS</span></span>
<span data-ttu-id="749eb-103">Utwórz/zaktualizuj certyfikat centrum IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="749eb-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="749eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="749eb-104">SYNTAX</span></span>

### <span data-ttu-id="749eb-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="749eb-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="749eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="749eb-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="749eb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="749eb-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="749eb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="749eb-108">DESCRIPTION</span></span>
<span data-ttu-id="749eb-109">Przekazanie nowego certyfikatu lub zastąpienie istniejącego certyfikatu taką samą nazwą.</span><span class="sxs-lookup"><span data-stu-id="749eb-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="749eb-110">Aby uzyskać szczegółowe objaśnienie certyfikatów urzędu certyfikacji w centrum Azure IoT Hub, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="749eb-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="749eb-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="749eb-111">EXAMPLES</span></span>

### <span data-ttu-id="749eb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="749eb-112">Example 1</span></span>
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

<span data-ttu-id="749eb-113">Przekazanie pliku certyfikatu certyfikacji CER do centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="749eb-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="749eb-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="749eb-114">Example 2</span></span>
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

<span data-ttu-id="749eb-115">Aktualizuje certyfikat urzędu certyfikacji w centrum IoT, przesyłając nowy plik CER.</span><span class="sxs-lookup"><span data-stu-id="749eb-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="749eb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="749eb-116">PARAMETERS</span></span>

### <span data-ttu-id="749eb-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="749eb-117">-CertificateName</span></span>
<span data-ttu-id="749eb-118">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="749eb-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="749eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="749eb-119">-DefaultProfile</span></span>
<span data-ttu-id="749eb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="749eb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="749eb-121">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="749eb-121">-Etag</span></span>
<span data-ttu-id="749eb-122">Etag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="749eb-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="749eb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="749eb-123">-InputObject</span></span>
<span data-ttu-id="749eb-124">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="749eb-124">Certificate Object</span></span>

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

### <span data-ttu-id="749eb-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="749eb-125">-Name</span></span>
<span data-ttu-id="749eb-126">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="749eb-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="749eb-127">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="749eb-127">-Path</span></span>
<span data-ttu-id="749eb-128">Base-64 representation of X509 certificate .cer file or .pem file path.</span><span class="sxs-lookup"><span data-stu-id="749eb-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="749eb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="749eb-129">-ResourceGroupName</span></span>
<span data-ttu-id="749eb-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="749eb-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="749eb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="749eb-131">-ResourceId</span></span>
<span data-ttu-id="749eb-132">Identyfikator zasobu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="749eb-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="749eb-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="749eb-133">-Confirm</span></span>
<span data-ttu-id="749eb-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="749eb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="749eb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="749eb-135">-WhatIf</span></span>
<span data-ttu-id="749eb-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="749eb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="749eb-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="749eb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="749eb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="749eb-138">CommonParameters</span></span>
<span data-ttu-id="749eb-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="749eb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="749eb-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="749eb-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="749eb-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="749eb-141">INPUTS</span></span>

### <span data-ttu-id="749eb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="749eb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="749eb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="749eb-143">System.String</span></span>

## <span data-ttu-id="749eb-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="749eb-144">OUTPUTS</span></span>

### <span data-ttu-id="749eb-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="749eb-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="749eb-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="749eb-146">NOTES</span></span>

## <span data-ttu-id="749eb-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="749eb-147">RELATED LINKS</span></span>
