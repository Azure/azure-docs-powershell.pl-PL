---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: d230a00701330caee83d9db6f0a41d4e26446aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704776"
---
# <span data-ttu-id="6a0e6-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="6a0e6-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="6a0e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a0e6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a0e6-103">Wyłącza aliasy prefiksów AzureRm dla modułów AZ.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="6a0e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a0e6-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a0e6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a0e6-105">DESCRIPTION</span></span>
<span data-ttu-id="6a0e6-106">Wyłącza aliasy prefiksów AzureRm dla modułów AZ.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="6a0e6-107">W przypadku określenia modułu jeżeli aliasy są wyłączone, na liście będą dostępne tylko moduły.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="6a0e6-108">W przeciwnym razie wszystkie aliasy AzureRm są wyłączone.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="6a0e6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a0e6-109">EXAMPLES</span></span>

### <span data-ttu-id="6a0e6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6a0e6-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="6a0e6-111">Wyłącza wszystkie prefiksy AzureRm dla bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="6a0e6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6a0e6-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="6a0e6-113">Wyłącza aliasy AzureRm dla modułu AZ. Accounts zarówno dla bieżącego procesu, jak i dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="6a0e6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a0e6-114">PARAMETERS</span></span>

### <span data-ttu-id="6a0e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a0e6-115">-DefaultProfile</span></span>
<span data-ttu-id="6a0e6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a0e6-117">-Module</span><span class="sxs-lookup"><span data-stu-id="6a0e6-117">-Module</span></span>
<span data-ttu-id="6a0e6-118">Wskazuje moduły, dla których mają zostać wyłączone aliasy.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="6a0e6-119">Jeśli nie określono żadnej wartości, domyślnie są włączone wszystkie moduły.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="6a0e6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a0e6-120">-PassThru</span></span>
<span data-ttu-id="6a0e6-121">Jeśli ta opcja jest określona, polecenie cmdlet zwróci wszystkie wyłączone aliasy</span><span class="sxs-lookup"><span data-stu-id="6a0e6-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="6a0e6-122">-Zakres</span><span class="sxs-lookup"><span data-stu-id="6a0e6-122">-Scope</span></span>
<span data-ttu-id="6a0e6-123">Wskazuje, że aliasy zakresu powinny być wyłączone.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="6a0e6-124">Domyślna to "Process"</span><span class="sxs-lookup"><span data-stu-id="6a0e6-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="6a0e6-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a0e6-125">-Confirm</span></span>
<span data-ttu-id="6a0e6-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a0e6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a0e6-127">-WhatIf</span></span>
<span data-ttu-id="6a0e6-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a0e6-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a0e6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a0e6-130">CommonParameters</span></span>
<span data-ttu-id="6a0e6-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a0e6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a0e6-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a0e6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a0e6-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a0e6-133">INPUTS</span></span>

### <span data-ttu-id="6a0e6-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6a0e6-134">None</span></span>

## <span data-ttu-id="6a0e6-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a0e6-135">OUTPUTS</span></span>

### <span data-ttu-id="6a0e6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6a0e6-136">System.String</span></span>

## <span data-ttu-id="6a0e6-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a0e6-137">NOTES</span></span>

## <span data-ttu-id="6a0e6-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a0e6-138">RELATED LINKS</span></span>
