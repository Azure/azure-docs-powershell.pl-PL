---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 8ac36dd86abb996a934b59d064980233c931d214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546112"
---
# <span data-ttu-id="18ad7-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="18ad7-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="18ad7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="18ad7-103">Pobiera dzierżawy autoryzowane na rzecz bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="18ad7-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18ad7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18ad7-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18ad7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="18ad7-106">Polecenie cmdlet Get-AzureRmTenant pobiera dzierżawy autoryzowane na rzecz bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="18ad7-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="18ad7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18ad7-107">EXAMPLES</span></span>

### <span data-ttu-id="18ad7-108">Przykład 1: uzyskiwanie wszystkich dzierżawców</span><span class="sxs-lookup"><span data-stu-id="18ad7-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="18ad7-109">W tym przykładzie pokazano, jak uzyskać wszystkich autoryzowanych dzierżawców konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="18ad7-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="18ad7-110">Przykład 2: uzyskiwanie określonego dzierżawy</span><span class="sxs-lookup"><span data-stu-id="18ad7-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="18ad7-111">W tym przykładzie pokazano, jak uzyskać określoną autoryzowaną dzierżawę konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="18ad7-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="18ad7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18ad7-112">PARAMETERS</span></span>

### <span data-ttu-id="18ad7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ad7-113">-DefaultProfile</span></span>
<span data-ttu-id="18ad7-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="18ad7-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ad7-115">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="18ad7-115">-TenantId</span></span>
<span data-ttu-id="18ad7-116">Określa identyfikator dzierżawy, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ad7-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ad7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ad7-117">CommonParameters</span></span>
<span data-ttu-id="18ad7-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ad7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ad7-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ad7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ad7-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18ad7-120">INPUTS</span></span>

## <span data-ttu-id="18ad7-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18ad7-121">OUTPUTS</span></span>

### <span data-ttu-id="18ad7-122">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="18ad7-122">PSAzureTenant</span></span>
<span data-ttu-id="18ad7-123">To polecenie cmdlet zwraca identyfikator dzierżawy i powiązane informacje o domenie dla dzierżaw autoryzowanych dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="18ad7-123">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="18ad7-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18ad7-124">NOTES</span></span>

## <span data-ttu-id="18ad7-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18ad7-125">RELATED LINKS</span></span>

