---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 0505f7452c20c0bdb3ccf3a9bc203380479083ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524381"
---
# <span data-ttu-id="e315c-101">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e315c-101">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e315c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e315c-102">SYNOPSIS</span></span>
<span data-ttu-id="e315c-103">Aktualizuje zaufany certyfikat główny bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e315c-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e315c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e315c-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e315c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e315c-105">DESCRIPTION</span></span>
<span data-ttu-id="e315c-106">Polecenie cmdlet **Set-AzureRmApplicationGatewayTrustedRootCertificate** modyfikuje istniejący zaufany certyfikat główny bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e315c-106">The **Set-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="e315c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e315c-107">EXAMPLES</span></span>

### <span data-ttu-id="e315c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e315c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="e315c-109">Powyżej przykładowych scenariuszy pokazano, jak zaktualizować istniejący zaufany certyfikat główny po dowróceniu certyfikatu głównego.</span><span class="sxs-lookup"><span data-stu-id="e315c-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="e315c-110">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="e315c-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="e315c-111">Drugie polecenie modyfikuje istniejący zaufany certyfikat główny z nowym certyfikatem głównym.</span><span class="sxs-lookup"><span data-stu-id="e315c-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="e315c-112">W trzecim poleceniu jest aktualizowana Brama Application Gateway na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e315c-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="e315c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e315c-113">PARAMETERS</span></span>

### <span data-ttu-id="e315c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e315c-114">-ApplicationGateway</span></span>
<span data-ttu-id="e315c-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e315c-115">The applicationGateway</span></span>

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

### <span data-ttu-id="e315c-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e315c-116">-CertificateFile</span></span>
<span data-ttu-id="e315c-117">Ścieżka pliku CER certyfikatu</span><span class="sxs-lookup"><span data-stu-id="e315c-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="e315c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e315c-118">-DefaultProfile</span></span>
<span data-ttu-id="e315c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e315c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e315c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e315c-120">-Name</span></span>
<span data-ttu-id="e315c-121">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="e315c-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="e315c-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e315c-122">-Confirm</span></span>
<span data-ttu-id="e315c-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e315c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e315c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e315c-124">-WhatIf</span></span>
<span data-ttu-id="e315c-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e315c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e315c-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e315c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e315c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e315c-127">CommonParameters</span></span>
<span data-ttu-id="e315c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e315c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e315c-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e315c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e315c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e315c-130">INPUTS</span></span>

### <span data-ttu-id="e315c-131">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e315c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e315c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e315c-132">OUTPUTS</span></span>

### <span data-ttu-id="e315c-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e315c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e315c-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e315c-134">NOTES</span></span>

## <span data-ttu-id="e315c-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e315c-135">RELATED LINKS</span></span>
