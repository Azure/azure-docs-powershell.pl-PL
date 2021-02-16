---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 6a530a0e20f3e69540320ad3eab8b8cc7f37b5af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195434"
---
# <span data-ttu-id="9963b-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="9963b-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="9963b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9963b-102">SYNOPSIS</span></span>
<span data-ttu-id="9963b-103">Włącza aliasy prefiksów usługi AzureRm dla modułów az.</span><span class="sxs-lookup"><span data-stu-id="9963b-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="9963b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9963b-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9963b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9963b-105">DESCRIPTION</span></span>
<span data-ttu-id="9963b-106">Włącza aliasy prefiksów usługi AzureRm dla modułów az.</span><span class="sxs-lookup"><span data-stu-id="9963b-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="9963b-107">Jeśli określono funkcję -Module, aliasy będą włączone tylko w modułach wymienionych na liście.</span><span class="sxs-lookup"><span data-stu-id="9963b-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="9963b-108">W przeciwnym razie są włączone wszystkie aliasy usługi AzureRm.</span><span class="sxs-lookup"><span data-stu-id="9963b-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="9963b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9963b-109">EXAMPLES</span></span>

### <span data-ttu-id="9963b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9963b-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="9963b-111">Włącza wszystkie prefiksy usługi AzureRm dla bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9963b-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="9963b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9963b-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="9963b-113">Umożliwia korzystanie z aliasów usługi AzureRm dla modułu Az.Accounts zarówno dla bieżącego procesu, jak i dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9963b-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="9963b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9963b-114">PARAMETERS</span></span>

### <span data-ttu-id="9963b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9963b-115">-DefaultProfile</span></span>
<span data-ttu-id="9963b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9963b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9963b-117">— Moduł</span><span class="sxs-lookup"><span data-stu-id="9963b-117">-Module</span></span>
<span data-ttu-id="9963b-118">Wskazuje moduły, dla których mają być włączane aliasy.</span><span class="sxs-lookup"><span data-stu-id="9963b-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="9963b-119">Jeśli nie zostanie określone, wartością domyślną są wszystkie moduły.</span><span class="sxs-lookup"><span data-stu-id="9963b-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="9963b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9963b-120">-PassThru</span></span>
<span data-ttu-id="9963b-121">Jeśli zostanie określona, polecenie cmdlet zwróci wszystkie włączone aliasy</span><span class="sxs-lookup"><span data-stu-id="9963b-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="9963b-122">— Zakres</span><span class="sxs-lookup"><span data-stu-id="9963b-122">-Scope</span></span>
<span data-ttu-id="9963b-123">Wskazuje, dla jakich aliasów zakresów należy włączyć obsługę.</span><span class="sxs-lookup"><span data-stu-id="9963b-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="9963b-124">Wartość domyślna to "Lokalne"</span><span class="sxs-lookup"><span data-stu-id="9963b-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="9963b-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9963b-125">-Confirm</span></span>
<span data-ttu-id="9963b-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9963b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9963b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9963b-127">-WhatIf</span></span>
<span data-ttu-id="9963b-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9963b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9963b-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9963b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9963b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9963b-130">CommonParameters</span></span>
<span data-ttu-id="9963b-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9963b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9963b-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9963b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9963b-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9963b-133">INPUTS</span></span>

### <span data-ttu-id="9963b-134">Brak</span><span class="sxs-lookup"><span data-stu-id="9963b-134">None</span></span>

## <span data-ttu-id="9963b-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9963b-135">OUTPUTS</span></span>

### <span data-ttu-id="9963b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9963b-136">System.String</span></span>

## <span data-ttu-id="9963b-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9963b-137">NOTES</span></span>

## <span data-ttu-id="9963b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9963b-138">RELATED LINKS</span></span>
