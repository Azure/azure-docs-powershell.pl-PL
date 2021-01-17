---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 6e8c3cdbfa1242cba19d3aa3250c4bf4e381ae92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379528"
---
# <span data-ttu-id="90ad2-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ad2-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="90ad2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="90ad2-103">Tworzy nową konfigurację uwierzytelniania klienta dla profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="90ad2-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="90ad2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90ad2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90ad2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="90ad2-106">Polecenie cmdlet **New-AzApplicationGatewayClientAuthConfiguration** tworzy nową konfigurację uwierzytelniania klienta dla profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="90ad2-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="90ad2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90ad2-107">EXAMPLES</span></span>

### <span data-ttu-id="90ad2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90ad2-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="90ad2-109">Polecenie tworzy nową konfigurację uwierzytelniania klienta i zapisuje ją w $clientAuthConfig zmiennej, która ma być używana w profilu SSL.</span><span class="sxs-lookup"><span data-stu-id="90ad2-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="90ad2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90ad2-110">PARAMETERS</span></span>

### <span data-ttu-id="90ad2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ad2-111">-DefaultProfile</span></span>
<span data-ttu-id="90ad2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90ad2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90ad2-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="90ad2-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="90ad2-114">Sprawdź nazwę wystawcy certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="90ad2-114">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="90ad2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ad2-115">CommonParameters</span></span>
<span data-ttu-id="90ad2-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ad2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ad2-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90ad2-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ad2-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90ad2-118">INPUTS</span></span>

### <span data-ttu-id="90ad2-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="90ad2-119">None</span></span>

## <span data-ttu-id="90ad2-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90ad2-120">OUTPUTS</span></span>

### <span data-ttu-id="90ad2-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ad2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="90ad2-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90ad2-122">NOTES</span></span>

## <span data-ttu-id="90ad2-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90ad2-123">RELATED LINKS</span></span>

[<span data-ttu-id="90ad2-124">Dodaj-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ad2-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="90ad2-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ad2-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="90ad2-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ad2-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="90ad2-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="90ad2-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)