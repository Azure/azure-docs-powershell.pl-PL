---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179954"
---
# <span data-ttu-id="38960-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="38960-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="38960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38960-102">SYNOPSIS</span></span>
<span data-ttu-id="38960-103">Dodaje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="38960-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="38960-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="38960-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38960-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="38960-105">DESCRIPTION</span></span>
<span data-ttu-id="38960-106">Polecenie **cmdlet Add-AzApplicationGatewayTrustedClientCertificate** dodaje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38960-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="38960-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="38960-107">EXAMPLES</span></span>

### <span data-ttu-id="38960-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38960-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="38960-109">Pierwsze polecenie pobiera bramę aplikacji i przechowuje ją w $gw zmienną.</span><span class="sxs-lookup"><span data-stu-id="38960-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="38960-110">Drugie polecenie tworzy nowy łańcuch certyfikatów zaufanego urzędu certyfikacji klienta, który przyjmuje ścieżkę certyfikatu urzędu certyfikacji klienta jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="38960-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="38960-111">Trzecie polecenie tworzy profil SSL przy użyciu certyfikatu zaufanego klienta.</span><span class="sxs-lookup"><span data-stu-id="38960-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="38960-112">Czwarte polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="38960-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="38960-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38960-113">PARAMETERS</span></span>

### <span data-ttu-id="38960-114">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38960-114">-ApplicationGateway</span></span>
<span data-ttu-id="38960-115">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="38960-115">The applicationGateway</span></span>

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

### <span data-ttu-id="38960-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="38960-116">-CertificateFile</span></span>
<span data-ttu-id="38960-117">Ścieżka pliku zaufanego łańcucha certyfikatów urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="38960-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="38960-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38960-118">-DefaultProfile</span></span>
<span data-ttu-id="38960-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="38960-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38960-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="38960-120">-Name</span></span>
<span data-ttu-id="38960-121">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="38960-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="38960-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38960-122">-Confirm</span></span>
<span data-ttu-id="38960-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="38960-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38960-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38960-124">-WhatIf</span></span>
<span data-ttu-id="38960-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38960-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38960-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="38960-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38960-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38960-127">CommonParameters</span></span>
<span data-ttu-id="38960-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38960-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38960-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38960-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38960-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38960-130">INPUTS</span></span>

### <span data-ttu-id="38960-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38960-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38960-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38960-132">OUTPUTS</span></span>

### <span data-ttu-id="38960-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38960-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38960-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="38960-134">NOTES</span></span>

## <span data-ttu-id="38960-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38960-135">RELATED LINKS</span></span>

[<span data-ttu-id="38960-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="38960-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="38960-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="38960-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="38960-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="38960-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="38960-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="38960-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)