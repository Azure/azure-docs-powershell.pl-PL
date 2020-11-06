---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5f71f9a28eb1daae1bee070907675c87002241f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554069"
---
# <span data-ttu-id="2fda0-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2fda0-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="2fda0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fda0-102">SYNOPSIS</span></span>
<span data-ttu-id="2fda0-103">Tworzy zaufany certyfikat główny dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2fda0-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fda0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fda0-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fda0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2fda0-105">DESCRIPTION</span></span>
<span data-ttu-id="2fda0-106">Polecenie cmdlet **New-AzureRmApplicationGatewayTrustedRootCertificate** tworzy zaufany certyfikat główny dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2fda0-106">The **New-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="2fda0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fda0-107">EXAMPLES</span></span>

### <span data-ttu-id="2fda0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2fda0-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzureRmApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="2fda0-109">To polecenie tworzy zaufany certyfikat główny o nazwie Lista "trc1" i zapisuje wynik w zmiennej o nazwie $trc.</span><span class="sxs-lookup"><span data-stu-id="2fda0-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="2fda0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fda0-110">PARAMETERS</span></span>

### <span data-ttu-id="2fda0-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="2fda0-111">-CertificateFile</span></span>
<span data-ttu-id="2fda0-112">Ścieżka pliku CER certyfikatu</span><span class="sxs-lookup"><span data-stu-id="2fda0-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="2fda0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fda0-113">-DefaultProfile</span></span>
<span data-ttu-id="2fda0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fda0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fda0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2fda0-115">-Name</span></span>
<span data-ttu-id="2fda0-116">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="2fda0-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="2fda0-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2fda0-117">-Confirm</span></span>
<span data-ttu-id="2fda0-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fda0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fda0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fda0-119">-WhatIf</span></span>
<span data-ttu-id="2fda0-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fda0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fda0-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2fda0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fda0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fda0-122">CommonParameters</span></span>
<span data-ttu-id="2fda0-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fda0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fda0-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fda0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fda0-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fda0-125">INPUTS</span></span>

### <span data-ttu-id="2fda0-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2fda0-126">None</span></span>

## <span data-ttu-id="2fda0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fda0-127">OUTPUTS</span></span>

### <span data-ttu-id="2fda0-128">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2fda0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="2fda0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fda0-129">NOTES</span></span>

## <span data-ttu-id="2fda0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fda0-130">RELATED LINKS</span></span>
