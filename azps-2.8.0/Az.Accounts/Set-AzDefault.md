---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 6cf3c98c721b5a4f72ef63cfa5f9be991bf517ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707190"
---
# <span data-ttu-id="a6700-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="a6700-101">Set-AzDefault</span></span>

## <span data-ttu-id="a6700-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6700-102">SYNOPSIS</span></span>
<span data-ttu-id="a6700-103">Ustawia wartość domyślną w bieżącym kontekście</span><span class="sxs-lookup"><span data-stu-id="a6700-103">Sets a default in the current context</span></span>

## <span data-ttu-id="a6700-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6700-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6700-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a6700-105">DESCRIPTION</span></span>
<span data-ttu-id="a6700-106">Polecenie cmdlet Set-AzDefault powoduje dodanie lub zmianę wartości domyślnych w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="a6700-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="a6700-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6700-107">EXAMPLES</span></span>

### <span data-ttu-id="a6700-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6700-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="a6700-109">To polecenie ustawia domyślną grupę zasobów dla grupy zasobów określonej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a6700-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="a6700-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6700-110">PARAMETERS</span></span>

### <span data-ttu-id="a6700-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6700-111">-DefaultProfile</span></span>
<span data-ttu-id="a6700-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6700-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6700-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a6700-113">-Force</span></span>
<span data-ttu-id="a6700-114">Tworzenie nowej grupy zasobów, jeśli określona wartość domyślna nie istnieje</span><span class="sxs-lookup"><span data-stu-id="a6700-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="a6700-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6700-115">-ResourceGroupName</span></span>
<span data-ttu-id="a6700-116">Nazwa grupy zasobów ustawiana jako domyślna</span><span class="sxs-lookup"><span data-stu-id="a6700-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6700-117">-Zakres</span><span class="sxs-lookup"><span data-stu-id="a6700-117">-Scope</span></span>
<span data-ttu-id="a6700-118">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a6700-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a6700-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6700-119">-Confirm</span></span>
<span data-ttu-id="a6700-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6700-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6700-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6700-121">-WhatIf</span></span>
<span data-ttu-id="a6700-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6700-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6700-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a6700-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6700-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6700-124">CommonParameters</span></span>
<span data-ttu-id="a6700-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6700-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6700-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6700-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6700-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6700-127">INPUTS</span></span>

### <span data-ttu-id="a6700-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a6700-128">System.String</span></span>

## <span data-ttu-id="a6700-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6700-129">OUTPUTS</span></span>

### <span data-ttu-id="a6700-130">Microsoft. Azure. Commands. profile. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a6700-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="a6700-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6700-131">NOTES</span></span>

## <span data-ttu-id="a6700-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6700-132">RELATED LINKS</span></span>
