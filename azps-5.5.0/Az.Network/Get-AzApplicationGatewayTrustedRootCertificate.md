---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203132"
---
# <span data-ttu-id="170f8-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="170f8-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="170f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="170f8-102">SYNOPSIS</span></span>
<span data-ttu-id="170f8-103">Pobiera zaufany certyfikat główny o określonej nazwie z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="170f8-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="170f8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="170f8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="170f8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="170f8-105">DESCRIPTION</span></span>
<span data-ttu-id="170f8-106">Polecenie **cmdlet Get-AzApplicationGatewayTrustedRootCertificate** pobiera certyfikat główny o określonej nazwie z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="170f8-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="170f8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="170f8-107">EXAMPLES</span></span>

### <span data-ttu-id="170f8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="170f8-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="170f8-109">Pierwsze polecenie pobiera bramę aplikacji i zapisuje je w $gw zmienną.</span><span class="sxs-lookup"><span data-stu-id="170f8-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="170f8-110">Drugie polecenie pobiera zaufany certyfikat główny o określonej nazwie z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="170f8-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="170f8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="170f8-111">PARAMETERS</span></span>

### <span data-ttu-id="170f8-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="170f8-112">-ApplicationGateway</span></span>
<span data-ttu-id="170f8-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="170f8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="170f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170f8-114">-DefaultProfile</span></span>
<span data-ttu-id="170f8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="170f8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170f8-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="170f8-116">-Name</span></span>
<span data-ttu-id="170f8-117">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="170f8-117">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170f8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170f8-118">CommonParameters</span></span>
<span data-ttu-id="170f8-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170f8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170f8-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="170f8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170f8-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="170f8-121">INPUTS</span></span>

### <span data-ttu-id="170f8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="170f8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="170f8-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="170f8-123">OUTPUTS</span></span>

### <span data-ttu-id="170f8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="170f8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="170f8-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="170f8-125">NOTES</span></span>

## <span data-ttu-id="170f8-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="170f8-126">RELATED LINKS</span></span>

[<span data-ttu-id="170f8-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="170f8-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="170f8-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="170f8-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="170f8-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="170f8-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="170f8-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="170f8-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
