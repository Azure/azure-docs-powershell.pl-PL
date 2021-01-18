---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 4bf362402ba3db0ba50d9144d6bb9fa79977a998
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503424"
---
# <span data-ttu-id="24637-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="24637-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="24637-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24637-102">SYNOPSIS</span></span>
<span data-ttu-id="24637-103">Generuje kod weryfikacyjny dla certyfikatu centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="24637-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="24637-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24637-104">SYNTAX</span></span>

### <span data-ttu-id="24637-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24637-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24637-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="24637-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24637-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="24637-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24637-108">Opis</span><span class="sxs-lookup"><span data-stu-id="24637-108">DESCRIPTION</span></span>
<span data-ttu-id="24637-109">Ten kod weryfikacyjny służy do dokończenia etapu posiadania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="24637-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="24637-110">Użyj tego kodu weryfikacyjnego jako CN nowego certyfikatu podpisanego kluczem prywatnym certyfikaty główne.</span><span class="sxs-lookup"><span data-stu-id="24637-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="24637-111">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="24637-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="24637-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24637-112">EXAMPLES</span></span>

### <span data-ttu-id="24637-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24637-113">Example 1</span></span>
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

<span data-ttu-id="24637-114">Generuje kod weryfikacyjny dla talonu</span><span class="sxs-lookup"><span data-stu-id="24637-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="24637-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24637-115">PARAMETERS</span></span>

### <span data-ttu-id="24637-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="24637-116">-CertificateName</span></span>
<span data-ttu-id="24637-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="24637-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="24637-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24637-118">-DefaultProfile</span></span>
<span data-ttu-id="24637-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24637-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24637-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="24637-120">-Etag</span></span>
<span data-ttu-id="24637-121">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="24637-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="24637-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="24637-122">-InputObject</span></span>
<span data-ttu-id="24637-123">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="24637-123">Certificate Object</span></span>

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

### <span data-ttu-id="24637-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24637-124">-Name</span></span>
<span data-ttu-id="24637-125">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="24637-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="24637-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24637-126">-ResourceGroupName</span></span>
<span data-ttu-id="24637-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="24637-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="24637-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24637-128">-ResourceId</span></span>
<span data-ttu-id="24637-129">Identyfikator zasobu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="24637-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="24637-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24637-130">CommonParameters</span></span>
<span data-ttu-id="24637-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24637-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24637-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24637-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24637-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24637-133">INPUTS</span></span>

### <span data-ttu-id="24637-134">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="24637-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="24637-135">System. String</span><span class="sxs-lookup"><span data-stu-id="24637-135">System.String</span></span>

## <span data-ttu-id="24637-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24637-136">OUTPUTS</span></span>

### <span data-ttu-id="24637-137">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="24637-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="24637-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24637-138">NOTES</span></span>

## <span data-ttu-id="24637-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24637-139">RELATED LINKS</span></span>
