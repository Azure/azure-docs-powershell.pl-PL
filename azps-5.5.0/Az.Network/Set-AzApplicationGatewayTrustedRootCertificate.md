---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 746bbc2ec606bff74a49130e356bd531a3f63f8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179378"
---
# <span data-ttu-id="469c3-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="469c3-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="469c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="469c3-102">SYNOPSIS</span></span>
<span data-ttu-id="469c3-103">Aktualizuje zaufany certyfikat główny bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="469c3-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="469c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="469c3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="469c3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="469c3-105">DESCRIPTION</span></span>
<span data-ttu-id="469c3-106">Polecenie **cmdlet Set-AzApplicationGatewayTrustedRootCertificate** modyfikuje istniejący zaufany certyfikat główny bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="469c3-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="469c3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="469c3-107">EXAMPLES</span></span>

### <span data-ttu-id="469c3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="469c3-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="469c3-109">W powyższych przykładowych scenariuszach pokazano, jak zaktualizować istniejący zaufany certyfikat główny podczas rzutowania certyfikatu głównego.</span><span class="sxs-lookup"><span data-stu-id="469c3-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="469c3-110">Pierwsze polecenie pobiera bramę aplikacji i zapisuje je w $gw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="469c3-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="469c3-111">Drugie polecenie modyfikuje istniejący zaufany certyfikat główny przy użyciu nowego certyfikatu głównego.</span><span class="sxs-lookup"><span data-stu-id="469c3-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="469c3-112">Trzecie polecenie aktualizuje bramę aplikacji na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="469c3-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="469c3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="469c3-113">PARAMETERS</span></span>

### <span data-ttu-id="469c3-114">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="469c3-114">-ApplicationGateway</span></span>
<span data-ttu-id="469c3-115">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="469c3-115">The applicationGateway</span></span>

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

### <span data-ttu-id="469c3-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="469c3-116">-CertificateFile</span></span>
<span data-ttu-id="469c3-117">Ścieżka pliku CER certyfikatu</span><span class="sxs-lookup"><span data-stu-id="469c3-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="469c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="469c3-118">-DefaultProfile</span></span>
<span data-ttu-id="469c3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="469c3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="469c3-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="469c3-120">-Name</span></span>
<span data-ttu-id="469c3-121">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="469c3-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="469c3-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="469c3-122">-Confirm</span></span>
<span data-ttu-id="469c3-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="469c3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="469c3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="469c3-124">-WhatIf</span></span>
<span data-ttu-id="469c3-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="469c3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="469c3-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="469c3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="469c3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469c3-127">CommonParameters</span></span>
<span data-ttu-id="469c3-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="469c3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469c3-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="469c3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469c3-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="469c3-130">INPUTS</span></span>

### <span data-ttu-id="469c3-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="469c3-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="469c3-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="469c3-132">OUTPUTS</span></span>

### <span data-ttu-id="469c3-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="469c3-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="469c3-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="469c3-134">NOTES</span></span>

## <span data-ttu-id="469c3-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="469c3-135">RELATED LINKS</span></span>

[<span data-ttu-id="469c3-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="469c3-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="469c3-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="469c3-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="469c3-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="469c3-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="469c3-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="469c3-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
