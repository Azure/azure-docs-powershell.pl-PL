---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 92c71163b922dacb7920fd842f3d662b18607a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548939"
---
# <span data-ttu-id="9aab7-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="9aab7-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="9aab7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9aab7-102">SYNOPSIS</span></span>
<span data-ttu-id="9aab7-103">Pobiera wstępnie zdefiniowane zasady SSL udostępnione przez bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9aab7-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aab7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9aab7-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9aab7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9aab7-105">DESCRIPTION</span></span>
<span data-ttu-id="9aab7-106">Polecenie cmdlet **Get-AzureRmApplicationGatewaySslPredefinedPolicy** umożliwia pobieranie wstępnie zdefiniowanych zasad SSL udostępnionych przez bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9aab7-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="9aab7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9aab7-107">EXAMPLES</span></span>

### <span data-ttu-id="9aab7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9aab7-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="9aab7-109">To polecenie zwraca wszystkie wstępnie zdefiniowane zasady SSL.</span><span class="sxs-lookup"><span data-stu-id="9aab7-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="9aab7-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9aab7-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="9aab7-111">To polecenie zwraca wstępnie zdefiniowane zasady z nazwą AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="9aab7-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="9aab7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9aab7-112">PARAMETERS</span></span>

### <span data-ttu-id="9aab7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aab7-113">-DefaultProfile</span></span>
<span data-ttu-id="9aab7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9aab7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aab7-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9aab7-115">-Name</span></span>
<span data-ttu-id="9aab7-116">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="9aab7-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="9aab7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aab7-117">CommonParameters</span></span>
<span data-ttu-id="9aab7-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aab7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aab7-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aab7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aab7-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9aab7-120">INPUTS</span></span>

### <span data-ttu-id="9aab7-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9aab7-121">None</span></span>

## <span data-ttu-id="9aab7-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9aab7-122">OUTPUTS</span></span>

### <span data-ttu-id="9aab7-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="9aab7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="9aab7-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9aab7-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9aab7-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9aab7-125">NOTES</span></span>

## <span data-ttu-id="9aab7-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9aab7-126">RELATED LINKS</span></span>

