---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 7b60c157f3e86e72461c82f34a2d23dcb5eb0b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524350"
---
# <span data-ttu-id="c377d-101">Set-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c377d-101">Set-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="c377d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c377d-102">SYNOPSIS</span></span>
<span data-ttu-id="c377d-103">Ustawia znaczniki dla istniejącej PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c377d-103">Sets the Tags for an existing PublicIpPrefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c377d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c377d-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c377d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c377d-105">DESCRIPTION</span></span>
<span data-ttu-id="c377d-106">Polecenie cmdlet **Set-AzureRmPublicIpPrefix** ustawia znaczniki dla publicznego PREFIKSU adresu IP.</span><span class="sxs-lookup"><span data-stu-id="c377d-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="c377d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c377d-107">EXAMPLES</span></span>

### <span data-ttu-id="c377d-108">Ustawianie tagów publicznego prefiksu adresu IP</span><span class="sxs-lookup"><span data-stu-id="c377d-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzureRmPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="c377d-109">Pierwsze polecenie pobiera istniejący publiczny prefiks IP, drugie polecenie ustawia właściwość Tagi, a trzecie polecenie aktualizuje istniejący obiekt.</span><span class="sxs-lookup"><span data-stu-id="c377d-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="c377d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c377d-110">PARAMETERS</span></span>

### <span data-ttu-id="c377d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c377d-111">-AsJob</span></span>
<span data-ttu-id="c377d-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c377d-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c377d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c377d-113">-DefaultProfile</span></span>
<span data-ttu-id="c377d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c377d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c377d-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c377d-115">-PublicIpPrefix</span></span>
<span data-ttu-id="c377d-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c377d-116">The PublicIpPrefix</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c377d-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c377d-117">-Confirm</span></span>
<span data-ttu-id="c377d-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c377d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c377d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c377d-119">-WhatIf</span></span>
<span data-ttu-id="c377d-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c377d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c377d-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c377d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c377d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c377d-122">CommonParameters</span></span>
<span data-ttu-id="c377d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c377d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c377d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c377d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c377d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c377d-125">INPUTS</span></span>

### <span data-ttu-id="c377d-126">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c377d-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="c377d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c377d-127">OUTPUTS</span></span>

### <span data-ttu-id="c377d-128">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c377d-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="c377d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c377d-129">NOTES</span></span>

## <span data-ttu-id="c377d-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c377d-130">RELATED LINKS</span></span>
