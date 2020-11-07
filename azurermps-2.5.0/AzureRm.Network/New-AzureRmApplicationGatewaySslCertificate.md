---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: e22760c2838cf0b4fb0597dbd45532374b604b79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897589"
---
# <span data-ttu-id="c76a1-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c76a1-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c76a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c76a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c76a1-103">Tworzy certyfikat SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c76a1-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c76a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c76a1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c76a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c76a1-105">DESCRIPTION</span></span>
<span data-ttu-id="c76a1-106">Polecenie cmdlet **New-AzureRmApplicationGatewaySslCertificate** tworzy certyfikat SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c76a1-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="c76a1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c76a1-107">EXAMPLES</span></span>

### <span data-ttu-id="c76a1-108">Przykład 1: Tworzenie certyfikatu SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c76a1-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="c76a1-109">To polecenie tworzy certyfikat SSL o nazwie Cert01 dla domyślnej bramy Application Gateway i zapisuje wynik w zmiennej o nazwie $Cert.</span><span class="sxs-lookup"><span data-stu-id="c76a1-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="c76a1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c76a1-110">PARAMETERS</span></span>

### <span data-ttu-id="c76a1-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c76a1-111">-CertificateFile</span></span>
<span data-ttu-id="c76a1-112">Określa ścieżkę pliku PFX certyfikatu SSL tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c76a1-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c76a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c76a1-113">-DefaultProfile</span></span>
<span data-ttu-id="c76a1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c76a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c76a1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c76a1-115">-Name</span></span>
<span data-ttu-id="c76a1-116">Określa nazwę certyfikatu SSL tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c76a1-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c76a1-117">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="c76a1-117">-Password</span></span>
<span data-ttu-id="c76a1-118">Określa hasło protokołu SSL tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c76a1-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c76a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76a1-119">CommonParameters</span></span>
<span data-ttu-id="c76a1-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c76a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76a1-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c76a1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76a1-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c76a1-122">INPUTS</span></span>

### <span data-ttu-id="c76a1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c76a1-123">System.String</span></span>

## <span data-ttu-id="c76a1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c76a1-124">OUTPUTS</span></span>

### <span data-ttu-id="c76a1-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c76a1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c76a1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c76a1-126">NOTES</span></span>

## <span data-ttu-id="c76a1-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c76a1-127">RELATED LINKS</span></span>

[<span data-ttu-id="c76a1-128">Dodaj-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c76a1-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c76a1-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c76a1-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c76a1-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c76a1-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c76a1-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c76a1-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


