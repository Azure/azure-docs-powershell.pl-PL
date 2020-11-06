---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 82713c41d6f2e3882c50ffbd5ab6b276a90dc2e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550295"
---
# <span data-ttu-id="64750-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="64750-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="64750-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64750-102">SYNOPSIS</span></span>
<span data-ttu-id="64750-103">Pobiera wstępnie zdefiniowane zasady SSL udostępnione przez bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="64750-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64750-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64750-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64750-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64750-105">DESCRIPTION</span></span>
<span data-ttu-id="64750-106">Polecenie cmdlet **Get-AzureRmApplicationGatewaySslPredefinedPolicy** umożliwia pobieranie wstępnie zdefiniowanych zasad SSL udostępnionych przez bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="64750-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="64750-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64750-107">EXAMPLES</span></span>

### <span data-ttu-id="64750-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64750-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="64750-109">To polecenie zwraca wszystkie wstępnie zdefiniowane zasady SSL.</span><span class="sxs-lookup"><span data-stu-id="64750-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="64750-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="64750-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="64750-111">To polecenie zwraca wstępnie zdefiniowane zasady z nazwą AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="64750-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="64750-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64750-112">PARAMETERS</span></span>

### <span data-ttu-id="64750-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64750-113">-DefaultProfile</span></span>
<span data-ttu-id="64750-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64750-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64750-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64750-115">-Name</span></span>
<span data-ttu-id="64750-116">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="64750-116">Name of the ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64750-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64750-117">CommonParameters</span></span>
<span data-ttu-id="64750-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64750-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64750-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64750-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64750-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64750-120">INPUTS</span></span>

### <span data-ttu-id="64750-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="64750-121">None</span></span>

## <span data-ttu-id="64750-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64750-122">OUTPUTS</span></span>

### <span data-ttu-id="64750-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="64750-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="64750-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64750-124">NOTES</span></span>

## <span data-ttu-id="64750-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64750-125">RELATED LINKS</span></span>
