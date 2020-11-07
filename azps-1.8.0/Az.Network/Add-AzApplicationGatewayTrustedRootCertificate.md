---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 9ad926a9dd9a3a13bff1f31cfa1ae7d689cadbb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709692"
---
# <span data-ttu-id="d1aaf-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d1aaf-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d1aaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="d1aaf-103">Dodaje zaufany certyfikat główny do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="d1aaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1aaf-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1aaf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d1aaf-105">DESCRIPTION</span></span>
<span data-ttu-id="d1aaf-106">Polecenie cmdlet **Add-AzApplicationGatewayTrustedRootCertificate** umożliwia dodanie zaufanego certyfikatu głównego do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="d1aaf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1aaf-107">EXAMPLES</span></span>

### <span data-ttu-id="d1aaf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d1aaf-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="d1aaf-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="d1aaf-110">Drugie polecenie addes nowego zaufanego certyfikatu głównego w celu podjęcia ścieżki głównego certyfikatu jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="d1aaf-111">Trzecie polecenie tworzy nowe ustawienie http zaplecza przy użyciu zaufanego certyfikatu głównego, aby sprawdzić poprawność certyfikatu serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="d1aaf-112">Polecenie Fouth aktualizuje bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="d1aaf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1aaf-113">PARAMETERS</span></span>

### <span data-ttu-id="d1aaf-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1aaf-114">-ApplicationGateway</span></span>
<span data-ttu-id="d1aaf-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1aaf-115">The applicationGateway</span></span>

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

### <span data-ttu-id="d1aaf-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d1aaf-116">-CertificateFile</span></span>
<span data-ttu-id="d1aaf-117">Ścieżka pliku CER certyfikatu</span><span class="sxs-lookup"><span data-stu-id="d1aaf-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="d1aaf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1aaf-118">-DefaultProfile</span></span>
<span data-ttu-id="d1aaf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1aaf-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1aaf-120">-Name</span></span>
<span data-ttu-id="d1aaf-121">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="d1aaf-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="d1aaf-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1aaf-122">-Confirm</span></span>
<span data-ttu-id="d1aaf-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1aaf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1aaf-124">-WhatIf</span></span>
<span data-ttu-id="d1aaf-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1aaf-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1aaf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1aaf-127">CommonParameters</span></span>
<span data-ttu-id="d1aaf-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1aaf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1aaf-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1aaf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1aaf-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1aaf-130">INPUTS</span></span>

### <span data-ttu-id="d1aaf-131">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1aaf-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1aaf-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1aaf-132">OUTPUTS</span></span>

### <span data-ttu-id="d1aaf-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1aaf-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1aaf-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1aaf-134">NOTES</span></span>

## <span data-ttu-id="d1aaf-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1aaf-135">RELATED LINKS</span></span>

[<span data-ttu-id="d1aaf-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d1aaf-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d1aaf-137">Nowe — AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d1aaf-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d1aaf-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d1aaf-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d1aaf-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d1aaf-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
