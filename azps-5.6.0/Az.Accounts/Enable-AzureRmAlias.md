---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: e99d7643fe67d4102e9f4eef7f9c10f131594948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008177"
---
# <span data-ttu-id="28112-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="28112-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="28112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28112-102">SYNOPSIS</span></span>
<span data-ttu-id="28112-103">Włącza aliasy prefiksów usługi AzureRm dla modułów az.</span><span class="sxs-lookup"><span data-stu-id="28112-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="28112-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="28112-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28112-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="28112-105">DESCRIPTION</span></span>
<span data-ttu-id="28112-106">Włącza aliasy prefiksów usługi AzureRm dla modułów az.</span><span class="sxs-lookup"><span data-stu-id="28112-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="28112-107">Jeśli określono funkcję -Module, aliasy będą włączone tylko w modułach wymienionych na liście.</span><span class="sxs-lookup"><span data-stu-id="28112-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="28112-108">W przeciwnym razie są włączone wszystkie aliasy usługi AzureRm.</span><span class="sxs-lookup"><span data-stu-id="28112-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="28112-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="28112-109">EXAMPLES</span></span>

### <span data-ttu-id="28112-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28112-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="28112-111">Włącza wszystkie prefiksy usługi AzureRm dla bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28112-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="28112-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="28112-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="28112-113">Umożliwia korzystanie z aliasów usługi AzureRm dla modułu Az.Accounts zarówno dla bieżącego procesu, jak i dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="28112-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="28112-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28112-114">PARAMETERS</span></span>

### <span data-ttu-id="28112-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28112-115">-DefaultProfile</span></span>
<span data-ttu-id="28112-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="28112-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28112-117">— Moduł</span><span class="sxs-lookup"><span data-stu-id="28112-117">-Module</span></span>
<span data-ttu-id="28112-118">Wskazuje moduły, dla których mają być włączane aliasy.</span><span class="sxs-lookup"><span data-stu-id="28112-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="28112-119">Jeśli nie zostaną określone żadne moduły, wartością domyślną są wszystkie moduły.</span><span class="sxs-lookup"><span data-stu-id="28112-119">If none are specified, default is all modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28112-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28112-120">-PassThru</span></span>
<span data-ttu-id="28112-121">Jeśli zostanie określona, polecenie cmdlet zwróci wszystkie włączone aliasy</span><span class="sxs-lookup"><span data-stu-id="28112-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="28112-122">— Zakres</span><span class="sxs-lookup"><span data-stu-id="28112-122">-Scope</span></span>
<span data-ttu-id="28112-123">Wskazuje, dla których aliasów zakresów należy włączyć obsługę.</span><span class="sxs-lookup"><span data-stu-id="28112-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="28112-124">Wartość domyślna to "Lokalna"</span><span class="sxs-lookup"><span data-stu-id="28112-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28112-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28112-125">-Confirm</span></span>
<span data-ttu-id="28112-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="28112-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28112-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28112-127">-WhatIf</span></span>
<span data-ttu-id="28112-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28112-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28112-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="28112-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28112-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28112-130">CommonParameters</span></span>
<span data-ttu-id="28112-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28112-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28112-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28112-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28112-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28112-133">INPUTS</span></span>

### <span data-ttu-id="28112-134">Brak</span><span class="sxs-lookup"><span data-stu-id="28112-134">None</span></span>

## <span data-ttu-id="28112-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28112-135">OUTPUTS</span></span>

### <span data-ttu-id="28112-136">System.String</span><span class="sxs-lookup"><span data-stu-id="28112-136">System.String</span></span>

## <span data-ttu-id="28112-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="28112-137">NOTES</span></span>

## <span data-ttu-id="28112-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28112-138">RELATED LINKS</span></span>
