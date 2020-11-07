---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 964e99912e4f21d48e89b725da1aa44ac32ea186
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891005"
---
# <span data-ttu-id="2f3b6-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f3b6-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="2f3b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f3b6-102">SYNOPSIS</span></span>
<span data-ttu-id="2f3b6-103">Dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f3b6-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="2f3b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f3b6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f3b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f3b6-105">DESCRIPTION</span></span>
<span data-ttu-id="2f3b6-106">Polecenie cmdlet **Add-AzApplicationGatewaySslCertificate** dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f3b6-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="2f3b6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f3b6-107">EXAMPLES</span></span>

### <span data-ttu-id="2f3b6-108">Przykład 1. Dodaj certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f3b6-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="2f3b6-109">To polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01, a następnie dodaje do niej certyfikat SSL o nazwie Cert01.</span><span class="sxs-lookup"><span data-stu-id="2f3b6-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="2f3b6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f3b6-110">PARAMETERS</span></span>

### <span data-ttu-id="2f3b6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f3b6-111">-ApplicationGateway</span></span>
<span data-ttu-id="2f3b6-112">Określa nazwę bramy aplikacji, z którą to polecenie cmdlet dodaje certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="2f3b6-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f3b6-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="2f3b6-113">-CertificateFile</span></span>
<span data-ttu-id="2f3b6-114">Określa plik PFX certyfikatu SSL, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f3b6-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f3b6-115">-DefaultProfile</span></span>
<span data-ttu-id="2f3b6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f3b6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3b6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f3b6-117">-Name</span></span>
<span data-ttu-id="2f3b6-118">Określa nazwę certyfikatu SSL, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f3b6-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3b6-119">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="2f3b6-119">-Password</span></span>
<span data-ttu-id="2f3b6-120">Określa hasło certyfikatu SSL, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f3b6-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3b6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f3b6-121">CommonParameters</span></span>
<span data-ttu-id="2f3b6-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f3b6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f3b6-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f3b6-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f3b6-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f3b6-124">INPUTS</span></span>

### <span data-ttu-id="2f3b6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2f3b6-125">System.String</span></span>

## <span data-ttu-id="2f3b6-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f3b6-126">OUTPUTS</span></span>

### <span data-ttu-id="2f3b6-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f3b6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2f3b6-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f3b6-128">NOTES</span></span>

## <span data-ttu-id="2f3b6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f3b6-129">RELATED LINKS</span></span>

[<span data-ttu-id="2f3b6-130">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f3b6-130">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2f3b6-131">Nowe — AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f3b6-131">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2f3b6-132">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f3b6-132">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2f3b6-133">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f3b6-133">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


