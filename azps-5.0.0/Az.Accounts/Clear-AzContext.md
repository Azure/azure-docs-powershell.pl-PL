---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225269"
---
# <span data-ttu-id="84763-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="84763-101">Clear-AzContext</span></span>

## <span data-ttu-id="84763-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84763-102">SYNOPSIS</span></span>
<span data-ttu-id="84763-103">Usuwanie wszystkich poświadczeń Azure, kont i informacji o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="84763-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="84763-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84763-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84763-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84763-105">DESCRIPTION</span></span>
<span data-ttu-id="84763-106">Usuwanie wszystkich poświadczeń Azure, kont i informacji o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="84763-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="84763-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84763-107">EXAMPLES</span></span>

### <span data-ttu-id="84763-108">Przykład 1. Wyczyść kontekst globalny</span><span class="sxs-lookup"><span data-stu-id="84763-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="84763-109">Usuń wszystkie informacje dotyczące konta, abonamentu i poświadczeń dla dowolnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="84763-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="84763-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84763-110">PARAMETERS</span></span>

### <span data-ttu-id="84763-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84763-111">-DefaultProfile</span></span>
<span data-ttu-id="84763-112">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="84763-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84763-113">-Force</span><span class="sxs-lookup"><span data-stu-id="84763-113">-Force</span></span>
<span data-ttu-id="84763-114">Usuwanie wszystkich użytkowników i grup z zakresu globalnego bez monitowania</span><span class="sxs-lookup"><span data-stu-id="84763-114">Delete all users and groups from the global scope without prompting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84763-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84763-115">-PassThru</span></span>
<span data-ttu-id="84763-116">Zwracanie wartości oznaczającej sukces lub niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="84763-116">Return a value indicating success or failure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84763-117">-Zakres</span><span class="sxs-lookup"><span data-stu-id="84763-117">-Scope</span></span>
<span data-ttu-id="84763-118">Wyczyść kontekst tylko dla bieżącej sesji programu PowerShell lub dla wszystkich sesji.</span><span class="sxs-lookup"><span data-stu-id="84763-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="84763-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84763-119">-Confirm</span></span>
<span data-ttu-id="84763-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84763-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84763-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84763-121">-WhatIf</span></span>
<span data-ttu-id="84763-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84763-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84763-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84763-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84763-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84763-124">CommonParameters</span></span>
<span data-ttu-id="84763-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84763-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84763-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84763-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84763-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84763-127">INPUTS</span></span>

### <span data-ttu-id="84763-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="84763-128">None</span></span>

## <span data-ttu-id="84763-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84763-129">OUTPUTS</span></span>

### <span data-ttu-id="84763-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84763-130">System.Boolean</span></span>

## <span data-ttu-id="84763-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84763-131">NOTES</span></span>

## <span data-ttu-id="84763-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84763-132">RELATED LINKS</span></span>
