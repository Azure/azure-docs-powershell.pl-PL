---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 14bda211d79e871d71bdef320df552b592fb1b89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541576"
---
# <span data-ttu-id="c459c-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="c459c-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="c459c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c459c-102">SYNOPSIS</span></span>
<span data-ttu-id="c459c-103">Usuwanie wszystkich poświadczeń Azure, kont i informacji o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c459c-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c459c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c459c-104">SYNTAX</span></span>

```
Clear-AzureRmContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c459c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c459c-105">DESCRIPTION</span></span>
<span data-ttu-id="c459c-106">Usuwanie wszystkich poświadczeń Azure, kont i informacji o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c459c-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="c459c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c459c-107">EXAMPLES</span></span>

### <span data-ttu-id="c459c-108">Wyczyść kontekst globalny</span><span class="sxs-lookup"><span data-stu-id="c459c-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="c459c-109">Usuń wszystkie informacje dotyczące konta, abonamentu i poświadczeń dla dowolnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c459c-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="c459c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c459c-110">PARAMETERS</span></span>

### <span data-ttu-id="c459c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c459c-111">-DefaultProfile</span></span>
<span data-ttu-id="c459c-112">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c459c-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c459c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c459c-113">-Force</span></span>
<span data-ttu-id="c459c-114">Usuwanie wszystkich użytkowników i grup z zakresu globalnego bez monitowania</span><span class="sxs-lookup"><span data-stu-id="c459c-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="c459c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c459c-115">-PassThru</span></span>
<span data-ttu-id="c459c-116">Zwracanie wartości oznaczającej sukces lub niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="c459c-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="c459c-117">-Zakres</span><span class="sxs-lookup"><span data-stu-id="c459c-117">-Scope</span></span>
<span data-ttu-id="c459c-118">Wyczyść kontekst tylko dla bieżącej sesji programu PowerShell lub dla wszystkich sesji.</span><span class="sxs-lookup"><span data-stu-id="c459c-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="c459c-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c459c-119">-Confirm</span></span>
<span data-ttu-id="c459c-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c459c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c459c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c459c-121">-WhatIf</span></span>
<span data-ttu-id="c459c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c459c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c459c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c459c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c459c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c459c-124">CommonParameters</span></span>
<span data-ttu-id="c459c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c459c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c459c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c459c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c459c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c459c-127">INPUTS</span></span>

### <span data-ttu-id="c459c-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c459c-128">None</span></span>

## <span data-ttu-id="c459c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c459c-129">OUTPUTS</span></span>

### <span data-ttu-id="c459c-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c459c-130">System.Boolean</span></span>

## <span data-ttu-id="c459c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c459c-131">NOTES</span></span>

## <span data-ttu-id="c459c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c459c-132">RELATED LINKS</span></span>
