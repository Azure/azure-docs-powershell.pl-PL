---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 99d56b837b67fe8b816c4f27c8658932a74452e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193915"
---
# <span data-ttu-id="ada92-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ada92-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="ada92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada92-102">SYNOPSIS</span></span>
<span data-ttu-id="ada92-103">Pobiera łańcuch certyfikatów zaufanego urzędu certyfikacji klienta o określonej nazwie z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ada92-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="ada92-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ada92-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ada92-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ada92-105">DESCRIPTION</span></span>
<span data-ttu-id="ada92-106">Polecenie Get-AzApplicationGatewayTrustedClientCertificate pobiera łańcuch certyfikatów zaufanego urzędu certyfikacji klienta o określonej nazwie z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ada92-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="ada92-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ada92-107">EXAMPLES</span></span>

### <span data-ttu-id="ada92-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ada92-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="ada92-109">Pierwsze polecenie pobiera bramę aplikacji i przechowuje je w $gw zmienną.</span><span class="sxs-lookup"><span data-stu-id="ada92-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="ada92-110">Drugie polecenie pobiera łańcuch certyfikatów zaufanego urzędu certyfikacji klienta o określonej nazwie z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ada92-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="ada92-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ada92-111">PARAMETERS</span></span>

### <span data-ttu-id="ada92-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ada92-112">-ApplicationGateway</span></span>
<span data-ttu-id="ada92-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="ada92-113">The applicationGateway</span></span>

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

### <span data-ttu-id="ada92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada92-114">-DefaultProfile</span></span>
<span data-ttu-id="ada92-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ada92-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ada92-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ada92-116">-Name</span></span>
<span data-ttu-id="ada92-117">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="ada92-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="ada92-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada92-118">CommonParameters</span></span>
<span data-ttu-id="ada92-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada92-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada92-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ada92-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada92-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada92-121">INPUTS</span></span>

### <span data-ttu-id="ada92-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ada92-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ada92-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ada92-123">OUTPUTS</span></span>

### <span data-ttu-id="ada92-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ada92-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="ada92-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ada92-125">NOTES</span></span>

## <span data-ttu-id="ada92-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ada92-126">RELATED LINKS</span></span>

[<span data-ttu-id="ada92-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ada92-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ada92-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ada92-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ada92-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ada92-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ada92-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ada92-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)