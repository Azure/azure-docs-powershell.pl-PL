---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e34d170167aac09cd64ca11d0838f36fc0515423
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990032"
---
# <span data-ttu-id="0e242-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0e242-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="0e242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e242-102">SYNOPSIS</span></span>
<span data-ttu-id="0e242-103">Tworzy łańcuch certyfikatów zaufanego urzędu certyfikacji klienta dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0e242-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="0e242-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e242-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e242-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e242-105">DESCRIPTION</span></span>
<span data-ttu-id="0e242-106">Polecenie New-AzApplicationGatewayTrustedClientCertificate cmdlet tworzy łańcuch certyfikatów zaufanego urzędu certyfikacji klienta dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0e242-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="0e242-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e242-107">EXAMPLES</span></span>

### <span data-ttu-id="0e242-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e242-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="0e242-109">Polecenie tworzy nowy obiekt łańcucha certyfikatów zaufanego urzędu certyfikacji klienta, który przyjmuje ścieżkę certyfikatu urzędu certyfikacji klienta jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="0e242-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="0e242-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e242-110">PARAMETERS</span></span>

### <span data-ttu-id="0e242-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0e242-111">-CertificateFile</span></span>
<span data-ttu-id="0e242-112">Ścieżka pliku zaufanego łańcucha certyfikatów urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="0e242-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="0e242-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e242-113">-DefaultProfile</span></span>
<span data-ttu-id="0e242-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e242-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e242-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0e242-115">-Name</span></span>
<span data-ttu-id="0e242-116">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="0e242-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="0e242-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e242-117">-Confirm</span></span>
<span data-ttu-id="0e242-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0e242-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e242-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e242-119">-WhatIf</span></span>
<span data-ttu-id="0e242-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e242-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e242-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0e242-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e242-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e242-122">CommonParameters</span></span>
<span data-ttu-id="0e242-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e242-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e242-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e242-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e242-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e242-125">INPUTS</span></span>

### <span data-ttu-id="0e242-126">Brak</span><span class="sxs-lookup"><span data-stu-id="0e242-126">None</span></span>

## <span data-ttu-id="0e242-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e242-127">OUTPUTS</span></span>

### <span data-ttu-id="0e242-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0e242-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="0e242-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e242-129">NOTES</span></span>

## <span data-ttu-id="0e242-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e242-130">RELATED LINKS</span></span>

[<span data-ttu-id="0e242-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0e242-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="0e242-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0e242-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="0e242-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0e242-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="0e242-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0e242-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)