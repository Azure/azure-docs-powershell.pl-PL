---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 56352ff165d2e7dcbf5386e713028fae5c991d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552879"
---
# <span data-ttu-id="fdb25-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="fdb25-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="fdb25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fdb25-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb25-103">Tworzy znacznik IP.</span><span class="sxs-lookup"><span data-stu-id="fdb25-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fdb25-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fdb25-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fdb25-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb25-106">Polecenie cmdlet **New-AzureRmPublicIpTag** tworzy tag IP.</span><span class="sxs-lookup"><span data-stu-id="fdb25-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="fdb25-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fdb25-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb25-108">1: Tworzenie nowego tagu IP</span><span class="sxs-lookup"><span data-stu-id="fdb25-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="fdb25-109">To polecenie tworzy nowy tag IP z TagType "FirstPartyUsage" i znacznikiem like "/SQL".</span><span class="sxs-lookup"><span data-stu-id="fdb25-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="fdb25-110">Ta funkcja jest używana w publicIpAddress tworzenia przy użyciu tych specjalnych znaczników do przydzielenia.</span><span class="sxs-lookup"><span data-stu-id="fdb25-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="fdb25-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fdb25-111">PARAMETERS</span></span>

### <span data-ttu-id="fdb25-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb25-112">-DefaultProfile</span></span>
<span data-ttu-id="fdb25-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb25-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdb25-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="fdb25-114">-IpTagType</span></span>
<span data-ttu-id="fdb25-115">Typ IpTag przykład: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="fdb25-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb25-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="fdb25-116">-Tag</span></span>
<span data-ttu-id="fdb25-117">IpTag wartość przykład:/SQL</span><span class="sxs-lookup"><span data-stu-id="fdb25-117">IpTag value Example:/Sql</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb25-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fdb25-118">-Confirm</span></span>
<span data-ttu-id="fdb25-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdb25-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb25-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb25-120">-WhatIf</span></span>
<span data-ttu-id="fdb25-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdb25-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb25-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fdb25-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="fdb25-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fdb25-123">INPUTS</span></span>

### <span data-ttu-id="fdb25-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fdb25-124">System.String</span></span>


## <span data-ttu-id="fdb25-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fdb25-125">OUTPUTS</span></span>

### <span data-ttu-id="fdb25-126">Microsoft. Azure. Commands. Network. models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="fdb25-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>


## <span data-ttu-id="fdb25-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fdb25-127">NOTES</span></span>

## <span data-ttu-id="fdb25-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fdb25-128">RELATED LINKS</span></span>

