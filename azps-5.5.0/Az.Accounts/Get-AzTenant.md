---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190475"
---
# <span data-ttu-id="bb259-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="bb259-101">Get-AzTenant</span></span>

## <span data-ttu-id="bb259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb259-102">SYNOPSIS</span></span>
<span data-ttu-id="bb259-103">Pobiera dzierżawy autoryzowane dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bb259-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="bb259-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb259-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb259-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb259-105">DESCRIPTION</span></span>
<span data-ttu-id="bb259-106">Polecenie Get-AzTenant cmdlet uzyskuje autoryzację dzierżaw dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bb259-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="bb259-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb259-107">EXAMPLES</span></span>

### <span data-ttu-id="bb259-108">Przykład 1. Uzyskiwanie wszystkich dzierżaw</span><span class="sxs-lookup"><span data-stu-id="bb259-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="bb259-109">W tym przykładzie pokazano, jak uzyskać wszystkie autoryzowane dzierżawy konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bb259-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="bb259-110">Przykład 2. Uzyskiwanie określonej dzierżawy</span><span class="sxs-lookup"><span data-stu-id="bb259-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="bb259-111">W tym przykładzie pokazano, jak uzyskać konkretną autoryzowaną dzierżawę konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bb259-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="bb259-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb259-112">PARAMETERS</span></span>

### <span data-ttu-id="bb259-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb259-113">-DefaultProfile</span></span>
<span data-ttu-id="bb259-114">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="bb259-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb259-115">- TenantId</span><span class="sxs-lookup"><span data-stu-id="bb259-115">-TenantId</span></span>
<span data-ttu-id="bb259-116">Określa identyfikator dzierżawy, do których otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb259-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bb259-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb259-117">CommonParameters</span></span>
<span data-ttu-id="bb259-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb259-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb259-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb259-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb259-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb259-120">INPUTS</span></span>

### <span data-ttu-id="bb259-121">System.String</span><span class="sxs-lookup"><span data-stu-id="bb259-121">System.String</span></span>

## <span data-ttu-id="bb259-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb259-122">OUTPUTS</span></span>

### <span data-ttu-id="bb259-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="bb259-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="bb259-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb259-124">NOTES</span></span>

## <span data-ttu-id="bb259-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb259-125">RELATED LINKS</span></span>
