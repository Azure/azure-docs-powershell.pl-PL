---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 687838573459c09ceaf08c0d1c3335caa4a99769
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061636"
---
# <span data-ttu-id="6dd28-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="6dd28-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="6dd28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6dd28-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd28-103">Zwraca listę przydziałów magazynowania w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="6dd28-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="6dd28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6dd28-104">SYNTAX</span></span>

### <span data-ttu-id="6dd28-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6dd28-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6dd28-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="6dd28-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="6dd28-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="6dd28-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6dd28-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6dd28-108">DESCRIPTION</span></span>
<span data-ttu-id="6dd28-109">Zwraca listę przydziałów magazynowania w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="6dd28-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="6dd28-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6dd28-110">EXAMPLES</span></span>

### <span data-ttu-id="6dd28-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="6dd28-111">EXAMPLE 1</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="6dd28-112">Uzyskaj listę przydziałów magazynowania.</span><span class="sxs-lookup"><span data-stu-id="6dd28-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="6dd28-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="6dd28-113">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="6dd28-114">Uzyskaj szczegółowe informacje o określonym przydziale magazynowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6dd28-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="6dd28-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6dd28-115">PARAMETERS</span></span>

### <span data-ttu-id="6dd28-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6dd28-116">-Name</span></span>
<span data-ttu-id="6dd28-117">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="6dd28-117">The name of the storage quota.</span></span>

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

### <span data-ttu-id="6dd28-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6dd28-118">-Location</span></span>
<span data-ttu-id="6dd28-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="6dd28-119">Resource location.</span></span>

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

### <span data-ttu-id="6dd28-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dd28-120">-ResourceId</span></span>
<span data-ttu-id="6dd28-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="6dd28-121">The resource id.</span></span>

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

### <span data-ttu-id="6dd28-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="6dd28-122">-Skip</span></span>
<span data-ttu-id="6dd28-123">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="6dd28-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6dd28-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="6dd28-124">-Top</span></span>
<span data-ttu-id="6dd28-125">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="6dd28-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6dd28-126">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="6dd28-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6dd28-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd28-127">CommonParameters</span></span>
<span data-ttu-id="6dd28-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd28-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd28-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd28-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd28-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dd28-130">INPUTS</span></span>

## <span data-ttu-id="6dd28-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6dd28-131">OUTPUTS</span></span>

### <span data-ttu-id="6dd28-132">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="6dd28-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="6dd28-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6dd28-133">NOTES</span></span>

## <span data-ttu-id="6dd28-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6dd28-134">RELATED LINKS</span></span>
