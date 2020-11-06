---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523397"
---
# <span data-ttu-id="53e40-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="53e40-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="53e40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53e40-102">SYNOPSIS</span></span>
<span data-ttu-id="53e40-103">Pobiera dzierżawy autoryzowane na rzecz bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="53e40-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="53e40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53e40-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="53e40-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53e40-105">DESCRIPTION</span></span>
<span data-ttu-id="53e40-106">Polecenie cmdlet Get-AzureRmTenant pobiera dzierżawy autoryzowane na rzecz bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="53e40-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="53e40-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53e40-107">EXAMPLES</span></span>

### <span data-ttu-id="53e40-108">Przykład 1: uzyskiwanie wszystkich dzierżawców</span><span class="sxs-lookup"><span data-stu-id="53e40-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="53e40-109">W tym przykładzie pokazano, jak uzyskać wszystkich autoryzowanych dzierżawców konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53e40-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="53e40-110">Przykład 2: uzyskiwanie określonego dzierżawy</span><span class="sxs-lookup"><span data-stu-id="53e40-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="53e40-111">W tym przykładzie pokazano, jak uzyskać określoną autoryzowaną dzierżawę konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53e40-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="53e40-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53e40-112">PARAMETERS</span></span>

### <span data-ttu-id="53e40-113">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="53e40-113">-TenantId</span></span>
<span data-ttu-id="53e40-114">Określa identyfikator dzierżawy, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53e40-114">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="53e40-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e40-115">CommonParameters</span></span>
<span data-ttu-id="53e40-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53e40-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e40-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53e40-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e40-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53e40-118">INPUTS</span></span>

## <span data-ttu-id="53e40-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53e40-119">OUTPUTS</span></span>

### <span data-ttu-id="53e40-120">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="53e40-120">PSAzureTenant</span></span>
<span data-ttu-id="53e40-121">To polecenie cmdlet zwraca identyfikator dzierżawy i powiązane informacje o domenie dla dzierżaw autoryzowanych dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="53e40-121">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="53e40-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53e40-122">NOTES</span></span>

## <span data-ttu-id="53e40-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53e40-123">RELATED LINKS</span></span>

