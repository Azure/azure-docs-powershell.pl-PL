---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
ms.openlocfilehash: 35f63b4655b92e42eb0a7d1bae70e2ef01c57a02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545084"
---
# <span data-ttu-id="2b552-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2b552-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="2b552-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b552-102">SYNOPSIS</span></span>
<span data-ttu-id="2b552-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="2b552-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b552-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b552-104">SYNTAX</span></span>

### <span data-ttu-id="2b552-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="2b552-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b552-106">Większa</span><span class="sxs-lookup"><span data-stu-id="2b552-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b552-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2b552-107">DESCRIPTION</span></span>
<span data-ttu-id="2b552-108">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="2b552-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2b552-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b552-109">EXAMPLES</span></span>

### <span data-ttu-id="2b552-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2b552-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2b552-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="2b552-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="2b552-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b552-112">PARAMETERS</span></span>

### <span data-ttu-id="2b552-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b552-113">-DefaultProfile</span></span>
<span data-ttu-id="2b552-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b552-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b552-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="2b552-115">-ExpandResource</span></span>
<span data-ttu-id="2b552-116">Odwołanie do zasobu, które ma zostać rozwinięte.</span><span class="sxs-lookup"><span data-stu-id="2b552-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b552-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b552-117">-Name</span></span>
<span data-ttu-id="2b552-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="2b552-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b552-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b552-119">-ResourceGroupName</span></span>
<span data-ttu-id="2b552-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2b552-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b552-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b552-121">CommonParameters</span></span>
<span data-ttu-id="2b552-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b552-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b552-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b552-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b552-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b552-124">INPUTS</span></span>

### <span data-ttu-id="2b552-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2b552-125">System.String</span></span>

## <span data-ttu-id="2b552-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b552-126">OUTPUTS</span></span>

### <span data-ttu-id="2b552-127">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2b552-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2b552-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b552-128">NOTES</span></span>

## <span data-ttu-id="2b552-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b552-129">RELATED LINKS</span></span>
