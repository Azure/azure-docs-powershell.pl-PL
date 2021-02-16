---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202865"
---
# <span data-ttu-id="910c4-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="910c4-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="910c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="910c4-102">SYNOPSIS</span></span>
<span data-ttu-id="910c4-103">Tworzy konfigurację nagłówka reguły ponownego w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="910c4-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="910c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="910c4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="910c4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="910c4-105">DESCRIPTION</span></span>
<span data-ttu-id="910c4-106">**Polecenie cmdlet AzApplicationGatewayRewriteRuleHeaderConfiguration** tworzy zestaw akcji reguły ponownego w przypadku bramy aplikacji azure.</span><span class="sxs-lookup"><span data-stu-id="910c4-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="910c4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="910c4-107">EXAMPLES</span></span>

### <span data-ttu-id="910c4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="910c4-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="910c4-109">To polecenie tworzy konfigurację nagłówka reguły ponownego tworzenia i zapisuje wynik w zmiennej o nazwie $hc.</span><span class="sxs-lookup"><span data-stu-id="910c4-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="910c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="910c4-110">PARAMETERS</span></span>

### <span data-ttu-id="910c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910c4-111">-DefaultProfile</span></span>
<span data-ttu-id="910c4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="910c4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="910c4-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="910c4-113">-HeaderName</span></span>
<span data-ttu-id="910c4-114">Nazwa nagłówka do ponownego nac.</span><span class="sxs-lookup"><span data-stu-id="910c4-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="910c4-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="910c4-115">-HeaderValue</span></span>
<span data-ttu-id="910c4-116">Wartość nagłówka ustawiona dla danej nazwy nagłówka.</span><span class="sxs-lookup"><span data-stu-id="910c4-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="910c4-117">Nagłówek zostanie usunięty, jeśli zostanie pominięty</span><span class="sxs-lookup"><span data-stu-id="910c4-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="910c4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910c4-118">CommonParameters</span></span>
<span data-ttu-id="910c4-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="910c4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910c4-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="910c4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910c4-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="910c4-121">INPUTS</span></span>

### <span data-ttu-id="910c4-122">Brak</span><span class="sxs-lookup"><span data-stu-id="910c4-122">None</span></span>

## <span data-ttu-id="910c4-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="910c4-123">OUTPUTS</span></span>

### <span data-ttu-id="910c4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="910c4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="910c4-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="910c4-125">NOTES</span></span>

## <span data-ttu-id="910c4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="910c4-126">RELATED LINKS</span></span>

[<span data-ttu-id="910c4-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="910c4-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="910c4-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="910c4-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="910c4-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="910c4-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="910c4-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="910c4-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="910c4-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="910c4-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="910c4-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="910c4-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="910c4-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="910c4-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
