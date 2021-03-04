---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: 6d5bbd0cd0b5581e129e63e7559c09751d8f91cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956794"
---
# <span data-ttu-id="3608f-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3608f-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="3608f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3608f-102">SYNOPSIS</span></span>
<span data-ttu-id="3608f-103">Tworzy konfigurację nagłówka reguły ponownego w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3608f-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="3608f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3608f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3608f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3608f-105">DESCRIPTION</span></span>
<span data-ttu-id="3608f-106">**Polecenie cmdlet AzApplicationGatewayRewriteRuleHeaderConfiguration** tworzy zestaw akcji reguły ponownego tworzenia dla bramy aplikacji azure.</span><span class="sxs-lookup"><span data-stu-id="3608f-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="3608f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3608f-107">EXAMPLES</span></span>

### <span data-ttu-id="3608f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3608f-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="3608f-109">To polecenie tworzy konfigurację nagłówka reguły ponownego tworzenia i zapisuje wynik w zmiennej o nazwie $hc.</span><span class="sxs-lookup"><span data-stu-id="3608f-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="3608f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3608f-110">PARAMETERS</span></span>

### <span data-ttu-id="3608f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3608f-111">-DefaultProfile</span></span>
<span data-ttu-id="3608f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3608f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3608f-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="3608f-113">-HeaderName</span></span>
<span data-ttu-id="3608f-114">Nazwa nagłówka do ponownego nac.</span><span class="sxs-lookup"><span data-stu-id="3608f-114">Name of the Header to rewrite</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3608f-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="3608f-115">-HeaderValue</span></span>
<span data-ttu-id="3608f-116">Wartość nagłówka ustawiona dla danej nazwy nagłówka.</span><span class="sxs-lookup"><span data-stu-id="3608f-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="3608f-117">Nagłówek zostanie usunięty, jeśli zostanie pominięty</span><span class="sxs-lookup"><span data-stu-id="3608f-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="3608f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3608f-118">CommonParameters</span></span>
<span data-ttu-id="3608f-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3608f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3608f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3608f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3608f-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3608f-121">INPUTS</span></span>

### <span data-ttu-id="3608f-122">Brak</span><span class="sxs-lookup"><span data-stu-id="3608f-122">None</span></span>

## <span data-ttu-id="3608f-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3608f-123">OUTPUTS</span></span>

### <span data-ttu-id="3608f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3608f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="3608f-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3608f-125">NOTES</span></span>

## <span data-ttu-id="3608f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3608f-126">RELATED LINKS</span></span>

[<span data-ttu-id="3608f-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3608f-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3608f-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3608f-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3608f-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3608f-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3608f-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3608f-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3608f-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3608f-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3608f-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3608f-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="3608f-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3608f-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
