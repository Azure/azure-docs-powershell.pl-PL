---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd280133b3a0bc536c57f839fcc0faab81669c03
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889810"
---
# <span data-ttu-id="71b96-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="71b96-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="71b96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71b96-102">SYNOPSIS</span></span>
<span data-ttu-id="71b96-103">Zwraca listę wszystkich Farm przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="71b96-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="71b96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71b96-104">SYNTAX</span></span>

### <span data-ttu-id="71b96-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="71b96-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="71b96-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="71b96-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="71b96-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="71b96-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="71b96-108">Opis</span><span class="sxs-lookup"><span data-stu-id="71b96-108">DESCRIPTION</span></span>
<span data-ttu-id="71b96-109">Zwraca listę wszystkich Farm przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="71b96-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="71b96-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71b96-110">EXAMPLES</span></span>

### <span data-ttu-id="71b96-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="71b96-111">EXAMPLE 1</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="71b96-112">Pobierz listę wszystkich Farm magazynowania.</span><span class="sxs-lookup"><span data-stu-id="71b96-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="71b96-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71b96-113">PARAMETERS</span></span>

### <span data-ttu-id="71b96-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71b96-114">-Name</span></span>
<span data-ttu-id="71b96-115">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="71b96-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b96-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b96-116">-ResourceGroupName</span></span>
<span data-ttu-id="71b96-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="71b96-117">Resource group name.</span></span>

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

### <span data-ttu-id="71b96-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71b96-118">-ResourceId</span></span>
<span data-ttu-id="71b96-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="71b96-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b96-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="71b96-120">-Skip</span></span>
<span data-ttu-id="71b96-121">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="71b96-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b96-122">-Początek</span><span class="sxs-lookup"><span data-stu-id="71b96-122">-Top</span></span>
<span data-ttu-id="71b96-123">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="71b96-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="71b96-124">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="71b96-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b96-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b96-125">CommonParameters</span></span>
<span data-ttu-id="71b96-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b96-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b96-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b96-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b96-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71b96-128">INPUTS</span></span>

## <span data-ttu-id="71b96-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71b96-129">OUTPUTS</span></span>

### <span data-ttu-id="71b96-130">Microsoft. AzureStack. Management. Storage. admin. modele. farma</span><span class="sxs-lookup"><span data-stu-id="71b96-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="71b96-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71b96-131">NOTES</span></span>

## <span data-ttu-id="71b96-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71b96-132">RELATED LINKS</span></span>
