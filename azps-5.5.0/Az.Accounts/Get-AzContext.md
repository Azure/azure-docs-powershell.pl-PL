---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178123"
---
# <span data-ttu-id="3f1fb-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="3f1fb-101">Get-AzContext</span></span>

## <span data-ttu-id="3f1fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f1fb-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1fb-103">Pobiera metadane używane do uwierzytelniania żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3f1fb-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="3f1fb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3f1fb-104">SYNTAX</span></span>

### <span data-ttu-id="3f1fb-105">GetSingleContext (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3f1fb-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="3f1fb-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="3f1fb-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f1fb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3f1fb-107">DESCRIPTION</span></span>
<span data-ttu-id="3f1fb-108">Polecenie Get-AzContext pobiera bieżące metadane używane do uwierzytelniania żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3f1fb-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="3f1fb-109">To polecenie cmdlet pobiera konto usługi Active Directory, dzierżawę usługi Active Directory, subskrypcję platformy Azure i docelowe środowisko platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f1fb-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="3f1fb-110">Polecenia cmdlet usługi Azure Resource Manager używają tych ustawień domyślnie podczas tworzenia żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3f1fb-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="3f1fb-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3f1fb-111">EXAMPLES</span></span>

### <span data-ttu-id="3f1fb-112">Przykład 1. Uzyskiwanie bieżącego kontekstu</span><span class="sxs-lookup"><span data-stu-id="3f1fb-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="3f1fb-113">W tym przykładzie logujesz się do naszego konta za pomocą subskrypcji platformy Azure przy użyciu funkcji Connect-AzAccount, a następnie łączymy się z kontekstem bieżącej sesji, dzwoniąc do get-azContext.</span><span class="sxs-lookup"><span data-stu-id="3f1fb-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="3f1fb-114">Przykład 2. Wyświetlanie listy wszystkich dostępnych kontekstów</span><span class="sxs-lookup"><span data-stu-id="3f1fb-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="3f1fb-115">W tym przykładzie są wyświetlane wszystkie obecnie dostępne konteksty.</span><span class="sxs-lookup"><span data-stu-id="3f1fb-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="3f1fb-116">Użytkownik może wybrać jeden z tych kontekstów przy użyciu instrukcji Select-AzContext.</span><span class="sxs-lookup"><span data-stu-id="3f1fb-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="3f1fb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f1fb-117">PARAMETERS</span></span>

### <span data-ttu-id="3f1fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1fb-118">-DefaultProfile</span></span>
<span data-ttu-id="3f1fb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3f1fb-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f1fb-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="3f1fb-120">-ListAvailable</span></span>
<span data-ttu-id="3f1fb-121">Lista wszystkich dostępnych kontekstów w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="3f1fb-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="3f1fb-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3f1fb-122">-Name</span></span>
<span data-ttu-id="3f1fb-123">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="3f1fb-123">The name of the context</span></span>

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

### <span data-ttu-id="3f1fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1fb-124">CommonParameters</span></span>
<span data-ttu-id="3f1fb-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f1fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1fb-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f1fb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1fb-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f1fb-127">INPUTS</span></span>

### <span data-ttu-id="3f1fb-128">Brak</span><span class="sxs-lookup"><span data-stu-id="3f1fb-128">None</span></span>

## <span data-ttu-id="3f1fb-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f1fb-129">OUTPUTS</span></span>

### <span data-ttu-id="3f1fb-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3f1fb-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="3f1fb-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3f1fb-131">NOTES</span></span>

## <span data-ttu-id="3f1fb-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f1fb-132">RELATED LINKS</span></span>

[<span data-ttu-id="3f1fb-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="3f1fb-133">Set-AzContext</span></span>](./Set-AzContext.md)

