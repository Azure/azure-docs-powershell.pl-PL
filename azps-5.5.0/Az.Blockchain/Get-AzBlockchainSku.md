---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195195"
---
# <span data-ttu-id="6fdc1-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="6fdc1-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="6fdc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fdc1-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdc1-103">Lista jednostki SKU typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="6fdc1-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="6fdc1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6fdc1-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6fdc1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6fdc1-105">DESCRIPTION</span></span>
<span data-ttu-id="6fdc1-106">Lista jednostki SKU typu zasobu.</span><span class="sxs-lookup"><span data-stu-id="6fdc1-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="6fdc1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6fdc1-107">EXAMPLES</span></span>

### <span data-ttu-id="6fdc1-108">Przykład 1. Lista SKU dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6fdc1-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="6fdc1-109">To polecenie zawiera listę SKU dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6fdc1-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="6fdc1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fdc1-110">PARAMETERS</span></span>

### <span data-ttu-id="6fdc1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdc1-111">-DefaultProfile</span></span>
<span data-ttu-id="6fdc1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fdc1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fdc1-113">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6fdc1-113">-SubscriptionId</span></span>
<span data-ttu-id="6fdc1-114">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6fdc1-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6fdc1-115">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="6fdc1-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6fdc1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdc1-116">CommonParameters</span></span>
<span data-ttu-id="6fdc1-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fdc1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdc1-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fdc1-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdc1-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fdc1-119">INPUTS</span></span>

## <span data-ttu-id="6fdc1-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fdc1-120">OUTPUTS</span></span>

### <span data-ttu-id="6fdc1-121">Microsoft.Azure.PowerShell.cmdlet.u7.models.api20180601Preview.IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="6fdc1-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="6fdc1-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6fdc1-122">NOTES</span></span>

<span data-ttu-id="6fdc1-123">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6fdc1-123">ALIASES</span></span>

## <span data-ttu-id="6fdc1-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fdc1-124">RELATED LINKS</span></span>

