---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523402"
---
# <span data-ttu-id="846fe-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="846fe-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="846fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="846fe-102">SYNOPSIS</span></span>
<span data-ttu-id="846fe-103">Pobiera metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="846fe-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="846fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="846fe-104">SYNTAX</span></span>

```
Get-AzureRmContext [<CommonParameters>]
```

## <span data-ttu-id="846fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="846fe-105">DESCRIPTION</span></span>
<span data-ttu-id="846fe-106">Polecenie cmdlet Get-AzureRmContext pobiera bieżące metadane używane do uwierzytelniania żądań Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="846fe-106">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="846fe-107">To polecenie cmdlet umożliwia pobieranie konta usługi Active Directory, dzierżawy usługi Active Directory, subskrypcji platformy Azure i ukierunkowanego środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="846fe-107">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="846fe-108">Polecenia cmdlet usługi Azure Resource Manager domyślnie wykorzystują te ustawienia podczas przeprowadzania żądań Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="846fe-108">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="846fe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="846fe-109">EXAMPLES</span></span>

### <span data-ttu-id="846fe-110">Przykład 1. Uzyskiwanie bieżącego kontekstu</span><span class="sxs-lookup"><span data-stu-id="846fe-110">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="846fe-111">W tym przykładzie będziemy logować się na naszym koncie za pomocą subskrypcji usługi Azure przy użyciu dodatku Add-AzureRmAccount, a następnie uzyskujemy kontekst bieżącej sesji przez dzwonienie do funkcji Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="846fe-111">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

## <span data-ttu-id="846fe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="846fe-112">PARAMETERS</span></span>

### <span data-ttu-id="846fe-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="846fe-113">CommonParameters</span></span>
<span data-ttu-id="846fe-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="846fe-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="846fe-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="846fe-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="846fe-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="846fe-116">INPUTS</span></span>

## <span data-ttu-id="846fe-117">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="846fe-117">OUTPUTS</span></span>

### <span data-ttu-id="846fe-118">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="846fe-118">PSAzureContext</span></span>
<span data-ttu-id="846fe-119">To polecenie cmdlet zwraca konto, dzierżawcę i subskrypcję używane przez polecenia cmdlet Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="846fe-119">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="846fe-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="846fe-120">NOTES</span></span>

## <span data-ttu-id="846fe-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="846fe-121">RELATED LINKS</span></span>

[<span data-ttu-id="846fe-122">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="846fe-122">Set-AzureRMContext</span></span>]()

