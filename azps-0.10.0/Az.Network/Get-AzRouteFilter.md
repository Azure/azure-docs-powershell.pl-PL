---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 1d914509b43dd59d95d32a11c3f5ce3487b03e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890682"
---
# <span data-ttu-id="4472a-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4472a-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="4472a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4472a-102">SYNOPSIS</span></span>
<span data-ttu-id="4472a-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="4472a-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="4472a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4472a-104">SYNTAX</span></span>

### <span data-ttu-id="4472a-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="4472a-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4472a-106">Większa</span><span class="sxs-lookup"><span data-stu-id="4472a-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4472a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4472a-107">DESCRIPTION</span></span>
<span data-ttu-id="4472a-108">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="4472a-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="4472a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4472a-109">EXAMPLES</span></span>

### <span data-ttu-id="4472a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4472a-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4472a-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="4472a-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="4472a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4472a-112">PARAMETERS</span></span>

### <span data-ttu-id="4472a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4472a-113">-DefaultProfile</span></span>
<span data-ttu-id="4472a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4472a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4472a-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4472a-115">-ExpandResource</span></span>
<span data-ttu-id="4472a-116">Odwołanie do zasobu, które ma zostać rozwinięte.</span><span class="sxs-lookup"><span data-stu-id="4472a-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="4472a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4472a-117">-Name</span></span>
<span data-ttu-id="4472a-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4472a-118">The resource name.</span></span>

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

### <span data-ttu-id="4472a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4472a-119">-ResourceGroupName</span></span>
<span data-ttu-id="4472a-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4472a-120">The resource group name.</span></span>

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

### <span data-ttu-id="4472a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4472a-121">CommonParameters</span></span>
<span data-ttu-id="4472a-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4472a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4472a-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4472a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4472a-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4472a-124">INPUTS</span></span>

### <span data-ttu-id="4472a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4472a-125">System.String</span></span>

## <span data-ttu-id="4472a-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4472a-126">OUTPUTS</span></span>

### <span data-ttu-id="4472a-127">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4472a-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4472a-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4472a-128">NOTES</span></span>

## <span data-ttu-id="4472a-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4472a-129">RELATED LINKS</span></span>

