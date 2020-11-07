---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 2c55da6b7193d02de51e273df4626152d6d088fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890842"
---
# <span data-ttu-id="4f943-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="4f943-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="4f943-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f943-102">SYNOPSIS</span></span>
<span data-ttu-id="4f943-103">Pobiera wstępnie zdefiniowane zasady SSL udostępnione przez bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f943-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="4f943-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f943-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f943-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4f943-105">DESCRIPTION</span></span>
<span data-ttu-id="4f943-106">Polecenie cmdlet **Get-AzApplicationGatewaySslPredefinedPolicy** umożliwia pobieranie wstępnie zdefiniowanych zasad SSL udostępnionych przez bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f943-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="4f943-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f943-107">EXAMPLES</span></span>

### <span data-ttu-id="4f943-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4f943-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="4f943-109">To polecenie zwraca wszystkie wstępnie zdefiniowane zasady SSL.</span><span class="sxs-lookup"><span data-stu-id="4f943-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="4f943-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4f943-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="4f943-111">To polecenie zwraca wstępnie zdefiniowane zasady z nazwą AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="4f943-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="4f943-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f943-112">PARAMETERS</span></span>

### <span data-ttu-id="4f943-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f943-113">-DefaultProfile</span></span>
<span data-ttu-id="4f943-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f943-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f943-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4f943-115">-Name</span></span>
<span data-ttu-id="4f943-116">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="4f943-116">Name of the ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f943-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f943-117">CommonParameters</span></span>
<span data-ttu-id="4f943-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f943-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f943-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f943-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f943-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f943-120">INPUTS</span></span>

### <span data-ttu-id="4f943-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4f943-121">None</span></span>

## <span data-ttu-id="4f943-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f943-122">OUTPUTS</span></span>

### <span data-ttu-id="4f943-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="4f943-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="4f943-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4f943-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4f943-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f943-125">NOTES</span></span>

## <span data-ttu-id="4f943-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f943-126">RELATED LINKS</span></span>

