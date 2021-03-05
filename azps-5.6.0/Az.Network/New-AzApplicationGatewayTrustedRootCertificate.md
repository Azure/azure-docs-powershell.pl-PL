---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: bacdca3f26e18f3dc41ac19990e48f9e6bb63c1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970490"
---
# <span data-ttu-id="f096a-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f096a-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f096a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f096a-102">SYNOPSIS</span></span>
<span data-ttu-id="f096a-103">Tworzy zaufany certyfikat główny dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f096a-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="f096a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f096a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f096a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f096a-105">DESCRIPTION</span></span>
<span data-ttu-id="f096a-106">Polecenie **cmdlet New-AzApplicationGatewayTrustedRootCertificate** tworzy zaufany certyfikat główny dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f096a-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="f096a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f096a-107">EXAMPLES</span></span>

### <span data-ttu-id="f096a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f096a-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="f096a-109">To polecenie tworzy zaufany certyfikat główny o nazwie Lista "trc1" i przechowuje wynik w zmiennej o nazwie $trc.</span><span class="sxs-lookup"><span data-stu-id="f096a-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="f096a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f096a-110">PARAMETERS</span></span>

### <span data-ttu-id="f096a-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f096a-111">-CertificateFile</span></span>
<span data-ttu-id="f096a-112">Ścieżka pliku CER certyfikatu</span><span class="sxs-lookup"><span data-stu-id="f096a-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="f096a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f096a-113">-DefaultProfile</span></span>
<span data-ttu-id="f096a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f096a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f096a-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f096a-115">-Name</span></span>
<span data-ttu-id="f096a-116">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="f096a-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="f096a-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f096a-117">-Confirm</span></span>
<span data-ttu-id="f096a-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f096a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f096a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f096a-119">-WhatIf</span></span>
<span data-ttu-id="f096a-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f096a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f096a-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f096a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f096a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f096a-122">CommonParameters</span></span>
<span data-ttu-id="f096a-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f096a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f096a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f096a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f096a-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f096a-125">INPUTS</span></span>

### <span data-ttu-id="f096a-126">Brak</span><span class="sxs-lookup"><span data-stu-id="f096a-126">None</span></span>

## <span data-ttu-id="f096a-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f096a-127">OUTPUTS</span></span>

### <span data-ttu-id="f096a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f096a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f096a-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f096a-129">NOTES</span></span>

## <span data-ttu-id="f096a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f096a-130">RELATED LINKS</span></span>

[<span data-ttu-id="f096a-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f096a-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f096a-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f096a-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f096a-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f096a-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f096a-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f096a-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
