---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: f268c4171be78265843d5a04291bf430dc4f19b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890269"
---
# <span data-ttu-id="b9f02-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="b9f02-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="b9f02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9f02-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f02-103">Wyłącz Autozapisywanie poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9f02-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="b9f02-104">Informacje logowania zostaną zapomniane podczas następnego otwarcia okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9f02-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="b9f02-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9f02-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9f02-106">Opis</span><span class="sxs-lookup"><span data-stu-id="b9f02-106">DESCRIPTION</span></span>
<span data-ttu-id="b9f02-107">Wyłącz Autozapisywanie poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9f02-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="b9f02-108">Informacje logowania zostaną zapomniane podczas następnego otwarcia okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9f02-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="b9f02-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9f02-109">EXAMPLES</span></span>

### <span data-ttu-id="b9f02-110">Wyłączanie autozapisywania kontekstu</span><span class="sxs-lookup"><span data-stu-id="b9f02-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="b9f02-111">Wyłącz Autozapis dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b9f02-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="b9f02-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9f02-112">PARAMETERS</span></span>

### <span data-ttu-id="b9f02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f02-113">-DefaultProfile</span></span>
<span data-ttu-id="b9f02-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b9f02-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9f02-115">-Zakres</span><span class="sxs-lookup"><span data-stu-id="b9f02-115">-Scope</span></span>
<span data-ttu-id="b9f02-116">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b9f02-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="b9f02-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9f02-117">-Confirm</span></span>
<span data-ttu-id="b9f02-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9f02-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9f02-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9f02-119">-WhatIf</span></span>
<span data-ttu-id="b9f02-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9f02-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9f02-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9f02-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9f02-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f02-122">CommonParameters</span></span>
<span data-ttu-id="b9f02-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9f02-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f02-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9f02-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f02-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9f02-125">INPUTS</span></span>

### <span data-ttu-id="b9f02-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b9f02-126">None</span></span>

## <span data-ttu-id="b9f02-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9f02-127">OUTPUTS</span></span>

### <span data-ttu-id="b9f02-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="b9f02-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="b9f02-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9f02-129">NOTES</span></span>

## <span data-ttu-id="b9f02-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9f02-130">RELATED LINKS</span></span>
