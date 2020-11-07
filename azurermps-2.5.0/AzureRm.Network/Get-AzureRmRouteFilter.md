---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 007f020d97d0c46f5db5031f4163d669d976f642
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899260"
---
# <span data-ttu-id="4a418-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4a418-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="4a418-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a418-102">SYNOPSIS</span></span>
<span data-ttu-id="4a418-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="4a418-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a418-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a418-104">SYNTAX</span></span>

### <span data-ttu-id="4a418-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="4a418-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a418-106">Większa</span><span class="sxs-lookup"><span data-stu-id="4a418-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a418-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4a418-107">DESCRIPTION</span></span>
<span data-ttu-id="4a418-108">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="4a418-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="4a418-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a418-109">EXAMPLES</span></span>

### <span data-ttu-id="4a418-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a418-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4a418-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="4a418-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="4a418-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a418-112">PARAMETERS</span></span>

### <span data-ttu-id="4a418-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a418-113">-DefaultProfile</span></span>
<span data-ttu-id="4a418-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a418-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a418-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4a418-115">-ExpandResource</span></span>
<span data-ttu-id="4a418-116">Odwołanie do zasobu, które ma zostać rozwinięte.</span><span class="sxs-lookup"><span data-stu-id="4a418-116">The resource reference to be expanded.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a418-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a418-117">-Name</span></span>
<span data-ttu-id="4a418-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4a418-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a418-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a418-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a418-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a418-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a418-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a418-121">CommonParameters</span></span>
<span data-ttu-id="4a418-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a418-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a418-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a418-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a418-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a418-124">INPUTS</span></span>

### <span data-ttu-id="4a418-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4a418-125">System.String</span></span>

## <span data-ttu-id="4a418-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a418-126">OUTPUTS</span></span>

### <span data-ttu-id="4a418-127">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4a418-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4a418-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a418-128">NOTES</span></span>

## <span data-ttu-id="4a418-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a418-129">RELATED LINKS</span></span>

