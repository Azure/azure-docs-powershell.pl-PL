---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 746bbc2ec606bff74a49130e356bd531a3f63f8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503194"
---
# <span data-ttu-id="79210-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="79210-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="79210-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79210-102">SYNOPSIS</span></span>
<span data-ttu-id="79210-103">Aktualizuje zaufany certyfikat główny bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79210-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="79210-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79210-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79210-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79210-105">DESCRIPTION</span></span>
<span data-ttu-id="79210-106">Polecenie cmdlet **Set-AzApplicationGatewayTrustedRootCertificate** modyfikuje istniejący zaufany certyfikat główny bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="79210-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="79210-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79210-107">EXAMPLES</span></span>

### <span data-ttu-id="79210-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79210-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="79210-109">Powyżej przykładowych scenariuszy pokazano, jak zaktualizować istniejący zaufany certyfikat główny po dowróceniu certyfikatu głównego.</span><span class="sxs-lookup"><span data-stu-id="79210-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="79210-110">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="79210-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="79210-111">Drugie polecenie modyfikuje istniejący zaufany certyfikat główny z nowym certyfikatem głównym.</span><span class="sxs-lookup"><span data-stu-id="79210-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="79210-112">W trzecim poleceniu jest aktualizowana Brama Application Gateway na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="79210-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="79210-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79210-113">PARAMETERS</span></span>

### <span data-ttu-id="79210-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79210-114">-ApplicationGateway</span></span>
<span data-ttu-id="79210-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79210-115">The applicationGateway</span></span>

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

### <span data-ttu-id="79210-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="79210-116">-CertificateFile</span></span>
<span data-ttu-id="79210-117">Ścieżka pliku CER certyfikatu</span><span class="sxs-lookup"><span data-stu-id="79210-117">Path of certificate CER file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79210-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79210-118">-DefaultProfile</span></span>
<span data-ttu-id="79210-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79210-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79210-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79210-120">-Name</span></span>
<span data-ttu-id="79210-121">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="79210-121">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79210-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79210-122">-Confirm</span></span>
<span data-ttu-id="79210-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79210-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79210-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79210-124">-WhatIf</span></span>
<span data-ttu-id="79210-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79210-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79210-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79210-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79210-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79210-127">CommonParameters</span></span>
<span data-ttu-id="79210-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79210-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79210-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79210-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79210-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79210-130">INPUTS</span></span>

### <span data-ttu-id="79210-131">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79210-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79210-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79210-132">OUTPUTS</span></span>

### <span data-ttu-id="79210-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79210-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79210-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79210-134">NOTES</span></span>

## <span data-ttu-id="79210-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79210-135">RELATED LINKS</span></span>

[<span data-ttu-id="79210-136">Dodaj-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="79210-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="79210-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="79210-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="79210-138">Nowe — AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="79210-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="79210-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="79210-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
