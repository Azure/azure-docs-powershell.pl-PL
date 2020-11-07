---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7ed7029d3f623db1cc3379dfe50436a352927c60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718168"
---
# <span data-ttu-id="c0f34-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c0f34-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c0f34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0f34-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f34-103">Dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c0f34-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0f34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0f34-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0f34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c0f34-105">DESCRIPTION</span></span>
<span data-ttu-id="c0f34-106">Polecenie cmdlet **Add-AzureRmApplicationGatewaySslCertificate** dodaje certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c0f34-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="c0f34-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0f34-107">EXAMPLES</span></span>

### <span data-ttu-id="c0f34-108">Przykład 1. Dodaj certyfikat SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c0f34-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="c0f34-109">To polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01, a następnie dodaje do niej certyfikat SSL o nazwie Cert01.</span><span class="sxs-lookup"><span data-stu-id="c0f34-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="c0f34-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0f34-110">PARAMETERS</span></span>

### <span data-ttu-id="c0f34-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0f34-111">-ApplicationGateway</span></span>
<span data-ttu-id="c0f34-112">Określa nazwę bramy aplikacji, z którą to polecenie cmdlet dodaje certyfikat SSL.</span><span class="sxs-lookup"><span data-stu-id="c0f34-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0f34-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c0f34-113">-CertificateFile</span></span>
<span data-ttu-id="c0f34-114">Określa plik PFX certyfikatu SSL, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0f34-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0f34-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0f34-115">-Name</span></span>
<span data-ttu-id="c0f34-116">Określa nazwę certyfikatu SSL, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0f34-116">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0f34-117">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="c0f34-117">-Password</span></span>
<span data-ttu-id="c0f34-118">Określa hasło certyfikatu SSL, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0f34-118">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0f34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f34-119">-DefaultProfile</span></span>
<span data-ttu-id="c0f34-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f34-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0f34-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f34-121">CommonParameters</span></span>
<span data-ttu-id="c0f34-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f34-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f34-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0f34-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f34-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0f34-124">INPUTS</span></span>

### <span data-ttu-id="c0f34-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c0f34-125">System.String</span></span>

## <span data-ttu-id="c0f34-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0f34-126">OUTPUTS</span></span>

### <span data-ttu-id="c0f34-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0f34-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c0f34-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0f34-128">NOTES</span></span>

## <span data-ttu-id="c0f34-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0f34-129">RELATED LINKS</span></span>

[<span data-ttu-id="c0f34-130">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c0f34-130">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c0f34-131">Nowe — AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c0f34-131">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c0f34-132">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c0f34-132">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c0f34-133">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c0f34-133">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


