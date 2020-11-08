---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054630"
---
# <span data-ttu-id="88fc0-101">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="88fc0-101">Get-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="88fc0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="88fc0-103">Pobiera certyfikaty bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="88fc0-103">Gets Application Gateway certificates.</span></span>

## <span data-ttu-id="88fc0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88fc0-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="88fc0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="88fc0-106">Polecenie cmdlet **Get-AzureApplicationGatewaySslCertificate** pobiera certyfikaty SSL (Secure Sockets Layer) dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88fc0-106">The **Get-AzureApplicationGatewaySslCertificate** cmdlet gets Secure Sockets Layer (SSL) certificates for an Azure Application Gateway.</span></span>

## <span data-ttu-id="88fc0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88fc0-107">EXAMPLES</span></span>

### <span data-ttu-id="88fc0-108">Przykład 1: Uzyskaj certyfikat SSL</span><span class="sxs-lookup"><span data-stu-id="88fc0-108">Example 1: Get an SSL certificate</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="88fc0-109">To polecenie pobiera certyfikat SSL o nazwie SslCertificate13 na bramie Application Gateway o nazwie ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="88fc0-109">This command gets an SSL certificate named SslCertificate13 on the Application Gateway named ApplicationGateway08.</span></span>

### <span data-ttu-id="88fc0-110">Przykład 2: uzyskiwanie wszystkich certyfikatów SSL</span><span class="sxs-lookup"><span data-stu-id="88fc0-110">Example 2: Get all SSL certificates</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

<span data-ttu-id="88fc0-111">To polecenie pobiera wszystkie certyfikaty SSL z bramy Application Gateway o nazwie ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="88fc0-111">This command gets all the SSL certificates on the Application Gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="88fc0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88fc0-112">PARAMETERS</span></span>

### <span data-ttu-id="88fc0-113">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="88fc0-113">-CertificateName</span></span>
<span data-ttu-id="88fc0-114">Określa nazwę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="88fc0-114">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="88fc0-115">To polecenie cmdlet pobiera certyfikat, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="88fc0-115">This cmdlet gets the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88fc0-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88fc0-116">-Name</span></span>
<span data-ttu-id="88fc0-117">Określa nazwę bramy aplikacji, z której to polecenie cmdlet pobiera certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="88fc0-117">Specifies the name of the Application Gateway from which this cmdlet gets an SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88fc0-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="88fc0-118">-Profile</span></span>
<span data-ttu-id="88fc0-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88fc0-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="88fc0-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="88fc0-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fc0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88fc0-121">CommonParameters</span></span>
<span data-ttu-id="88fc0-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88fc0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88fc0-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88fc0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88fc0-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88fc0-124">INPUTS</span></span>

### <span data-ttu-id="88fc0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="88fc0-125">System.String</span></span>

## <span data-ttu-id="88fc0-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88fc0-126">OUTPUTS</span></span>

### <span data-ttu-id="88fc0-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, list<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate></span><span class="sxs-lookup"><span data-stu-id="88fc0-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate, List<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate></span></span>

## <span data-ttu-id="88fc0-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88fc0-128">NOTES</span></span>

## <span data-ttu-id="88fc0-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88fc0-129">RELATED LINKS</span></span>

[<span data-ttu-id="88fc0-130">Dodaj-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="88fc0-130">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="88fc0-131">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="88fc0-131">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
