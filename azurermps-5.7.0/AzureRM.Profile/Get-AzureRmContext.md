---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 96b9b5a6bec10082d7b004dcede73b743a7e538b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551691"
---
# <span data-ttu-id="3fabc-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="3fabc-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="3fabc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fabc-102">SYNOPSIS</span></span>
<span data-ttu-id="3fabc-103">Pobiera metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3fabc-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fabc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fabc-104">SYNTAX</span></span>

### <span data-ttu-id="3fabc-105">GetSingleContext (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3fabc-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="3fabc-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="3fabc-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fabc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3fabc-107">DESCRIPTION</span></span>
<span data-ttu-id="3fabc-108">Polecenie cmdlet Get-AzureRmContext pobiera bieżące metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3fabc-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="3fabc-109">To polecenie cmdlet umożliwia pobieranie konta usługi Active Directory, dzierżawy usługi Active Directory, subskrypcji platformy Azure i ukierunkowanego środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3fabc-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="3fabc-110">Polecenia cmdlet usługi Azure Resource Manager domyślnie wykorzystują te ustawienia podczas przeprowadzania żądań Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3fabc-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="3fabc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fabc-111">EXAMPLES</span></span>

### <span data-ttu-id="3fabc-112">Przykład 1. Uzyskiwanie bieżącego kontekstu</span><span class="sxs-lookup"><span data-stu-id="3fabc-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="3fabc-113">W tym przykładzie rejestrujemy się na naszym koncie za pomocą abonamentu na platformie Azure za pomocą funkcji Connect-AzureRmAccount, a następnie uzyskujemy kontekst bieżącej sesji przez nawiązanie połączenia Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="3fabc-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="3fabc-114">Przykład 2: wyświetlanie wszystkich dostępnych kontekstów</span><span class="sxs-lookup"><span data-stu-id="3fabc-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

<span data-ttu-id="3fabc-115">W tym przykładzie są wyświetlane wszystkie obecnie dostępne konteksty.</span><span class="sxs-lookup"><span data-stu-id="3fabc-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="3fabc-116">Użytkownik może wybrać jedno z tych kontekstów przy użyciu polecenia SELECT-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="3fabc-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="3fabc-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fabc-117">PARAMETERS</span></span>

### <span data-ttu-id="3fabc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fabc-118">-DefaultProfile</span></span>
<span data-ttu-id="3fabc-119">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3fabc-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fabc-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="3fabc-120">-ListAvailable</span></span>
<span data-ttu-id="3fabc-121">Wyświetlanie wszystkich dostępnych kontekstów w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="3fabc-121">List all available contexts in the current session.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllContexts
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fabc-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3fabc-122">-Name</span></span>
<span data-ttu-id="3fabc-123">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="3fabc-123">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fabc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fabc-124">CommonParameters</span></span>
<span data-ttu-id="3fabc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fabc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fabc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fabc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fabc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fabc-127">INPUTS</span></span>

### <span data-ttu-id="3fabc-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3fabc-128">None</span></span>
<span data-ttu-id="3fabc-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3fabc-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3fabc-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fabc-130">OUTPUTS</span></span>

### <span data-ttu-id="3fabc-131">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3fabc-131">PSAzureContext</span></span>
<span data-ttu-id="3fabc-132">To polecenie cmdlet zwraca konto, dzierżawcę i subskrypcję używane przez polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3fabc-132">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="3fabc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fabc-133">NOTES</span></span>

## <span data-ttu-id="3fabc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fabc-134">RELATED LINKS</span></span>

[<span data-ttu-id="3fabc-135">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="3fabc-135">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

