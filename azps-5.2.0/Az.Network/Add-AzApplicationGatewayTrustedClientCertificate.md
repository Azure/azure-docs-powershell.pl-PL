---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346645"
---
# <span data-ttu-id="75c34-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="75c34-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="75c34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75c34-102">SYNOPSIS</span></span>
<span data-ttu-id="75c34-103">Dodaje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="75c34-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="75c34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75c34-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75c34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="75c34-105">DESCRIPTION</span></span>
<span data-ttu-id="75c34-106">Polecenie cmdlet **Add-AzApplicationGatewayTrustedClientCertificate** dodaje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="75c34-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="75c34-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75c34-107">EXAMPLES</span></span>

### <span data-ttu-id="75c34-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="75c34-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="75c34-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="75c34-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="75c34-110">Drugie polecenie tworzy nowy łańcuch certyfikatów zaufanego certyfikatu urzędu certyfikacji klienta jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="75c34-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="75c34-111">Trzecie polecenie tworzy profil SSL przy użyciu zaufanego certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="75c34-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="75c34-112">Czwarte polecenie aktualizuje bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="75c34-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="75c34-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75c34-113">PARAMETERS</span></span>

### <span data-ttu-id="75c34-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75c34-114">-ApplicationGateway</span></span>
<span data-ttu-id="75c34-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75c34-115">The applicationGateway</span></span>

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

### <span data-ttu-id="75c34-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="75c34-116">-CertificateFile</span></span>
<span data-ttu-id="75c34-117">Ścieżka pliku łańcucha certyfikatu zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="75c34-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="75c34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c34-118">-DefaultProfile</span></span>
<span data-ttu-id="75c34-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="75c34-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75c34-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75c34-120">-Name</span></span>
<span data-ttu-id="75c34-121">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="75c34-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="75c34-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75c34-122">-Confirm</span></span>
<span data-ttu-id="75c34-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75c34-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c34-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75c34-124">-WhatIf</span></span>
<span data-ttu-id="75c34-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75c34-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75c34-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="75c34-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c34-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c34-127">CommonParameters</span></span>
<span data-ttu-id="75c34-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c34-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c34-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75c34-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c34-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75c34-130">INPUTS</span></span>

### <span data-ttu-id="75c34-131">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75c34-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="75c34-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75c34-132">OUTPUTS</span></span>

### <span data-ttu-id="75c34-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75c34-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="75c34-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75c34-134">NOTES</span></span>

## <span data-ttu-id="75c34-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75c34-135">RELATED LINKS</span></span>

[<span data-ttu-id="75c34-136">Nowe — AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="75c34-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="75c34-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="75c34-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="75c34-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="75c34-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="75c34-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="75c34-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)