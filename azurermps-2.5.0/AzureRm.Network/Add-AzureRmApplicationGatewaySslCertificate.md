---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: 65c178cc8cf293cf6c20e6262733031e377f61fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897625"
---
# <span data-ttu-id="16910-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="16910-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="16910-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16910-102">SYNOPSIS</span></span>
<span data-ttu-id="16910-103">Dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16910-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16910-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16910-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16910-105">Opis</span><span class="sxs-lookup"><span data-stu-id="16910-105">DESCRIPTION</span></span>
<span data-ttu-id="16910-106">Polecenie cmdlet **Add-AzureRmApplicationGatewaySslCertificate** dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16910-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="16910-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16910-107">EXAMPLES</span></span>

### <span data-ttu-id="16910-108">Przykład 1. Dodaj certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16910-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="16910-109">To polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01, a następnie dodaje do niej certyfikat SSL o nazwie Cert01.</span><span class="sxs-lookup"><span data-stu-id="16910-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="16910-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16910-110">PARAMETERS</span></span>

### <span data-ttu-id="16910-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16910-111">-ApplicationGateway</span></span>
<span data-ttu-id="16910-112">Określa nazwę bramy aplikacji, z którą to polecenie cmdlet dodaje certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="16910-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="16910-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="16910-113">-CertificateFile</span></span>
<span data-ttu-id="16910-114">Określa plik PFX certyfikatu SSL, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16910-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="16910-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16910-115">-DefaultProfile</span></span>
<span data-ttu-id="16910-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16910-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16910-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="16910-117">-Name</span></span>
<span data-ttu-id="16910-118">Określa nazwę certyfikatu SSL, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16910-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="16910-119">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="16910-119">-Password</span></span>
<span data-ttu-id="16910-120">Określa hasło certyfikatu SSL, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16910-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="16910-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16910-121">CommonParameters</span></span>
<span data-ttu-id="16910-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16910-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16910-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16910-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16910-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16910-124">INPUTS</span></span>

### <span data-ttu-id="16910-125">System. String</span><span class="sxs-lookup"><span data-stu-id="16910-125">System.String</span></span>

## <span data-ttu-id="16910-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16910-126">OUTPUTS</span></span>

### <span data-ttu-id="16910-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16910-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16910-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16910-128">NOTES</span></span>

## <span data-ttu-id="16910-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16910-129">RELATED LINKS</span></span>

[<span data-ttu-id="16910-130">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="16910-130">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="16910-131">Nowe — AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="16910-131">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="16910-132">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="16910-132">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="16910-133">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="16910-133">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


