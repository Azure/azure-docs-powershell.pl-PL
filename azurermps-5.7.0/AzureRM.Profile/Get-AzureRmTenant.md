---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 7d9687877e3a27d175719a7a7b9ec6c78a529e52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549631"
---
# <span data-ttu-id="89f32-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="89f32-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="89f32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89f32-102">SYNOPSIS</span></span>
<span data-ttu-id="89f32-103">Pobiera dzierżawy autoryzowane na rzecz bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89f32-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89f32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89f32-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89f32-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89f32-105">DESCRIPTION</span></span>
<span data-ttu-id="89f32-106">Polecenie cmdlet Get-AzureRmTenant pobiera dzierżawy autoryzowane na rzecz bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89f32-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="89f32-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89f32-107">EXAMPLES</span></span>

### <span data-ttu-id="89f32-108">Przykład 1: uzyskiwanie wszystkich dzierżawców</span><span class="sxs-lookup"><span data-stu-id="89f32-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="89f32-109">W tym przykładzie pokazano, jak uzyskać wszystkich autoryzowanych dzierżawców konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="89f32-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="89f32-110">Przykład 2: uzyskiwanie określonego dzierżawy</span><span class="sxs-lookup"><span data-stu-id="89f32-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="89f32-111">W tym przykładzie pokazano, jak uzyskać określoną autoryzowaną dzierżawę konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="89f32-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="89f32-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89f32-112">PARAMETERS</span></span>

### <span data-ttu-id="89f32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f32-113">-DefaultProfile</span></span>
<span data-ttu-id="89f32-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="89f32-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89f32-115">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="89f32-115">-TenantId</span></span>
<span data-ttu-id="89f32-116">Określa identyfikator dzierżawy, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f32-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f32-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f32-117">CommonParameters</span></span>
<span data-ttu-id="89f32-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f32-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f32-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f32-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f32-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89f32-120">INPUTS</span></span>

### <span data-ttu-id="89f32-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="89f32-121">None</span></span>
<span data-ttu-id="89f32-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="89f32-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="89f32-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89f32-123">OUTPUTS</span></span>

### <span data-ttu-id="89f32-124">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="89f32-124">PSAzureTenant</span></span>
<span data-ttu-id="89f32-125">To polecenie cmdlet zwraca identyfikator dzierżawy i powiązane informacje o domenie dla dzierżaw autoryzowanych dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="89f32-125">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="89f32-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89f32-126">NOTES</span></span>

## <span data-ttu-id="89f32-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89f32-127">RELATED LINKS</span></span>

