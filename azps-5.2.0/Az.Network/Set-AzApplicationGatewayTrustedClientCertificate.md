---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336565"
---
# <span data-ttu-id="56931-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="56931-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="56931-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56931-102">SYNOPSIS</span></span>
<span data-ttu-id="56931-103">Modyfikuje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta w bramie Application.</span><span class="sxs-lookup"><span data-stu-id="56931-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="56931-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56931-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56931-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56931-105">DESCRIPTION</span></span>
<span data-ttu-id="56931-106">Polecenie cmdlet **Set-AzApplicationGatewayTrustedClientCertificate** modyfikuje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta w bramie Application.</span><span class="sxs-lookup"><span data-stu-id="56931-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="56931-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56931-107">EXAMPLES</span></span>

### <span data-ttu-id="56931-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56931-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="56931-109">Powyżej przykładowych scenariuszy pokazano, jak zaktualizować istniejący obiekt łańcucha certyfikatu zaufanego urzędu certyfikacji klienta.</span><span class="sxs-lookup"><span data-stu-id="56931-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="56931-110">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="56931-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="56931-111">Drugie polecenie modyfikuje istniejący obiekt łańcuchowy certyfikatu zaufanego urzędu certyfikacji klienta za pomocą nowego pliku łańcucha certyfikatów urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="56931-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="56931-112">W trzecim poleceniu jest aktualizowana Brama Application Gateway na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="56931-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="56931-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56931-113">PARAMETERS</span></span>

### <span data-ttu-id="56931-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56931-114">-ApplicationGateway</span></span>
<span data-ttu-id="56931-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56931-115">The applicationGateway</span></span>

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

### <span data-ttu-id="56931-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="56931-116">-CertificateFile</span></span>
<span data-ttu-id="56931-117">Ścieżka pliku łańcucha certyfikatu zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="56931-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="56931-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56931-118">-DefaultProfile</span></span>
<span data-ttu-id="56931-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56931-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56931-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56931-120">-Name</span></span>
<span data-ttu-id="56931-121">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="56931-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="56931-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56931-122">-Confirm</span></span>
<span data-ttu-id="56931-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56931-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56931-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56931-124">-WhatIf</span></span>
<span data-ttu-id="56931-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56931-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56931-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56931-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56931-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56931-127">CommonParameters</span></span>
<span data-ttu-id="56931-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56931-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56931-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56931-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56931-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56931-130">INPUTS</span></span>

### <span data-ttu-id="56931-131">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56931-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="56931-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56931-132">OUTPUTS</span></span>

### <span data-ttu-id="56931-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56931-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="56931-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56931-134">NOTES</span></span>

## <span data-ttu-id="56931-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56931-135">RELATED LINKS</span></span>

[<span data-ttu-id="56931-136">Dodaj-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="56931-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="56931-137">Nowe — AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="56931-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="56931-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="56931-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="56931-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="56931-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)