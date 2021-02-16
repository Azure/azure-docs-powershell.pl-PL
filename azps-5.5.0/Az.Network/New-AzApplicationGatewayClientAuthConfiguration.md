---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 68ab3fbd87e5fe28fffdd0f6d769fb21d0ce9e6e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398091"
---
# <span data-ttu-id="08e4d-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="08e4d-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="08e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="08e4d-103">Tworzy nową konfigurację uwierzytelniania klienta dla profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="08e4d-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="08e4d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="08e4d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e4d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="08e4d-105">DESCRIPTION</span></span>
<span data-ttu-id="08e4d-106">Polecenie **cmdlet New-AzApplicationGatewayClientAuthConfiguration** tworzy nową konfigurację uwierzytelniania klienta dla profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="08e4d-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="08e4d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="08e4d-107">EXAMPLES</span></span>

### <span data-ttu-id="08e4d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="08e4d-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="08e4d-109">Polecenie tworzy nową konfigurację uwierzytelniania klienta i przechowuje ją w $clientAuthConfig, która ma być używana w profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="08e4d-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="08e4d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08e4d-110">PARAMETERS</span></span>

### <span data-ttu-id="08e4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e4d-111">-DefaultProfile</span></span>
<span data-ttu-id="08e4d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="08e4d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08e4d-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="08e4d-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="08e4d-114">Sprawdź nazwę wystawcy certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="08e4d-114">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e4d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e4d-115">CommonParameters</span></span>
<span data-ttu-id="08e4d-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e4d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e4d-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08e4d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e4d-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08e4d-118">INPUTS</span></span>

### <span data-ttu-id="08e4d-119">Brak</span><span class="sxs-lookup"><span data-stu-id="08e4d-119">None</span></span>

## <span data-ttu-id="08e4d-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="08e4d-120">OUTPUTS</span></span>

### <span data-ttu-id="08e4d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="08e4d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="08e4d-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="08e4d-122">NOTES</span></span>

## <span data-ttu-id="08e4d-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08e4d-123">RELATED LINKS</span></span>


[<span data-ttu-id="08e4d-124">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="08e4d-124">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="08e4d-125">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="08e4d-125">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="08e4d-126">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="08e4d-126">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
