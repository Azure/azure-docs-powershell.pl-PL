---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055460"
---
# <span data-ttu-id="1d992-101">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1d992-101">Remove-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="1d992-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d992-102">SYNOPSIS</span></span>
<span data-ttu-id="1d992-103">Usuwa certyfikat SSL z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1d992-103">Removes an SSL certificate from an application gateway.</span></span>

## <span data-ttu-id="1d992-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d992-104">SYNTAX</span></span>

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1d992-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d992-105">DESCRIPTION</span></span>
<span data-ttu-id="1d992-106">Polecenie cmdlet **Remove-AzureApplicationGatewaySslCertificate** usuwa certyfikat SSL (Secure Sockets Layer) z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1d992-106">The **Remove-AzureApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an application gateway.</span></span>

## <span data-ttu-id="1d992-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d992-107">EXAMPLES</span></span>

### <span data-ttu-id="1d992-108">Przykład 1: Usuwanie certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="1d992-108">Example 1: Remove an SSL certificate</span></span>
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="1d992-109">To polecenie usuwa certyfikat SSL o nazwie SslCertificate13 z bramy Application Gateway o nazwie ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="1d992-109">This command removes an SSL certificate named SslCertificate13 from the application gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="1d992-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d992-110">PARAMETERS</span></span>

### <span data-ttu-id="1d992-111">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="1d992-111">-CertificateName</span></span>
<span data-ttu-id="1d992-112">Określa nazwę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="1d992-112">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="1d992-113">To polecenie cmdlet usuwa certyfikat, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1d992-113">This cmdlet removes the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d992-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d992-114">-Name</span></span>
<span data-ttu-id="1d992-115">Określa nazwę bramy aplikacji, z której to polecenie cmdlet usuwa certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="1d992-115">Specifies the name of the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="1d992-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="1d992-116">-Profile</span></span>
<span data-ttu-id="1d992-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d992-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1d992-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1d992-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1d992-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d992-119">CommonParameters</span></span>
<span data-ttu-id="1d992-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d992-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d992-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d992-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d992-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d992-122">INPUTS</span></span>

### <span data-ttu-id="1d992-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1d992-123">System.String</span></span>

## <span data-ttu-id="1d992-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d992-124">OUTPUTS</span></span>

### <span data-ttu-id="1d992-125">Microsoft. platformy windowsazure. Management. ApplicationGateway. MODELES. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1d992-125">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="1d992-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d992-126">NOTES</span></span>

## <span data-ttu-id="1d992-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d992-127">RELATED LINKS</span></span>

[<span data-ttu-id="1d992-128">Dodaj-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1d992-128">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1d992-129">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1d992-129">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)
