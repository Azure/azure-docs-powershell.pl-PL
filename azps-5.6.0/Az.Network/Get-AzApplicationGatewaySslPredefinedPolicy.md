---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: dda293d8d765470d9ac99c9ce4313422cdb8b72b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994036"
---
# <span data-ttu-id="3dacb-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="3dacb-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="3dacb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dacb-102">SYNOPSIS</span></span>
<span data-ttu-id="3dacb-103">Pobiera wstępnie zdefiniowane zasady SSL udostępniane przez bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dacb-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="3dacb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3dacb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dacb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3dacb-105">DESCRIPTION</span></span>
<span data-ttu-id="3dacb-106">Polecenie **cmdlet Get-AzApplicationGatewaySslPredefinedPolicy** pobiera wstępnie zdefiniowane zasady SSL udostępniane przez bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dacb-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="3dacb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3dacb-107">EXAMPLES</span></span>

### <span data-ttu-id="3dacb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3dacb-108">Example 1</span></span>
```
PS C:\> Get-AzApplicationGatewaySslPredefinedPolicy

Name: AppGwSslPolicy20150501
MinProtocolVersion: TLSv1_0
CipherSuites:
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_DHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_DHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_DHE_RSA_WITH_AES_256_CBC_SHA
    TLS_DHE_RSA_WITH_AES_128_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_DHE_DSS_WITH_AES_256_CBC_SHA256
    TLS_DHE_DSS_WITH_AES_128_CBC_SHA256
    TLS_DHE_DSS_WITH_AES_256_CBC_SHA
    TLS_DHE_DSS_WITH_AES_128_CBC_SHA
    TLS_RSA_WITH_3DES_EDE_CBC_SHA
    TLS_DHE_DSS_WITH_3DES_EDE_CBC_SHA


Name: AppGwSslPolicy20170401
MinProtocolVersion: TLSv1_1
CipherSuites:
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA


Name: AppGwSslPolicy20170401S
MinProtocolVersion: TLSv1_2
CipherSuites:
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA
```

<span data-ttu-id="3dacb-109">To polecenia zwraca wszystkie wstępnie zdefiniowane zasady SSL.</span><span class="sxs-lookup"><span data-stu-id="3dacb-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="3dacb-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3dacb-110">Example 2</span></span>
```
PS C:\> Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401

Name: AppGwSslPolicy20170401
MinProtocolVersion: TLSv1_1
CipherSuites:
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA
```

<span data-ttu-id="3dacb-111">To polecenia zwraca wstępnie zdefiniowane zasady o nazwie AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="3dacb-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

### <span data-ttu-id="3dacb-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3dacb-112">Example 3</span></span>
```
PS C:\> Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy2017*

Name: AppGwSslPolicy20170401
MinProtocolVersion: TLSv1_1
CipherSuites:
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA


Name: AppGwSslPolicy20170401S
MinProtocolVersion: TLSv1_2
CipherSuites:
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA
```

<span data-ttu-id="3dacb-113">To polecenia zwraca wstępnie zdefiniowane zasady o nazwie zaczynającej się od "AppGwSslPolicy2017".</span><span class="sxs-lookup"><span data-stu-id="3dacb-113">This commands returns predefined policy with name starting with "AppGwSslPolicy2017".</span></span>

## <span data-ttu-id="3dacb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dacb-114">PARAMETERS</span></span>

### <span data-ttu-id="3dacb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dacb-115">-DefaultProfile</span></span>
<span data-ttu-id="3dacb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3dacb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dacb-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3dacb-117">-Name</span></span>
<span data-ttu-id="3dacb-118">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="3dacb-118">Name of the ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="3dacb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dacb-119">CommonParameters</span></span>
<span data-ttu-id="3dacb-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dacb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dacb-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3dacb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dacb-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dacb-122">INPUTS</span></span>

### <span data-ttu-id="3dacb-123">Brak</span><span class="sxs-lookup"><span data-stu-id="3dacb-123">None</span></span>

## <span data-ttu-id="3dacb-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dacb-124">OUTPUTS</span></span>

### <span data-ttu-id="3dacb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="3dacb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="3dacb-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3dacb-126">NOTES</span></span>

## <span data-ttu-id="3dacb-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dacb-127">RELATED LINKS</span></span>
