---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 1f9f17e03a9b3cf79b2764c7711da9eee6ca104d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999076"
---
# <span data-ttu-id="69825-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="69825-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="69825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69825-102">SYNOPSIS</span></span>
<span data-ttu-id="69825-103">Wyłącza aliasy prefiksów usługi AzureRm dla modułów az.</span><span class="sxs-lookup"><span data-stu-id="69825-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="69825-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69825-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69825-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="69825-105">DESCRIPTION</span></span>
<span data-ttu-id="69825-106">Wyłącza aliasy prefiksów usługi AzureRm dla modułów az.</span><span class="sxs-lookup"><span data-stu-id="69825-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="69825-107">Jeśli określono wartość -Module, aliasy będą wyłączone tylko w modułach wymienionych na liście.</span><span class="sxs-lookup"><span data-stu-id="69825-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="69825-108">W przeciwnym razie wszystkie aliasy usługi AzureRm są wyłączone.</span><span class="sxs-lookup"><span data-stu-id="69825-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="69825-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69825-109">EXAMPLES</span></span>

### <span data-ttu-id="69825-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69825-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="69825-111">Wyłącza wszystkie prefiksy usługi AzureRm dla bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="69825-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="69825-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69825-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="69825-113">Wyłącza aliasy usługi AzureRm dla modułu Az.Accounts zarówno dla bieżącego procesu, jak i dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="69825-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="69825-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69825-114">PARAMETERS</span></span>

### <span data-ttu-id="69825-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69825-115">-DefaultProfile</span></span>
<span data-ttu-id="69825-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69825-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69825-117">— Moduł</span><span class="sxs-lookup"><span data-stu-id="69825-117">-Module</span></span>
<span data-ttu-id="69825-118">Wskazuje moduły, dla których mają być wyłączane aliasy.</span><span class="sxs-lookup"><span data-stu-id="69825-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="69825-119">Jeśli żadne z nich nie zostanie określone, domyślnie wszystkie włączone moduły.</span><span class="sxs-lookup"><span data-stu-id="69825-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="69825-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69825-120">-PassThru</span></span>
<span data-ttu-id="69825-121">Jeśli zostanie określona, polecenie cmdlet zwróci wszystkie wyłączone aliasy</span><span class="sxs-lookup"><span data-stu-id="69825-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="69825-122">— Zakres</span><span class="sxs-lookup"><span data-stu-id="69825-122">-Scope</span></span>
<span data-ttu-id="69825-123">Wskazuje, dla których aliasów zakresu należy wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="69825-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="69825-124">Wartość domyślna to "Proces"</span><span class="sxs-lookup"><span data-stu-id="69825-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69825-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69825-125">-Confirm</span></span>
<span data-ttu-id="69825-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69825-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69825-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69825-127">-WhatIf</span></span>
<span data-ttu-id="69825-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69825-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69825-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="69825-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69825-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69825-130">CommonParameters</span></span>
<span data-ttu-id="69825-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69825-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69825-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69825-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69825-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69825-133">INPUTS</span></span>

### <span data-ttu-id="69825-134">Brak</span><span class="sxs-lookup"><span data-stu-id="69825-134">None</span></span>

## <span data-ttu-id="69825-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69825-135">OUTPUTS</span></span>

### <span data-ttu-id="69825-136">System.String</span><span class="sxs-lookup"><span data-stu-id="69825-136">System.String</span></span>

## <span data-ttu-id="69825-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69825-137">NOTES</span></span>

## <span data-ttu-id="69825-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69825-138">RELATED LINKS</span></span>
