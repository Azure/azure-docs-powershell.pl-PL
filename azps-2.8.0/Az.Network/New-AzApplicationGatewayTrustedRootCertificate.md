---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 473e759e43c59c48b9e47706ac55b388379b6d6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870495"
---
# <span data-ttu-id="fa927-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fa927-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="fa927-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa927-102">SYNOPSIS</span></span>
<span data-ttu-id="fa927-103">Tworzy zaufany certyfikat główny dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fa927-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="fa927-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa927-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa927-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fa927-105">DESCRIPTION</span></span>
<span data-ttu-id="fa927-106">Polecenie cmdlet **New-AzApplicationGatewayTrustedRootCertificate** tworzy zaufany certyfikat główny dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fa927-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="fa927-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa927-107">EXAMPLES</span></span>

### <span data-ttu-id="fa927-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa927-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="fa927-109">To polecenie tworzy zaufany certyfikat główny o nazwie Lista "trc1" i zapisuje wynik w zmiennej o nazwie $trc.</span><span class="sxs-lookup"><span data-stu-id="fa927-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="fa927-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa927-110">PARAMETERS</span></span>

### <span data-ttu-id="fa927-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fa927-111">-CertificateFile</span></span>
<span data-ttu-id="fa927-112">Ścieżka pliku CER certyfikatu</span><span class="sxs-lookup"><span data-stu-id="fa927-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="fa927-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa927-113">-DefaultProfile</span></span>
<span data-ttu-id="fa927-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa927-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa927-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa927-115">-Name</span></span>
<span data-ttu-id="fa927-116">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="fa927-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="fa927-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa927-117">-Confirm</span></span>
<span data-ttu-id="fa927-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa927-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa927-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa927-119">-WhatIf</span></span>
<span data-ttu-id="fa927-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa927-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa927-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa927-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa927-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa927-122">CommonParameters</span></span>
<span data-ttu-id="fa927-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa927-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa927-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa927-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa927-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa927-125">INPUTS</span></span>

### <span data-ttu-id="fa927-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fa927-126">None</span></span>

## <span data-ttu-id="fa927-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa927-127">OUTPUTS</span></span>

### <span data-ttu-id="fa927-128">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fa927-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="fa927-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa927-129">NOTES</span></span>

## <span data-ttu-id="fa927-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa927-130">RELATED LINKS</span></span>

[<span data-ttu-id="fa927-131">Dodaj-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fa927-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="fa927-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fa927-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="fa927-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fa927-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="fa927-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fa927-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
