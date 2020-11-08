---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 6a530a0e20f3e69540320ad3eab8b8cc7f37b5af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220895"
---
# <span data-ttu-id="21109-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="21109-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="21109-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21109-102">SYNOPSIS</span></span>
<span data-ttu-id="21109-103">Włącza aliasy prefiksów AzureRm dla modułów AZ.</span><span class="sxs-lookup"><span data-stu-id="21109-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="21109-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21109-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21109-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21109-105">DESCRIPTION</span></span>
<span data-ttu-id="21109-106">Włącza aliasy prefiksów AzureRm dla modułów AZ.</span><span class="sxs-lookup"><span data-stu-id="21109-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="21109-107">Jeśli określono-moduł, na liście będą dostępne tylko moduły.</span><span class="sxs-lookup"><span data-stu-id="21109-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="21109-108">W przeciwnym razie wszystkie aliasy AzureRm są włączone.</span><span class="sxs-lookup"><span data-stu-id="21109-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="21109-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21109-109">EXAMPLES</span></span>

### <span data-ttu-id="21109-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21109-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="21109-111">Włącza wszystkie prefiksy AzureRm dla bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="21109-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="21109-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="21109-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="21109-113">Włącza aliasy AzureRm dla modułu AZ. Accounts dla bieżącego procesu i dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="21109-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="21109-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21109-114">PARAMETERS</span></span>

### <span data-ttu-id="21109-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21109-115">-DefaultProfile</span></span>
<span data-ttu-id="21109-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21109-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21109-117">-Module</span><span class="sxs-lookup"><span data-stu-id="21109-117">-Module</span></span>
<span data-ttu-id="21109-118">Wskazuje moduły, dla których mają być włączone aliasy.</span><span class="sxs-lookup"><span data-stu-id="21109-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="21109-119">Jeśli nie określono żadnego, domyślnie przyjmowany jest wszystkie moduły.</span><span class="sxs-lookup"><span data-stu-id="21109-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="21109-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21109-120">-PassThru</span></span>
<span data-ttu-id="21109-121">Jeśli ta opcja jest określona, polecenie cmdlet zwróci wszystkie włączone aliasy</span><span class="sxs-lookup"><span data-stu-id="21109-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="21109-122">-Zakres</span><span class="sxs-lookup"><span data-stu-id="21109-122">-Scope</span></span>
<span data-ttu-id="21109-123">Wskazuje, dla których aliasów zakresu należy włączyć.</span><span class="sxs-lookup"><span data-stu-id="21109-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="21109-124">Domyślnie jest to "Local"</span><span class="sxs-lookup"><span data-stu-id="21109-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="21109-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21109-125">-Confirm</span></span>
<span data-ttu-id="21109-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21109-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21109-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21109-127">-WhatIf</span></span>
<span data-ttu-id="21109-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21109-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21109-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21109-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21109-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21109-130">CommonParameters</span></span>
<span data-ttu-id="21109-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21109-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21109-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21109-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21109-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21109-133">INPUTS</span></span>

### <span data-ttu-id="21109-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="21109-134">None</span></span>

## <span data-ttu-id="21109-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21109-135">OUTPUTS</span></span>

### <span data-ttu-id="21109-136">System. String</span><span class="sxs-lookup"><span data-stu-id="21109-136">System.String</span></span>

## <span data-ttu-id="21109-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21109-137">NOTES</span></span>

## <span data-ttu-id="21109-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21109-138">RELATED LINKS</span></span>
