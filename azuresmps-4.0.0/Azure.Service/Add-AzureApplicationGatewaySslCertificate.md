---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054702"
---
# <span data-ttu-id="3d759-101">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3d759-101">Add-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="3d759-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d759-102">SYNOPSIS</span></span>
<span data-ttu-id="3d759-103">Dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3d759-103">Adds an SSL certificate to an Application Gateway.</span></span>

## <span data-ttu-id="3d759-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d759-104">SYNTAX</span></span>

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d759-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d759-105">DESCRIPTION</span></span>
<span data-ttu-id="3d759-106">Polecenie cmdlet **Add-AzureApplicationGatewaySslCertificate** dodaje certyfikat SSL (Secure Sockets Layer) do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d759-106">The **Add-AzureApplicationGatewaySslCertificate** cmdlet adds a Secure Sockets Layer (SSL) certificate to an Azure Application Gateway.</span></span>

## <span data-ttu-id="3d759-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d759-107">EXAMPLES</span></span>

### <span data-ttu-id="3d759-108">Przykład 1: Dodawanie certyfikatu SSL</span><span class="sxs-lookup"><span data-stu-id="3d759-108">Example 1: Add an SSL certificate</span></span>
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

<span data-ttu-id="3d759-109">To polecenie dodaje certyfikat SSL o nazwie SslCertificate13 do bramy Application Gateway o nazwie ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="3d759-109">This command adds an SSL certificate named SslCertificate13 to the Application Gateway named ApplicationGateway08.</span></span>
<span data-ttu-id="3d759-110">Polecenie określa ścieżkę pliku certyfikatu oraz hasło do certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="3d759-110">The command specifies the path of the certificate file and the password for the certificate.</span></span>

## <span data-ttu-id="3d759-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d759-111">PARAMETERS</span></span>

### <span data-ttu-id="3d759-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3d759-112">-CertificateFile</span></span>
<span data-ttu-id="3d759-113">Określa ścieżkę do pliku certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="3d759-113">Specifies the path of an SSL certificate file.</span></span>
<span data-ttu-id="3d759-114">To polecenie cmdlet dodaje certyfikat do pliku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3d759-114">This cmdlet adds the certificate in the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d759-115">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="3d759-115">-CertificateName</span></span>
<span data-ttu-id="3d759-116">Określa nazwę certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="3d759-116">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="3d759-117">To polecenie cmdlet dodaje certyfikat, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3d759-117">This cmdlet adds the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d759-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d759-118">-Name</span></span>
<span data-ttu-id="3d759-119">Określa nazwę bramy aplikacji, z którą to polecenie cmdlet dodaje certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="3d759-119">Specifies the name of the Application Gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="3d759-120">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="3d759-120">-Password</span></span>
<span data-ttu-id="3d759-121">Określa hasło certyfikatu SSL, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d759-121">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="3d759-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d759-122">-Profile</span></span>
<span data-ttu-id="3d759-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d759-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d759-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3d759-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d759-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d759-125">CommonParameters</span></span>
<span data-ttu-id="3d759-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d759-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d759-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d759-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d759-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d759-128">INPUTS</span></span>

### <span data-ttu-id="3d759-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3d759-129">System.String</span></span>

## <span data-ttu-id="3d759-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d759-130">OUTPUTS</span></span>

### <span data-ttu-id="3d759-131">Microsoft. platformy windowsazure. Management. ApplicationGateway. MODELES. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3d759-131">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="3d759-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d759-132">NOTES</span></span>

## <span data-ttu-id="3d759-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d759-133">RELATED LINKS</span></span>

[<span data-ttu-id="3d759-134">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3d759-134">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3d759-135">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3d759-135">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
