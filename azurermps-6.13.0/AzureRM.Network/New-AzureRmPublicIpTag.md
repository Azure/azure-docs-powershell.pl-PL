---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 6d46be31d443bdfeeda850cd03ce2a050e25549f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554048"
---
# <span data-ttu-id="184ac-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="184ac-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="184ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="184ac-102">SYNOPSIS</span></span>
<span data-ttu-id="184ac-103">Tworzy znacznik IP.</span><span class="sxs-lookup"><span data-stu-id="184ac-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="184ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="184ac-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="184ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="184ac-105">DESCRIPTION</span></span>
<span data-ttu-id="184ac-106">Polecenie cmdlet **New-AzureRmPublicIpTag** tworzy tag IP.</span><span class="sxs-lookup"><span data-stu-id="184ac-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="184ac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="184ac-107">EXAMPLES</span></span>

### <span data-ttu-id="184ac-108">1: Tworzenie nowego tagu IP</span><span class="sxs-lookup"><span data-stu-id="184ac-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="184ac-109">To polecenie tworzy nowy tag IP z TagType "FirstPartyUsage" i znacznikiem like "/SQL".</span><span class="sxs-lookup"><span data-stu-id="184ac-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="184ac-110">Ta funkcja jest używana w publicIpAddress tworzenia przy użyciu tych specjalnych znaczników do przydzielenia.</span><span class="sxs-lookup"><span data-stu-id="184ac-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="184ac-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="184ac-111">PARAMETERS</span></span>

### <span data-ttu-id="184ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184ac-112">-DefaultProfile</span></span>
<span data-ttu-id="184ac-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="184ac-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="184ac-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="184ac-114">-IpTagType</span></span>
<span data-ttu-id="184ac-115">Typ IpTag przykład: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="184ac-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184ac-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="184ac-116">-Tag</span></span>
<span data-ttu-id="184ac-117">IpTag wartość przykład:/SQL</span><span class="sxs-lookup"><span data-stu-id="184ac-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184ac-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="184ac-118">-Confirm</span></span>
<span data-ttu-id="184ac-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="184ac-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184ac-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="184ac-120">-WhatIf</span></span>
<span data-ttu-id="184ac-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="184ac-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="184ac-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="184ac-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184ac-123">CommonParameters</span></span>
<span data-ttu-id="184ac-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="184ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184ac-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="184ac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184ac-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="184ac-126">INPUTS</span></span>

### <span data-ttu-id="184ac-127">System. String</span><span class="sxs-lookup"><span data-stu-id="184ac-127">System.String</span></span>

## <span data-ttu-id="184ac-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="184ac-128">OUTPUTS</span></span>

### <span data-ttu-id="184ac-129">Microsoft. Azure. Commands. Network. models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="184ac-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="184ac-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="184ac-130">NOTES</span></span>

## <span data-ttu-id="184ac-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="184ac-131">RELATED LINKS</span></span>
