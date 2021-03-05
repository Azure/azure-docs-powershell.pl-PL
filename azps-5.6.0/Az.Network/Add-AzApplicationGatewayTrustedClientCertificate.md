---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: ac4da06b2f90f9d7bb5c3cbccbde98c8c65db481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982474"
---
# <span data-ttu-id="1f01c-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1f01c-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="1f01c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f01c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f01c-103">Dodaje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f01c-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="1f01c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f01c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f01c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f01c-105">DESCRIPTION</span></span>
<span data-ttu-id="1f01c-106">Polecenie **cmdlet Add-AzApplicationGatewayTrustedClientCertificate** dodaje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f01c-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="1f01c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f01c-107">EXAMPLES</span></span>

### <span data-ttu-id="1f01c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1f01c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="1f01c-109">Pierwsze polecenie pobiera bramę aplikacji i przechowuje ją w $gw zmienną.</span><span class="sxs-lookup"><span data-stu-id="1f01c-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="1f01c-110">Drugie polecenie tworzy nowy łańcuch certyfikatów zaufanego urzędu certyfikacji klienta, który przyjmuje ścieżkę certyfikatu urzędu certyfikacji klienta jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1f01c-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="1f01c-111">Trzecie polecenie tworzy profil SSL przy użyciu certyfikatu zaufanego klienta.</span><span class="sxs-lookup"><span data-stu-id="1f01c-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="1f01c-112">Czwarte polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f01c-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="1f01c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f01c-113">PARAMETERS</span></span>

### <span data-ttu-id="1f01c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f01c-114">-ApplicationGateway</span></span>
<span data-ttu-id="1f01c-115">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f01c-115">The applicationGateway</span></span>

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

### <span data-ttu-id="1f01c-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1f01c-116">-CertificateFile</span></span>
<span data-ttu-id="1f01c-117">Ścieżka pliku zaufanego łańcucha certyfikatów urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="1f01c-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="1f01c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f01c-118">-DefaultProfile</span></span>
<span data-ttu-id="1f01c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f01c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f01c-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1f01c-120">-Name</span></span>
<span data-ttu-id="1f01c-121">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="1f01c-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="1f01c-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f01c-122">-Confirm</span></span>
<span data-ttu-id="1f01c-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f01c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f01c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f01c-124">-WhatIf</span></span>
<span data-ttu-id="1f01c-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f01c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f01c-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1f01c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f01c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f01c-127">CommonParameters</span></span>
<span data-ttu-id="1f01c-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f01c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f01c-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f01c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f01c-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f01c-130">INPUTS</span></span>

### <span data-ttu-id="1f01c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f01c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1f01c-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f01c-132">OUTPUTS</span></span>

### <span data-ttu-id="1f01c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f01c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1f01c-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f01c-134">NOTES</span></span>

## <span data-ttu-id="1f01c-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f01c-135">RELATED LINKS</span></span>

[<span data-ttu-id="1f01c-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1f01c-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1f01c-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1f01c-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1f01c-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1f01c-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1f01c-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1f01c-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)