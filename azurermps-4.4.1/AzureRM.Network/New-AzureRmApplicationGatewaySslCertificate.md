---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: ad318c776662ebaeab3192ca584aa2aad7f2e20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544695"
---
# <span data-ttu-id="1037f-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1037f-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="1037f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1037f-102">SYNOPSIS</span></span>
<span data-ttu-id="1037f-103">Tworzy certyfikat SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1037f-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1037f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1037f-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1037f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1037f-105">DESCRIPTION</span></span>
<span data-ttu-id="1037f-106">Polecenie cmdlet **New-AzureRmApplicationGatewaySslCertificate** tworzy certyfikat SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1037f-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="1037f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1037f-107">EXAMPLES</span></span>

### <span data-ttu-id="1037f-108">Przykład 1: Tworzenie certyfikatu SSL dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1037f-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\>$Cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="1037f-109">To polecenie tworzy certyfikat SSL o nazwie Cert01 dla domyślnej bramy Application Gateway i zapisuje wynik w zmiennej o nazwie $Cert.</span><span class="sxs-lookup"><span data-stu-id="1037f-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="1037f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1037f-110">PARAMETERS</span></span>

### <span data-ttu-id="1037f-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1037f-111">-CertificateFile</span></span>
<span data-ttu-id="1037f-112">Określa ścieżkę pliku PFX certyfikatu SSL tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1037f-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1037f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1037f-113">-Name</span></span>
<span data-ttu-id="1037f-114">Określa nazwę certyfikatu SSL tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1037f-114">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1037f-115">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="1037f-115">-Password</span></span>
<span data-ttu-id="1037f-116">Określa hasło protokołu SSL tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1037f-116">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1037f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1037f-117">-DefaultProfile</span></span>
<span data-ttu-id="1037f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1037f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1037f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1037f-119">CommonParameters</span></span>
<span data-ttu-id="1037f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1037f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1037f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1037f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1037f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1037f-122">INPUTS</span></span>

### <span data-ttu-id="1037f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1037f-123">System.String</span></span>

## <span data-ttu-id="1037f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1037f-124">OUTPUTS</span></span>

### <span data-ttu-id="1037f-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1037f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="1037f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1037f-126">NOTES</span></span>

## <span data-ttu-id="1037f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1037f-127">RELATED LINKS</span></span>

[<span data-ttu-id="1037f-128">Dodaj-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1037f-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1037f-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1037f-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1037f-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1037f-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1037f-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1037f-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


