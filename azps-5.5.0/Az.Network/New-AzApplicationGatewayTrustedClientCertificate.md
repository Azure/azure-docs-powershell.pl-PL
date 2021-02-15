---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193675"
---
# <span data-ttu-id="ad95c-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ad95c-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="ad95c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad95c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad95c-103">Tworzy łańcuch certyfikatów zaufanego urzędu certyfikacji klienta dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ad95c-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="ad95c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad95c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad95c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad95c-105">DESCRIPTION</span></span>
<span data-ttu-id="ad95c-106">Polecenie New-AzApplicationGatewayTrustedClientCertificate cmdlet tworzy łańcuch certyfikatów zaufanego urzędu certyfikacji klienta dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ad95c-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="ad95c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad95c-107">EXAMPLES</span></span>

### <span data-ttu-id="ad95c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad95c-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="ad95c-109">Polecenie tworzy nowy obiekt łańcucha certyfikatów zaufanego urzędu certyfikacji klienta, który przyjmuje ścieżkę certyfikatu urzędu certyfikacji klienta jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="ad95c-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="ad95c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad95c-110">PARAMETERS</span></span>

### <span data-ttu-id="ad95c-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ad95c-111">-CertificateFile</span></span>
<span data-ttu-id="ad95c-112">Ścieżka pliku zaufanego łańcucha certyfikatów urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="ad95c-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="ad95c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad95c-113">-DefaultProfile</span></span>
<span data-ttu-id="ad95c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad95c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad95c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad95c-115">-Name</span></span>
<span data-ttu-id="ad95c-116">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="ad95c-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="ad95c-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad95c-117">-Confirm</span></span>
<span data-ttu-id="ad95c-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ad95c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad95c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad95c-119">-WhatIf</span></span>
<span data-ttu-id="ad95c-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad95c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad95c-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ad95c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad95c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad95c-122">CommonParameters</span></span>
<span data-ttu-id="ad95c-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad95c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad95c-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad95c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad95c-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad95c-125">INPUTS</span></span>

### <span data-ttu-id="ad95c-126">Brak</span><span class="sxs-lookup"><span data-stu-id="ad95c-126">None</span></span>

## <span data-ttu-id="ad95c-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad95c-127">OUTPUTS</span></span>

### <span data-ttu-id="ad95c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ad95c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="ad95c-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad95c-129">NOTES</span></span>

## <span data-ttu-id="ad95c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad95c-130">RELATED LINKS</span></span>

[<span data-ttu-id="ad95c-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ad95c-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ad95c-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ad95c-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ad95c-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ad95c-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ad95c-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ad95c-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)