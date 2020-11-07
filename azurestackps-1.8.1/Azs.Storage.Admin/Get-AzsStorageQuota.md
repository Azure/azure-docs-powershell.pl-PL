---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 687838573459c09ceaf08c0d1c3335caa4a99769
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889753"
---
# <span data-ttu-id="53e33-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="53e33-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="53e33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53e33-102">SYNOPSIS</span></span>
<span data-ttu-id="53e33-103">Zwraca listę przydziałów magazynowania w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="53e33-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="53e33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53e33-104">SYNTAX</span></span>

### <span data-ttu-id="53e33-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="53e33-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="53e33-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="53e33-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="53e33-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="53e33-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="53e33-108">Opis</span><span class="sxs-lookup"><span data-stu-id="53e33-108">DESCRIPTION</span></span>
<span data-ttu-id="53e33-109">Zwraca listę przydziałów magazynowania w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="53e33-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="53e33-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53e33-110">EXAMPLES</span></span>

### <span data-ttu-id="53e33-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="53e33-111">EXAMPLE 1</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="53e33-112">Uzyskaj listę przydziałów magazynowania.</span><span class="sxs-lookup"><span data-stu-id="53e33-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="53e33-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="53e33-113">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="53e33-114">Uzyskaj szczegółowe informacje o określonym przydziale magazynowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="53e33-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="53e33-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53e33-115">PARAMETERS</span></span>

### <span data-ttu-id="53e33-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53e33-116">-Name</span></span>
<span data-ttu-id="53e33-117">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="53e33-117">The name of the storage quota.</span></span>

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

### <span data-ttu-id="53e33-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="53e33-118">-Location</span></span>
<span data-ttu-id="53e33-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="53e33-119">Resource location.</span></span>

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

### <span data-ttu-id="53e33-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53e33-120">-ResourceId</span></span>
<span data-ttu-id="53e33-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="53e33-121">The resource id.</span></span>

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

### <span data-ttu-id="53e33-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="53e33-122">-Skip</span></span>
<span data-ttu-id="53e33-123">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="53e33-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="53e33-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="53e33-124">-Top</span></span>
<span data-ttu-id="53e33-125">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="53e33-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="53e33-126">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="53e33-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="53e33-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e33-127">CommonParameters</span></span>
<span data-ttu-id="53e33-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53e33-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e33-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53e33-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e33-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53e33-130">INPUTS</span></span>

## <span data-ttu-id="53e33-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53e33-131">OUTPUTS</span></span>

### <span data-ttu-id="53e33-132">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="53e33-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="53e33-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53e33-133">NOTES</span></span>

## <span data-ttu-id="53e33-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53e33-134">RELATED LINKS</span></span>
