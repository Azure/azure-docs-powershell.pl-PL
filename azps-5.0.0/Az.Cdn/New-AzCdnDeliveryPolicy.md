---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233991"
---
# <span data-ttu-id="a3bfd-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a3bfd-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="a3bfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="a3bfd-103">Tworzy zasady dostarczania.</span><span class="sxs-lookup"><span data-stu-id="a3bfd-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="a3bfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3bfd-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3bfd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3bfd-105">DESCRIPTION</span></span>
<span data-ttu-id="a3bfd-106">Polecenie cmdlet **New-AzCdnDeliveryPolicy** tworzy zasady dostarczania dla tworzenia punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="a3bfd-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="a3bfd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3bfd-107">EXAMPLES</span></span>

### <span data-ttu-id="a3bfd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3bfd-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="a3bfd-109">Tworzenie przykładowych zasad dostarczania</span><span class="sxs-lookup"><span data-stu-id="a3bfd-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="a3bfd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3bfd-110">PARAMETERS</span></span>

### <span data-ttu-id="a3bfd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3bfd-111">-DefaultProfile</span></span>
<span data-ttu-id="a3bfd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3bfd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3bfd-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="a3bfd-113">-Description</span></span>
<span data-ttu-id="a3bfd-114">Opis zasad</span><span class="sxs-lookup"><span data-stu-id="a3bfd-114">Description of the policy</span></span>

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

### <span data-ttu-id="a3bfd-115">— Reguła</span><span class="sxs-lookup"><span data-stu-id="a3bfd-115">-Rule</span></span>
<span data-ttu-id="a3bfd-116">Lista deliveryRules.</span><span class="sxs-lookup"><span data-stu-id="a3bfd-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3bfd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3bfd-117">CommonParameters</span></span>
<span data-ttu-id="a3bfd-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3bfd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3bfd-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3bfd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3bfd-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3bfd-120">INPUTS</span></span>

### <span data-ttu-id="a3bfd-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a3bfd-121">None</span></span>

## <span data-ttu-id="a3bfd-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3bfd-122">OUTPUTS</span></span>

### <span data-ttu-id="a3bfd-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a3bfd-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="a3bfd-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3bfd-124">NOTES</span></span>

## <span data-ttu-id="a3bfd-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3bfd-125">RELATED LINKS</span></span>
