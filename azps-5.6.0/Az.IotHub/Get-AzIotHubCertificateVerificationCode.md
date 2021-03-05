---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 5cad5da87b15430c33d748250501862dae77a38e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988142"
---
# <span data-ttu-id="c8353-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="c8353-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="c8353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8353-102">SYNOPSIS</span></span>
<span data-ttu-id="c8353-103">Generuje kod weryfikacyjny dla certyfikatu usługi Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c8353-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="c8353-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c8353-104">SYNTAX</span></span>

### <span data-ttu-id="c8353-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c8353-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8353-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c8353-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8353-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c8353-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8353-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c8353-108">DESCRIPTION</span></span>
<span data-ttu-id="c8353-109">Ten kod weryfikacyjny służy do ukończenia dowodu posiadania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="c8353-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="c8353-110">Użyj tego kodu weryfikacyjnego jako kodu CN nowego certyfikatu podpisanego za pomocą klucza prywatnego certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="c8353-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="c8353-111">Aby uzyskać szczegółowe objaśnienie certyfikatów urzędu certyfikacji w centrum Azure IoT Hub, zobacz https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="c8353-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="c8353-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c8353-112">EXAMPLES</span></span>

### <span data-ttu-id="c8353-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c8353-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="c8353-114">Generuje kod weryfikacyjny dla certyfikatu MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="c8353-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="c8353-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8353-115">PARAMETERS</span></span>

### <span data-ttu-id="c8353-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c8353-116">-CertificateName</span></span>
<span data-ttu-id="c8353-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="c8353-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="c8353-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8353-118">-DefaultProfile</span></span>
<span data-ttu-id="c8353-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8353-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8353-120">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="c8353-120">-Etag</span></span>
<span data-ttu-id="c8353-121">Etag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="c8353-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="c8353-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8353-122">-InputObject</span></span>
<span data-ttu-id="c8353-123">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="c8353-123">Certificate Object</span></span>

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

### <span data-ttu-id="c8353-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c8353-124">-Name</span></span>
<span data-ttu-id="c8353-125">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="c8353-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c8353-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8353-126">-ResourceGroupName</span></span>
<span data-ttu-id="c8353-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c8353-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c8353-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8353-128">-ResourceId</span></span>
<span data-ttu-id="c8353-129">Identyfikator zasobu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="c8353-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="c8353-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8353-130">CommonParameters</span></span>
<span data-ttu-id="c8353-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8353-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8353-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8353-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8353-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8353-133">INPUTS</span></span>

### <span data-ttu-id="c8353-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="c8353-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="c8353-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c8353-135">System.String</span></span>

## <span data-ttu-id="c8353-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8353-136">OUTPUTS</span></span>

### <span data-ttu-id="c8353-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="c8353-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="c8353-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c8353-138">NOTES</span></span>

## <span data-ttu-id="c8353-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8353-139">RELATED LINKS</span></span>
