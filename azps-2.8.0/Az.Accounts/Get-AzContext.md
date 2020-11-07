---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 0f306b7e42dbe5b37c1c814a9458a5e1fb81cc7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707227"
---
# <span data-ttu-id="77681-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="77681-101">Get-AzContext</span></span>

## <span data-ttu-id="77681-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77681-102">SYNOPSIS</span></span>
<span data-ttu-id="77681-103">Pobiera metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="77681-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="77681-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77681-104">SYNTAX</span></span>

### <span data-ttu-id="77681-105">GetSingleContext (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77681-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="77681-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="77681-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77681-107">Opis</span><span class="sxs-lookup"><span data-stu-id="77681-107">DESCRIPTION</span></span>
<span data-ttu-id="77681-108">Polecenie cmdlet Get-AzContext pobiera bieżące metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="77681-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="77681-109">To polecenie cmdlet umożliwia pobieranie konta usługi Active Directory, dzierżawy usługi Active Directory, subskrypcji platformy Azure i ukierunkowanego środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="77681-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="77681-110">Polecenia cmdlet usługi Azure Resource Manager domyślnie wykorzystują te ustawienia podczas przeprowadzania żądań Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="77681-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="77681-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77681-111">EXAMPLES</span></span>

### <span data-ttu-id="77681-112">Przykład 1. Uzyskiwanie bieżącego kontekstu</span><span class="sxs-lookup"><span data-stu-id="77681-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="77681-113">W tym przykładzie rejestrujemy się na naszym koncie za pomocą abonamentu na platformie Azure za pomocą funkcji Connect-AzAccount, a następnie uzyskujemy kontekst bieżącej sesji przez nawiązanie połączenia Get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="77681-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="77681-114">Przykład 2: wyświetlanie wszystkich dostępnych kontekstów</span><span class="sxs-lookup"><span data-stu-id="77681-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="77681-115">W tym przykładzie są wyświetlane wszystkie obecnie dostępne konteksty.</span><span class="sxs-lookup"><span data-stu-id="77681-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="77681-116">Użytkownik może wybrać jedno z tych kontekstów przy użyciu polecenia SELECT-AzContext.</span><span class="sxs-lookup"><span data-stu-id="77681-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="77681-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77681-117">PARAMETERS</span></span>

### <span data-ttu-id="77681-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77681-118">-DefaultProfile</span></span>
<span data-ttu-id="77681-119">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="77681-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77681-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="77681-120">-ListAvailable</span></span>
<span data-ttu-id="77681-121">Wyświetlanie wszystkich dostępnych kontekstów w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="77681-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77681-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77681-122">-Name</span></span>
<span data-ttu-id="77681-123">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="77681-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77681-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77681-124">CommonParameters</span></span>
<span data-ttu-id="77681-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77681-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77681-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77681-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77681-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77681-127">INPUTS</span></span>

### <span data-ttu-id="77681-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="77681-128">None</span></span>

## <span data-ttu-id="77681-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77681-129">OUTPUTS</span></span>

### <span data-ttu-id="77681-130">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="77681-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="77681-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77681-131">NOTES</span></span>

## <span data-ttu-id="77681-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77681-132">RELATED LINKS</span></span>

[<span data-ttu-id="77681-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="77681-133">Set-AzContext</span></span>](./Set-AzContext.md)

