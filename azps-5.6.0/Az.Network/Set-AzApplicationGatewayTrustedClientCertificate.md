---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 3c9b9b97e26738234acdf2c8f09c0e1da5eae2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952145"
---
# <span data-ttu-id="74197-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="74197-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="74197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74197-102">SYNOPSIS</span></span>
<span data-ttu-id="74197-103">Modyfikuje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="74197-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="74197-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74197-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74197-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="74197-105">DESCRIPTION</span></span>
<span data-ttu-id="74197-106">Polecenie **cmdlet Set-AzApplicationGatewayTrustedClientCertificate** modyfikuje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="74197-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="74197-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74197-107">EXAMPLES</span></span>

### <span data-ttu-id="74197-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74197-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="74197-109">Powyżej przykładowych scenariuszy pokazano, jak zaktualizować istniejący obiekt łańcucha certyfikatów zaufanego urzędu certyfikacji klienta.</span><span class="sxs-lookup"><span data-stu-id="74197-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="74197-110">Pierwsze polecenie otrzymuje bramę aplikacji i zapisuje je w $gw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="74197-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="74197-111">Drugie polecenie modyfikuje istniejący obiekt łańcucha certyfikatów zaufanego urzędu certyfikacji klienta przy użyciu nowego pliku łańcucha certyfikatów urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="74197-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="74197-112">Trzecie polecenie aktualizuje bramę aplikacji na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="74197-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="74197-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74197-113">PARAMETERS</span></span>

### <span data-ttu-id="74197-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74197-114">-ApplicationGateway</span></span>
<span data-ttu-id="74197-115">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="74197-115">The applicationGateway</span></span>

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

### <span data-ttu-id="74197-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="74197-116">-CertificateFile</span></span>
<span data-ttu-id="74197-117">Ścieżka pliku zaufanego łańcucha certyfikatów urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="74197-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="74197-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74197-118">-DefaultProfile</span></span>
<span data-ttu-id="74197-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74197-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74197-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74197-120">-Name</span></span>
<span data-ttu-id="74197-121">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="74197-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="74197-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74197-122">-Confirm</span></span>
<span data-ttu-id="74197-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74197-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74197-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74197-124">-WhatIf</span></span>
<span data-ttu-id="74197-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74197-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74197-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74197-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74197-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74197-127">CommonParameters</span></span>
<span data-ttu-id="74197-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74197-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74197-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74197-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74197-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74197-130">INPUTS</span></span>

### <span data-ttu-id="74197-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74197-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74197-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74197-132">OUTPUTS</span></span>

### <span data-ttu-id="74197-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74197-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74197-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74197-134">NOTES</span></span>

## <span data-ttu-id="74197-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74197-135">RELATED LINKS</span></span>

[<span data-ttu-id="74197-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="74197-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="74197-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="74197-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="74197-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="74197-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="74197-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="74197-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)