---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: e0aec59bf78d9876f6b2ef061204bdb833624791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704747"
---
# <span data-ttu-id="114b7-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="114b7-101">Select-AzContext</span></span>

## <span data-ttu-id="114b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="114b7-102">SYNOPSIS</span></span>
<span data-ttu-id="114b7-103">Wybierz abonament i konto docelowe dla poleceń cmdlet środowiska Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="114b7-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="114b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="114b7-104">SYNTAX</span></span>

### <span data-ttu-id="114b7-105">SelectByInputObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="114b7-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="114b7-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="114b7-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="114b7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="114b7-107">DESCRIPTION</span></span>
<span data-ttu-id="114b7-108">Wybierz abonament dla lokalizacji docelowej (lub konta lub dzierżawy) w poleceniach cmdlet środowiska Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="114b7-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="114b7-109">Po tym poleceniu cmdlet przyszłe polecenia cmdlet będą wskazywać wybrany kontekst.</span><span class="sxs-lookup"><span data-stu-id="114b7-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="114b7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="114b7-110">EXAMPLES</span></span>

### <span data-ttu-id="114b7-111">Przykład 1. cel nazwanego kontekstu</span><span class="sxs-lookup"><span data-stu-id="114b7-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="114b7-112">Docelowe przyszłe polecenia cmdlet programu PowerShell środowiska Azure na koncie, dzierżawie i subskrypcji w kontekście "praca".</span><span class="sxs-lookup"><span data-stu-id="114b7-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="114b7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="114b7-113">PARAMETERS</span></span>

### <span data-ttu-id="114b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114b7-114">-DefaultProfile</span></span>
<span data-ttu-id="114b7-115">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="114b7-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="114b7-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="114b7-116">-InputObject</span></span>
<span data-ttu-id="114b7-117">Obiekt kontekstu, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="114b7-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="114b7-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="114b7-118">-Name</span></span>
<span data-ttu-id="114b7-119">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="114b7-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114b7-120">-Zakres</span><span class="sxs-lookup"><span data-stu-id="114b7-120">-Scope</span></span>
<span data-ttu-id="114b7-121">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="114b7-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="114b7-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="114b7-122">-Confirm</span></span>
<span data-ttu-id="114b7-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="114b7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="114b7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="114b7-124">-WhatIf</span></span>
<span data-ttu-id="114b7-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="114b7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="114b7-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="114b7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="114b7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114b7-127">CommonParameters</span></span>
<span data-ttu-id="114b7-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="114b7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114b7-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="114b7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114b7-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="114b7-130">INPUTS</span></span>

### <span data-ttu-id="114b7-131">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="114b7-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="114b7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="114b7-132">OUTPUTS</span></span>

### <span data-ttu-id="114b7-133">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="114b7-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="114b7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="114b7-134">NOTES</span></span>

## <span data-ttu-id="114b7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="114b7-135">RELATED LINKS</span></span>
