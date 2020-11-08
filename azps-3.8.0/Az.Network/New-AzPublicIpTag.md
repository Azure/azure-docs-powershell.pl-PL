---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 1cf1d8cf40117afdb250332df466d7a787420e14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052068"
---
# <span data-ttu-id="6124d-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="6124d-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="6124d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6124d-102">SYNOPSIS</span></span>
<span data-ttu-id="6124d-103">Tworzy znacznik IP.</span><span class="sxs-lookup"><span data-stu-id="6124d-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="6124d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6124d-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6124d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6124d-105">DESCRIPTION</span></span>
<span data-ttu-id="6124d-106">Polecenie cmdlet **New-AzPublicIpTag** tworzy tag IP.</span><span class="sxs-lookup"><span data-stu-id="6124d-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="6124d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6124d-107">EXAMPLES</span></span>

### <span data-ttu-id="6124d-108">1: Tworzenie nowego tagu IP</span><span class="sxs-lookup"><span data-stu-id="6124d-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="6124d-109">To polecenie tworzy nowy tag IP z TagType "FirstPartyUsage" i znacznikiem like "/SQL".</span><span class="sxs-lookup"><span data-stu-id="6124d-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="6124d-110">Ta funkcja jest używana w publicIpAddress tworzenia przy użyciu tych specjalnych znaczników do przydzielenia.</span><span class="sxs-lookup"><span data-stu-id="6124d-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="6124d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6124d-111">PARAMETERS</span></span>

### <span data-ttu-id="6124d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6124d-112">-DefaultProfile</span></span>
<span data-ttu-id="6124d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6124d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6124d-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="6124d-114">-IpTagType</span></span>
<span data-ttu-id="6124d-115">Typ IpTag przykład: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="6124d-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="6124d-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="6124d-116">-Tag</span></span>
<span data-ttu-id="6124d-117">IpTag wartość przykład:/SQL</span><span class="sxs-lookup"><span data-stu-id="6124d-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="6124d-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6124d-118">-Confirm</span></span>
<span data-ttu-id="6124d-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6124d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6124d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6124d-120">-WhatIf</span></span>
<span data-ttu-id="6124d-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6124d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6124d-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6124d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6124d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6124d-123">CommonParameters</span></span>
<span data-ttu-id="6124d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6124d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6124d-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6124d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6124d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6124d-126">INPUTS</span></span>

### <span data-ttu-id="6124d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6124d-127">System.String</span></span>

## <span data-ttu-id="6124d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6124d-128">OUTPUTS</span></span>

### <span data-ttu-id="6124d-129">Microsoft. Azure. Commands. Network. models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="6124d-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="6124d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6124d-130">NOTES</span></span>

## <span data-ttu-id="6124d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6124d-131">RELATED LINKS</span></span>
