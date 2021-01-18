---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 99d56b837b67fe8b816c4f27c8658932a74452e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498770"
---
# <span data-ttu-id="8a482-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8a482-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="8a482-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a482-102">SYNOPSIS</span></span>
<span data-ttu-id="8a482-103">Pobiera łańcuch certyfikatów zaufanego urzędu certyfikacji klienta o określonej nazwie od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8a482-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="8a482-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a482-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a482-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8a482-105">DESCRIPTION</span></span>
<span data-ttu-id="8a482-106">Polecenie cmdlet Get-AzApplicationGatewayTrustedClientCertificate Pobiera łańcuch certyfikatów zaufanego urzędu certyfikacji klienta z określoną nazwą z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8a482-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="8a482-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a482-107">EXAMPLES</span></span>

### <span data-ttu-id="8a482-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a482-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="8a482-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="8a482-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="8a482-110">Drugie polecenie Pobiera łańcuch certyfikatów zaufanego urzędu certyfikacji klienta o określonej nazwie z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8a482-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="8a482-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a482-111">PARAMETERS</span></span>

### <span data-ttu-id="8a482-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a482-112">-ApplicationGateway</span></span>
<span data-ttu-id="8a482-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a482-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8a482-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a482-114">-DefaultProfile</span></span>
<span data-ttu-id="8a482-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a482-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a482-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8a482-116">-Name</span></span>
<span data-ttu-id="8a482-117">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="8a482-117">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a482-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a482-118">CommonParameters</span></span>
<span data-ttu-id="8a482-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a482-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a482-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a482-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a482-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a482-121">INPUTS</span></span>

### <span data-ttu-id="8a482-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a482-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a482-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a482-123">OUTPUTS</span></span>

### <span data-ttu-id="8a482-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8a482-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="8a482-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a482-125">NOTES</span></span>

## <span data-ttu-id="8a482-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a482-126">RELATED LINKS</span></span>

[<span data-ttu-id="8a482-127">Nowe — AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8a482-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="8a482-128">Dodaj-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8a482-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="8a482-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8a482-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="8a482-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8a482-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)