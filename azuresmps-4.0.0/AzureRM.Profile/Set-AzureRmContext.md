---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523554"
---
# <span data-ttu-id="b41be-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="b41be-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="b41be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b41be-102">SYNOPSIS</span></span>
<span data-ttu-id="b41be-103">Ustawia dzierżawę, abonament i środowisko dla poleceń cmdlet, które mają być używane w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="b41be-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="b41be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b41be-104">SYNTAX</span></span>

### <span data-ttu-id="b41be-105">Abonamentname (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b41be-105">SubscriptionName (Default)</span></span>
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b41be-106">Świetle</span><span class="sxs-lookup"><span data-stu-id="b41be-106">Context</span></span>
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b41be-107">Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b41be-107">SubscriptionId</span></span>
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b41be-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b41be-108">DESCRIPTION</span></span>
<span data-ttu-id="b41be-109">Polecenie cmdlet Set-AzureRmContext ustawia informacje uwierzytelniające dotyczące apletów poleceń uruchomionych w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="b41be-109">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="b41be-110">Kontekst obejmuje informacje dotyczące dzierżawy, abonamentu i środowiska.</span><span class="sxs-lookup"><span data-stu-id="b41be-110">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="b41be-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b41be-111">EXAMPLES</span></span>

### <span data-ttu-id="b41be-112">Przykład 1. Ustawianie kontekstu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b41be-112">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="b41be-113">To polecenie umożliwia ustawienie kontekstu do korzystania z określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b41be-113">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="b41be-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b41be-114">PARAMETERS</span></span>

### <span data-ttu-id="b41be-115">-Context</span><span class="sxs-lookup"><span data-stu-id="b41be-115">-Context</span></span>
<span data-ttu-id="b41be-116">Określa kontekst bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="b41be-116">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b41be-117">-SubscriptionId</span></span>
<span data-ttu-id="b41be-118">Określa identyfikator subskrypcji dla kontekstu, który jest ustawiany przez to polecenie cmdlet dla bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="b41be-118">Specifies the subscription ID for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-119">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="b41be-119">-SubscriptionName</span></span>
<span data-ttu-id="b41be-120">Określa nazwę subskrypcji dla kontekstu, który jest ustawiany przez to polecenie cmdlet dla bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="b41be-120">Specifies the subscription name for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-121">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="b41be-121">-TenantId</span></span>
<span data-ttu-id="b41be-122">Określa identyfikator dzierżawy dla kontekstu, który jest ustawiany przez to polecenie cmdlet dla bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="b41be-122">Specifies the ID of the tenant for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b41be-123">-Confirm</span></span>
<span data-ttu-id="b41be-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b41be-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b41be-125">-WhatIf</span></span>
<span data-ttu-id="b41be-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b41be-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b41be-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b41be-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41be-128">CommonParameters</span></span>
<span data-ttu-id="b41be-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b41be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41be-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b41be-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41be-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b41be-131">INPUTS</span></span>

## <span data-ttu-id="b41be-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b41be-132">OUTPUTS</span></span>

### <span data-ttu-id="b41be-133">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="b41be-133">PSAzureContext</span></span>

## <span data-ttu-id="b41be-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b41be-134">NOTES</span></span>

## <span data-ttu-id="b41be-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b41be-135">RELATED LINKS</span></span>

[<span data-ttu-id="b41be-136">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="b41be-136">Get-AzureRMContext</span></span>]()

