---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 1d5312cfaf7afb96149ae00b0e7900905206fb3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544940"
---
# <span data-ttu-id="a34ce-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="a34ce-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="a34ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a34ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a34ce-103">Pobiera dzierżawy autoryzowane na rzecz bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a34ce-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a34ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a34ce-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a34ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a34ce-105">DESCRIPTION</span></span>
<span data-ttu-id="a34ce-106">Polecenie cmdlet Get-AzureRmTenant pobiera dzierżawy autoryzowane na rzecz bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a34ce-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="a34ce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a34ce-107">EXAMPLES</span></span>

### <span data-ttu-id="a34ce-108">Przykład 1: uzyskiwanie wszystkich dzierżawców</span><span class="sxs-lookup"><span data-stu-id="a34ce-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="a34ce-109">W tym przykładzie pokazano, jak uzyskać wszystkich autoryzowanych dzierżawców konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a34ce-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="a34ce-110">Przykład 2: uzyskiwanie określonego dzierżawy</span><span class="sxs-lookup"><span data-stu-id="a34ce-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="a34ce-111">W tym przykładzie pokazano, jak uzyskać określoną autoryzowaną dzierżawę konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a34ce-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="a34ce-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a34ce-112">PARAMETERS</span></span>

### <span data-ttu-id="a34ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a34ce-113">-DefaultProfile</span></span>
<span data-ttu-id="a34ce-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a34ce-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a34ce-115">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="a34ce-115">-TenantId</span></span>
<span data-ttu-id="a34ce-116">Określa identyfikator dzierżawy, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a34ce-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a34ce-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34ce-117">CommonParameters</span></span>
<span data-ttu-id="a34ce-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a34ce-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34ce-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a34ce-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34ce-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a34ce-120">INPUTS</span></span>

### <span data-ttu-id="a34ce-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a34ce-121">System.String</span></span>

## <span data-ttu-id="a34ce-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a34ce-122">OUTPUTS</span></span>

### <span data-ttu-id="a34ce-123">Microsoft. Azure. Commands. profile. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="a34ce-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="a34ce-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a34ce-124">NOTES</span></span>

## <span data-ttu-id="a34ce-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a34ce-125">RELATED LINKS</span></span>
