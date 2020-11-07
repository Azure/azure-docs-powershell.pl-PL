---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: 76271fc9b6ef8546f8f02b64ac32cc65cf4abb3f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890266"
---
# <span data-ttu-id="c5e64-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="c5e64-101">Clear-AzDefault</span></span>

## <span data-ttu-id="c5e64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5e64-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e64-103">Czyści ustawienia domyślne ustawione przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="c5e64-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="c5e64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5e64-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5e64-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c5e64-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e64-106">Polecenie cmdlet Clear-AzDefault usuwa ustawienia domyślne ustawiane przez użytkownika w zależności od parametrów przełącznika określonych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c5e64-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="c5e64-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5e64-107">EXAMPLES</span></span>

### <span data-ttu-id="c5e64-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5e64-108">Example 1</span></span>
```
PS C:\> Clear-AzDefault
```

<span data-ttu-id="c5e64-109">To polecenie usuwa wszystkie ustawienia domyślne ustawione przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="c5e64-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="c5e64-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5e64-110">Example 1</span></span>
```
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="c5e64-111">To polecenie usuwa domyślną grupę zasobów ustawioną przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="c5e64-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="c5e64-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5e64-112">PARAMETERS</span></span>

### <span data-ttu-id="c5e64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e64-113">-DefaultProfile</span></span>
<span data-ttu-id="c5e64-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5e64-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5e64-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c5e64-115">-Force</span></span>
<span data-ttu-id="c5e64-116">Usuwanie wszystkich ustawień domyślnych, jeśli nie określono wartości domyślnej</span><span class="sxs-lookup"><span data-stu-id="c5e64-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="c5e64-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5e64-117">-PassThru</span></span>
<span data-ttu-id="c5e64-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c5e64-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c5e64-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c5e64-119">-ResourceGroup</span></span>
<span data-ttu-id="c5e64-120">Wyczyść domyślną grupę zasobów</span><span class="sxs-lookup"><span data-stu-id="c5e64-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e64-121">-Zakres</span><span class="sxs-lookup"><span data-stu-id="c5e64-121">-Scope</span></span>
<span data-ttu-id="c5e64-122">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c5e64-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c5e64-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c5e64-123">-Confirm</span></span>
<span data-ttu-id="c5e64-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e64-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5e64-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e64-125">-WhatIf</span></span>
<span data-ttu-id="c5e64-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e64-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e64-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c5e64-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5e64-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e64-128">CommonParameters</span></span>
<span data-ttu-id="c5e64-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e64-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e64-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5e64-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e64-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5e64-131">INPUTS</span></span>

### <span data-ttu-id="c5e64-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c5e64-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c5e64-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5e64-133">OUTPUTS</span></span>

### <span data-ttu-id="c5e64-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5e64-134">System.Boolean</span></span>

## <span data-ttu-id="c5e64-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5e64-135">NOTES</span></span>

## <span data-ttu-id="c5e64-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5e64-136">RELATED LINKS</span></span>
