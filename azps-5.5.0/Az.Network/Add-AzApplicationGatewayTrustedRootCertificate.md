---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f5e8624beeb8053cbf054526cddc24c7da6cdf3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192034"
---
# <span data-ttu-id="560d9-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="560d9-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="560d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="560d9-102">SYNOPSIS</span></span>
<span data-ttu-id="560d9-103">Dodaje zaufany certyfikat główny do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="560d9-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="560d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="560d9-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="560d9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="560d9-105">DESCRIPTION</span></span>
<span data-ttu-id="560d9-106">Polecenie **cmdlet Add-AzApplicationGatewayTrustedRootCertificate** dodaje zaufany certyfikat główny do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="560d9-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="560d9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="560d9-107">EXAMPLES</span></span>

### <span data-ttu-id="560d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="560d9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="560d9-109">Pierwsze polecenie pobiera bramę aplikacji i przechowuje ją w $gw zmienną.</span><span class="sxs-lookup"><span data-stu-id="560d9-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="560d9-110">Drugie polecenie dodaje nowy zaufany certyfikat główny do bramy aplikacji, która przyjmuje ścieżkę certyfikatu głównego jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="560d9-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="560d9-111">Trzecie polecenie tworzy nowe ustawienie http zaplecza przy użyciu zaufanego certyfikatu głównego do sprawdzania poprawności certyfikatu serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="560d9-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="560d9-112">Czwarte polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="560d9-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="560d9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="560d9-113">PARAMETERS</span></span>

### <span data-ttu-id="560d9-114">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="560d9-114">-ApplicationGateway</span></span>
<span data-ttu-id="560d9-115">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="560d9-115">The applicationGateway</span></span>

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

### <span data-ttu-id="560d9-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="560d9-116">-CertificateFile</span></span>
<span data-ttu-id="560d9-117">Ścieżka pliku CER certyfikatu</span><span class="sxs-lookup"><span data-stu-id="560d9-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="560d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560d9-118">-DefaultProfile</span></span>
<span data-ttu-id="560d9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="560d9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="560d9-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="560d9-120">-Name</span></span>
<span data-ttu-id="560d9-121">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="560d9-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="560d9-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="560d9-122">-Confirm</span></span>
<span data-ttu-id="560d9-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="560d9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="560d9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="560d9-124">-WhatIf</span></span>
<span data-ttu-id="560d9-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="560d9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="560d9-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="560d9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="560d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560d9-127">CommonParameters</span></span>
<span data-ttu-id="560d9-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="560d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560d9-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="560d9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560d9-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="560d9-130">INPUTS</span></span>

### <span data-ttu-id="560d9-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="560d9-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="560d9-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="560d9-132">OUTPUTS</span></span>

### <span data-ttu-id="560d9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="560d9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="560d9-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="560d9-134">NOTES</span></span>

## <span data-ttu-id="560d9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="560d9-135">RELATED LINKS</span></span>

[<span data-ttu-id="560d9-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="560d9-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="560d9-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="560d9-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="560d9-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="560d9-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="560d9-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="560d9-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
