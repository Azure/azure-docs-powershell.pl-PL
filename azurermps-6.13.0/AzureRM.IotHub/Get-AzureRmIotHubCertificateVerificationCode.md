---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
ms.openlocfilehash: a2c4c72f93597f3275e9edb1fecb6139eafbeb50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552823"
---
# <span data-ttu-id="8ef95-101">Get-AzureRmIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="8ef95-101">Get-AzureRmIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="8ef95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ef95-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef95-103">Generuje kod weryfikacyjny dla certyfikatu centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8ef95-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ef95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ef95-104">SYNTAX</span></span>

### <span data-ttu-id="8ef95-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8ef95-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ef95-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8ef95-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ef95-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8ef95-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ef95-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8ef95-108">DESCRIPTION</span></span>
<span data-ttu-id="8ef95-109">Ten kod weryfikacyjny służy do dokończenia etapu posiadania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8ef95-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="8ef95-110">Użyj tego kodu weryfikacyjnego jako CN nowego certyfikatu podpisanego kluczem prywatnym certyfikaty główne.</span><span class="sxs-lookup"><span data-stu-id="8ef95-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="8ef95-111">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="8ef95-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="8ef95-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ef95-112">EXAMPLES</span></span>

### <span data-ttu-id="8ef95-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ef95-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="8ef95-114">Generuje kod weryfikacyjny dla talonu</span><span class="sxs-lookup"><span data-stu-id="8ef95-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="8ef95-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ef95-115">PARAMETERS</span></span>

### <span data-ttu-id="8ef95-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="8ef95-116">-CertificateName</span></span>
<span data-ttu-id="8ef95-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="8ef95-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="8ef95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef95-118">-DefaultProfile</span></span>
<span data-ttu-id="8ef95-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef95-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ef95-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="8ef95-120">-Etag</span></span>
<span data-ttu-id="8ef95-121">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="8ef95-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="8ef95-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ef95-122">-InputObject</span></span>
<span data-ttu-id="8ef95-123">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="8ef95-123">Certificate Object</span></span>

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

### <span data-ttu-id="8ef95-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ef95-124">-Name</span></span>
<span data-ttu-id="8ef95-125">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="8ef95-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8ef95-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ef95-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ef95-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8ef95-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8ef95-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ef95-128">-ResourceId</span></span>
<span data-ttu-id="8ef95-129">Identyfikator zasobu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="8ef95-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="8ef95-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef95-130">CommonParameters</span></span>
<span data-ttu-id="8ef95-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ef95-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef95-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ef95-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef95-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ef95-133">INPUTS</span></span>

### <span data-ttu-id="8ef95-134">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="8ef95-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="8ef95-135">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ef95-135">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8ef95-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8ef95-136">System.String</span></span>

## <span data-ttu-id="8ef95-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ef95-137">OUTPUTS</span></span>

### <span data-ttu-id="8ef95-138">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="8ef95-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="8ef95-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ef95-139">NOTES</span></span>

## <span data-ttu-id="8ef95-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ef95-140">RELATED LINKS</span></span>
