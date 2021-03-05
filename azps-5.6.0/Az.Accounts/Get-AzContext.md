---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 2060a1cbe9f002a20b94e82ac9547c5fc96c0e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010129"
---
# <span data-ttu-id="a8c4c-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="a8c4c-101">Get-AzContext</span></span>

## <span data-ttu-id="a8c4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c4c-103">Pobiera metadane używane do uwierzytelniania żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a8c4c-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="a8c4c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a8c4c-104">SYNTAX</span></span>

### <span data-ttu-id="a8c4c-105">GetSingleContext (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a8c4c-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="a8c4c-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="a8c4c-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-RefreshContextFromTokenCache] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8c4c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a8c4c-107">DESCRIPTION</span></span>
<span data-ttu-id="a8c4c-108">Polecenie Get-AzContext pobiera bieżące metadane używane do uwierzytelniania żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a8c4c-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="a8c4c-109">To polecenie cmdlet pobiera konto usługi Active Directory, dzierżawę usługi Active Directory, subskrypcję platformy Azure i docelowe środowisko platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a8c4c-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="a8c4c-110">Polecenia cmdlet usługi Azure Resource Manager używają tych ustawień domyślnie podczas tworzenia żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a8c4c-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="a8c4c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a8c4c-111">EXAMPLES</span></span>

### <span data-ttu-id="a8c4c-112">Przykład 1. Uzyskiwanie bieżącego kontekstu</span><span class="sxs-lookup"><span data-stu-id="a8c4c-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="a8c4c-113">W tym przykładzie logujesz się do naszego konta za pomocą subskrypcji platformy Azure przy użyciu funkcji Connect-AzAccount, a następnie łączymy się z kontekstem bieżącej sesji, dzwoniąc do get-azContext.</span><span class="sxs-lookup"><span data-stu-id="a8c4c-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="a8c4c-114">Przykład 2. Wyświetlanie listy wszystkich dostępnych kontekstów</span><span class="sxs-lookup"><span data-stu-id="a8c4c-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="a8c4c-115">W tym przykładzie są wyświetlane wszystkie obecnie dostępne konteksty.</span><span class="sxs-lookup"><span data-stu-id="a8c4c-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="a8c4c-116">Użytkownik może wybrać jeden z tych kontekstów przy użyciu instrukcji Select-AzContext.</span><span class="sxs-lookup"><span data-stu-id="a8c4c-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="a8c4c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8c4c-117">PARAMETERS</span></span>

### <span data-ttu-id="a8c4c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c4c-118">-DefaultProfile</span></span>
<span data-ttu-id="a8c4c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a8c4c-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8c4c-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="a8c4c-120">-ListAvailable</span></span>
<span data-ttu-id="a8c4c-121">Lista wszystkich dostępnych kontekstów w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="a8c4c-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="a8c4c-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a8c4c-122">-Name</span></span>
<span data-ttu-id="a8c4c-123">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="a8c4c-123">The name of the context</span></span>

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

### <span data-ttu-id="a8c4c-124">-RefreshContextFromTokenCache</span><span class="sxs-lookup"><span data-stu-id="a8c4c-124">-RefreshContextFromTokenCache</span></span>
<span data-ttu-id="a8c4c-125">Odświeżanie kontekstów z pamięci podręcznej tokenów</span><span class="sxs-lookup"><span data-stu-id="a8c4c-125">Refresh contexts from token cache</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c4c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c4c-126">CommonParameters</span></span>
<span data-ttu-id="a8c4c-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c4c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c4c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8c4c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c4c-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8c4c-129">INPUTS</span></span>

### <span data-ttu-id="a8c4c-130">Brak</span><span class="sxs-lookup"><span data-stu-id="a8c4c-130">None</span></span>

## <span data-ttu-id="a8c4c-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8c4c-131">OUTPUTS</span></span>

### <span data-ttu-id="a8c4c-132">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a8c4c-132">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="a8c4c-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a8c4c-133">NOTES</span></span>

## <span data-ttu-id="a8c4c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8c4c-134">RELATED LINKS</span></span>

[<span data-ttu-id="a8c4c-135">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="a8c4c-135">Set-AzContext</span></span>](./Set-AzContext.md)

