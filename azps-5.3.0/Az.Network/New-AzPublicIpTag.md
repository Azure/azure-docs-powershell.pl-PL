---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 5d7d73b3c7f49babc9e80929dab7b3fa2adad20a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490977"
---
# <span data-ttu-id="ab8a4-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="ab8a4-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="ab8a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab8a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8a4-103">Tworzy znacznik IP.</span><span class="sxs-lookup"><span data-stu-id="ab8a4-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="ab8a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab8a4-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab8a4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab8a4-105">DESCRIPTION</span></span>
<span data-ttu-id="ab8a4-106">Polecenie cmdlet **New-AzPublicIpTag** tworzy tag IP.</span><span class="sxs-lookup"><span data-stu-id="ab8a4-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="ab8a4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab8a4-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8a4-108">Przykład 1. Tworzenie nowego tagu IP</span><span class="sxs-lookup"><span data-stu-id="ab8a4-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="ab8a4-109">To polecenie tworzy nowy tag IP z TagType "FirstPartyUsage" i znacznikiem like "/SQL".</span><span class="sxs-lookup"><span data-stu-id="ab8a4-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="ab8a4-110">Ta funkcja jest używana w publicIpAddress tworzenia przy użyciu tych specjalnych znaczników do przydzielenia.</span><span class="sxs-lookup"><span data-stu-id="ab8a4-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="ab8a4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab8a4-111">PARAMETERS</span></span>

### <span data-ttu-id="ab8a4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8a4-112">-DefaultProfile</span></span>
<span data-ttu-id="ab8a4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab8a4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab8a4-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="ab8a4-114">-IpTagType</span></span>
<span data-ttu-id="ab8a4-115">Typ IpTag przykład: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="ab8a4-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="ab8a4-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab8a4-116">-Tag</span></span>
<span data-ttu-id="ab8a4-117">IpTag wartość przykład:/SQL</span><span class="sxs-lookup"><span data-stu-id="ab8a4-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="ab8a4-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab8a4-118">-Confirm</span></span>
<span data-ttu-id="ab8a4-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab8a4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab8a4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab8a4-120">-WhatIf</span></span>
<span data-ttu-id="ab8a4-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab8a4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab8a4-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab8a4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab8a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8a4-123">CommonParameters</span></span>
<span data-ttu-id="ab8a4-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8a4-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab8a4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8a4-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab8a4-126">INPUTS</span></span>

### <span data-ttu-id="ab8a4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ab8a4-127">System.String</span></span>

## <span data-ttu-id="ab8a4-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab8a4-128">OUTPUTS</span></span>

### <span data-ttu-id="ab8a4-129">Microsoft. Azure. Commands. Network. models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="ab8a4-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="ab8a4-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab8a4-130">NOTES</span></span>

## <span data-ttu-id="ab8a4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab8a4-131">RELATED LINKS</span></span>
