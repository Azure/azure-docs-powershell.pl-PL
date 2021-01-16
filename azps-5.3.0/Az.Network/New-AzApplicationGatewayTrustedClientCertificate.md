---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491066"
---
# <span data-ttu-id="4fca9-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4fca9-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="4fca9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fca9-102">SYNOPSIS</span></span>
<span data-ttu-id="4fca9-103">Tworzy łańcuch certyfikatów zaufanego urzędu certyfikacji klienta dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4fca9-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="4fca9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fca9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fca9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4fca9-105">DESCRIPTION</span></span>
<span data-ttu-id="4fca9-106">Polecenie cmdlet New-AzApplicationGatewayTrustedClientCertificate tworzy łańcuch certyfikatów zaufanego urzędu certyfikacji klienta dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4fca9-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="4fca9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fca9-107">EXAMPLES</span></span>

### <span data-ttu-id="4fca9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4fca9-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="4fca9-109">Polecenie tworzy nowy obiekt łańcucha certyfikatu zaufanego urzędu certyfikacji klienta, uwzględniając ścieżkę certyfikatu urzędu certyfikacji klienta jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="4fca9-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="4fca9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fca9-110">PARAMETERS</span></span>

### <span data-ttu-id="4fca9-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4fca9-111">-CertificateFile</span></span>
<span data-ttu-id="4fca9-112">Ścieżka pliku łańcucha certyfikatu zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="4fca9-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="4fca9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fca9-113">-DefaultProfile</span></span>
<span data-ttu-id="4fca9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fca9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fca9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4fca9-115">-Name</span></span>
<span data-ttu-id="4fca9-116">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="4fca9-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="4fca9-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4fca9-117">-Confirm</span></span>
<span data-ttu-id="4fca9-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fca9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fca9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fca9-119">-WhatIf</span></span>
<span data-ttu-id="4fca9-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fca9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fca9-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4fca9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fca9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fca9-122">CommonParameters</span></span>
<span data-ttu-id="4fca9-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fca9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fca9-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fca9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fca9-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fca9-125">INPUTS</span></span>

### <span data-ttu-id="4fca9-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4fca9-126">None</span></span>

## <span data-ttu-id="4fca9-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fca9-127">OUTPUTS</span></span>

### <span data-ttu-id="4fca9-128">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4fca9-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="4fca9-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fca9-129">NOTES</span></span>

## <span data-ttu-id="4fca9-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fca9-130">RELATED LINKS</span></span>

[<span data-ttu-id="4fca9-131">Dodaj-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4fca9-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4fca9-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4fca9-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4fca9-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4fca9-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4fca9-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4fca9-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)