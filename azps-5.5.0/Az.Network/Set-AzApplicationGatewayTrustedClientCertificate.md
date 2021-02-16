---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186890"
---
# <span data-ttu-id="95d5d-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="95d5d-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="95d5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="95d5d-103">Modyfikuje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="95d5d-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="95d5d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="95d5d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d5d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="95d5d-105">DESCRIPTION</span></span>
<span data-ttu-id="95d5d-106">Polecenie **cmdlet Set-AzApplicationGatewayTrustedClientCertificate** modyfikuje łańcuch certyfikatów zaufanego urzędu certyfikacji klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="95d5d-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="95d5d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="95d5d-107">EXAMPLES</span></span>

### <span data-ttu-id="95d5d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="95d5d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="95d5d-109">W powyższych przykładowych scenariuszach pokazano, jak zaktualizować istniejący obiekt łańcucha certyfikatów zaufanego urzędu certyfikacji klienta.</span><span class="sxs-lookup"><span data-stu-id="95d5d-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="95d5d-110">Pierwsze polecenie pobiera bramę aplikacji i przechowuje je w $gw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="95d5d-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="95d5d-111">Drugie polecenie modyfikuje istniejący obiekt łańcucha certyfikatów zaufanego urzędu certyfikacji klienta przy użyciu nowego pliku łańcucha certyfikatów urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="95d5d-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="95d5d-112">Trzecie polecenie aktualizuje bramę aplikacji na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="95d5d-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="95d5d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95d5d-113">PARAMETERS</span></span>

### <span data-ttu-id="95d5d-114">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95d5d-114">-ApplicationGateway</span></span>
<span data-ttu-id="95d5d-115">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="95d5d-115">The applicationGateway</span></span>

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

### <span data-ttu-id="95d5d-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="95d5d-116">-CertificateFile</span></span>
<span data-ttu-id="95d5d-117">Ścieżka pliku zaufanego łańcucha certyfikatów urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="95d5d-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="95d5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d5d-118">-DefaultProfile</span></span>
<span data-ttu-id="95d5d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="95d5d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95d5d-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="95d5d-120">-Name</span></span>
<span data-ttu-id="95d5d-121">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="95d5d-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="95d5d-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95d5d-122">-Confirm</span></span>
<span data-ttu-id="95d5d-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="95d5d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d5d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d5d-124">-WhatIf</span></span>
<span data-ttu-id="95d5d-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95d5d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95d5d-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="95d5d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d5d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d5d-127">CommonParameters</span></span>
<span data-ttu-id="95d5d-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d5d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d5d-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95d5d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d5d-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95d5d-130">INPUTS</span></span>

### <span data-ttu-id="95d5d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95d5d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95d5d-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95d5d-132">OUTPUTS</span></span>

### <span data-ttu-id="95d5d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95d5d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95d5d-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="95d5d-134">NOTES</span></span>

## <span data-ttu-id="95d5d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95d5d-135">RELATED LINKS</span></span>

[<span data-ttu-id="95d5d-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="95d5d-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="95d5d-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="95d5d-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="95d5d-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="95d5d-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="95d5d-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="95d5d-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)