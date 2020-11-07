---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f8c9192100536a04b664f981a9df9e1508a1f87
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889757"
---
# <span data-ttu-id="ffea9-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="ffea9-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="ffea9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffea9-102">SYNOPSIS</span></span>
<span data-ttu-id="ffea9-103">Zwraca listę udziałów w magazynie.</span><span class="sxs-lookup"><span data-stu-id="ffea9-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="ffea9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffea9-104">SYNTAX</span></span>

### <span data-ttu-id="ffea9-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ffea9-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ffea9-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ffea9-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -ShareName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ffea9-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="ffea9-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ffea9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ffea9-108">DESCRIPTION</span></span>
<span data-ttu-id="ffea9-109">Zwraca listę udziałów w magazynie.</span><span class="sxs-lookup"><span data-stu-id="ffea9-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="ffea9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffea9-110">EXAMPLES</span></span>

### <span data-ttu-id="ffea9-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="ffea9-111">EXAMPLE 1</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="ffea9-112">Pobierz listę udziałów w magazynie.</span><span class="sxs-lookup"><span data-stu-id="ffea9-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="ffea9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffea9-113">PARAMETERS</span></span>

### <span data-ttu-id="ffea9-114">-Farmname</span><span class="sxs-lookup"><span data-stu-id="ffea9-114">-FarmName</span></span>
<span data-ttu-id="ffea9-115">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="ffea9-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffea9-116">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="ffea9-116">-ShareName</span></span>
<span data-ttu-id="ffea9-117">Nazwa udziału.</span><span class="sxs-lookup"><span data-stu-id="ffea9-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffea9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffea9-118">-ResourceGroupName</span></span>
<span data-ttu-id="ffea9-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffea9-119">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffea9-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffea9-120">-ResourceId</span></span>
<span data-ttu-id="ffea9-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ffea9-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffea9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffea9-122">CommonParameters</span></span>
<span data-ttu-id="ffea9-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffea9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffea9-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffea9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffea9-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffea9-125">INPUTS</span></span>

## <span data-ttu-id="ffea9-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffea9-126">OUTPUTS</span></span>

### <span data-ttu-id="ffea9-127">Microsoft. AzureStack. Management. Storage. admin. models. Share</span><span class="sxs-lookup"><span data-stu-id="ffea9-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="ffea9-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffea9-128">NOTES</span></span>

## <span data-ttu-id="ffea9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffea9-129">RELATED LINKS</span></span>
