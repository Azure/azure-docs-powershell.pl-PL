---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219519"
---
# <span data-ttu-id="f3710-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f3710-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="f3710-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3710-102">SYNOPSIS</span></span>
<span data-ttu-id="f3710-103">Pobiera zasób link prywatny.</span><span class="sxs-lookup"><span data-stu-id="f3710-103">Gets a private link resource.</span></span>

## <span data-ttu-id="f3710-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3710-104">SYNTAX</span></span>

### <span data-ttu-id="f3710-105">ByPrivateLinkResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3710-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3710-106">Opis</span><span class="sxs-lookup"><span data-stu-id="f3710-106">DESCRIPTION</span></span>
<span data-ttu-id="f3710-107">Polecenie cmdlet **Get-AzPrivateLinkResource** pobiera wszystkie zasoby linku do PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="f3710-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="f3710-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3710-108">EXAMPLES</span></span>

### <span data-ttu-id="f3710-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3710-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="f3710-110">W tym przykładzie podano listę wszystkich prywatnych zasobów linków nbelong do programu SQL Server o nazwie mySql.</span><span class="sxs-lookup"><span data-stu-id="f3710-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="f3710-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3710-111">PARAMETERS</span></span>

### <span data-ttu-id="f3710-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3710-112">-DefaultProfile</span></span>
<span data-ttu-id="f3710-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3710-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3710-114">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f3710-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="f3710-115">Identyfikator Menedżera zasobów platformy Azure zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="f3710-115">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3710-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3710-116">CommonParameters</span></span>
<span data-ttu-id="f3710-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3710-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3710-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3710-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3710-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3710-119">INPUTS</span></span>

### <span data-ttu-id="f3710-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f3710-120">System.String</span></span>

## <span data-ttu-id="f3710-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3710-121">OUTPUTS</span></span>

### <span data-ttu-id="f3710-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3710-122">System.Boolean</span></span>

## <span data-ttu-id="f3710-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3710-123">NOTES</span></span>

## <span data-ttu-id="f3710-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3710-124">RELATED LINKS</span></span>
