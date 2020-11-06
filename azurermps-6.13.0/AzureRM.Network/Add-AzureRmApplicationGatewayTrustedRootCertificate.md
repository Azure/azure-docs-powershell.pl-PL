---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e44136d5fa9b0a6b0b979005c13faf6041d98f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551192"
---
# <span data-ttu-id="fb4e2-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fb4e2-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="fb4e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4e2-103">Dodaje zaufany certyfikat główny do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-103">Adds a trusted root certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb4e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb4e2-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb4e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fb4e2-105">DESCRIPTION</span></span>
<span data-ttu-id="fb4e2-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayTrustedRootCertificate** umożliwia dodanie zaufanego certyfikatu głównego do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-106">The **Add-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="fb4e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb4e2-107">EXAMPLES</span></span>

### <span data-ttu-id="fb4e2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb4e2-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzureRmApplicationGatewayBackendHttpSetting -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="fb4e2-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="fb4e2-110">Drugie polecenie addes nowego zaufanego certyfikatu głównego w celu podjęcia ścieżki głównego certyfikatu jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="fb4e2-111">Trzecie polecenie tworzy nowe ustawienie http zaplecza przy użyciu zaufanego certyfikatu głównego, aby sprawdzić poprawność certyfikatu serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="fb4e2-112">Polecenie Fouth aktualizuje bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="fb4e2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb4e2-113">PARAMETERS</span></span>

### <span data-ttu-id="fb4e2-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb4e2-114">-ApplicationGateway</span></span>
<span data-ttu-id="fb4e2-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb4e2-115">The applicationGateway</span></span>

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

### <span data-ttu-id="fb4e2-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fb4e2-116">-CertificateFile</span></span>
<span data-ttu-id="fb4e2-117">Ścieżka pliku CER certyfikatu</span><span class="sxs-lookup"><span data-stu-id="fb4e2-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="fb4e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4e2-118">-DefaultProfile</span></span>
<span data-ttu-id="fb4e2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4e2-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb4e2-120">-Name</span></span>
<span data-ttu-id="fb4e2-121">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="fb4e2-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="fb4e2-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb4e2-122">-Confirm</span></span>
<span data-ttu-id="fb4e2-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb4e2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb4e2-124">-WhatIf</span></span>
<span data-ttu-id="fb4e2-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb4e2-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb4e2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4e2-127">CommonParameters</span></span>
<span data-ttu-id="fb4e2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4e2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4e2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4e2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb4e2-130">INPUTS</span></span>

### <span data-ttu-id="fb4e2-131">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb4e2-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb4e2-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb4e2-132">OUTPUTS</span></span>

### <span data-ttu-id="fb4e2-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb4e2-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb4e2-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb4e2-134">NOTES</span></span>

## <span data-ttu-id="fb4e2-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb4e2-135">RELATED LINKS</span></span>
