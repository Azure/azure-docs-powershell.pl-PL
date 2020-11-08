---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234021"
---
# <span data-ttu-id="ebe18-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="ebe18-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="ebe18-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebe18-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe18-103">Wyświetla listę wersji SKU typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="ebe18-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="ebe18-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebe18-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ebe18-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ebe18-105">DESCRIPTION</span></span>
<span data-ttu-id="ebe18-106">Wyświetla listę wersji SKU typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="ebe18-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="ebe18-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebe18-107">EXAMPLES</span></span>

### <span data-ttu-id="ebe18-108">Przykład 1: Lista SKU dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ebe18-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="ebe18-109">To polecenie wyświetla listę jednostek SKU subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ebe18-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="ebe18-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebe18-110">PARAMETERS</span></span>

### <span data-ttu-id="ebe18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe18-111">-DefaultProfile</span></span>
<span data-ttu-id="ebe18-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe18-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe18-113">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ebe18-113">-SubscriptionId</span></span>
<span data-ttu-id="ebe18-114">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe18-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ebe18-115">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ebe18-115">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe18-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe18-116">CommonParameters</span></span>
<span data-ttu-id="ebe18-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebe18-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe18-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebe18-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe18-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebe18-119">INPUTS</span></span>

## <span data-ttu-id="ebe18-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebe18-120">OUTPUTS</span></span>

### <span data-ttu-id="ebe18-121">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="ebe18-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="ebe18-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebe18-122">NOTES</span></span>

<span data-ttu-id="ebe18-123">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ebe18-123">ALIASES</span></span>

## <span data-ttu-id="ebe18-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebe18-124">RELATED LINKS</span></span>

