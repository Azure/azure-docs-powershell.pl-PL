---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 923852448f96ddc59de7a1c1562d6665b00e25ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705249"
---
# <span data-ttu-id="5578d-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="5578d-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="5578d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5578d-102">SYNOPSIS</span></span>
<span data-ttu-id="5578d-103">Generuje kod weryfikacyjny dla certyfikatu centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5578d-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="5578d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5578d-104">SYNTAX</span></span>

### <span data-ttu-id="5578d-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5578d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5578d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5578d-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5578d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5578d-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5578d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5578d-108">DESCRIPTION</span></span>
<span data-ttu-id="5578d-109">Ten kod weryfikacyjny służy do dokończenia etapu posiadania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5578d-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="5578d-110">Użyj tego kodu weryfikacyjnego jako CN nowego certyfikatu podpisanego kluczem prywatnym certyfikaty główne.</span><span class="sxs-lookup"><span data-stu-id="5578d-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="5578d-111">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="5578d-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="5578d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5578d-112">EXAMPLES</span></span>

### <span data-ttu-id="5578d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5578d-113">Example 1</span></span>
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

<span data-ttu-id="5578d-114">Generuje kod weryfikacyjny dla talonu</span><span class="sxs-lookup"><span data-stu-id="5578d-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="5578d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5578d-115">PARAMETERS</span></span>

### <span data-ttu-id="5578d-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="5578d-116">-CertificateName</span></span>
<span data-ttu-id="5578d-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="5578d-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="5578d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5578d-118">-DefaultProfile</span></span>
<span data-ttu-id="5578d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5578d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5578d-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="5578d-120">-Etag</span></span>
<span data-ttu-id="5578d-121">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="5578d-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="5578d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5578d-122">-InputObject</span></span>
<span data-ttu-id="5578d-123">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="5578d-123">Certificate Object</span></span>

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

### <span data-ttu-id="5578d-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5578d-124">-Name</span></span>
<span data-ttu-id="5578d-125">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="5578d-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5578d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5578d-126">-ResourceGroupName</span></span>
<span data-ttu-id="5578d-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5578d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5578d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5578d-128">-ResourceId</span></span>
<span data-ttu-id="5578d-129">Identyfikator zasobu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="5578d-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="5578d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5578d-130">CommonParameters</span></span>
<span data-ttu-id="5578d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5578d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5578d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5578d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5578d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5578d-133">INPUTS</span></span>

### <span data-ttu-id="5578d-134">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="5578d-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="5578d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5578d-135">System.String</span></span>

## <span data-ttu-id="5578d-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5578d-136">OUTPUTS</span></span>

### <span data-ttu-id="5578d-137">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="5578d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="5578d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5578d-138">NOTES</span></span>

## <span data-ttu-id="5578d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5578d-139">RELATED LINKS</span></span>
