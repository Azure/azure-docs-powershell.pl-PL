---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889525"
---
# <span data-ttu-id="b8e84-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="b8e84-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="b8e84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8e84-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e84-103">Dzierżawa katalogu.</span><span class="sxs-lookup"><span data-stu-id="b8e84-103">Directory tenant.</span></span>

## <span data-ttu-id="b8e84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8e84-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b8e84-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8e84-105">DESCRIPTION</span></span>
<span data-ttu-id="b8e84-106">Dzierżawa katalogu.</span><span class="sxs-lookup"><span data-stu-id="b8e84-106">Directory tenant.</span></span>

## <span data-ttu-id="b8e84-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8e84-107">EXAMPLES</span></span>

### <span data-ttu-id="b8e84-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8e84-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b8e84-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="b8e84-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b8e84-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8e84-110">PARAMETERS</span></span>

### <span data-ttu-id="b8e84-111">-ID</span><span class="sxs-lookup"><span data-stu-id="b8e84-111">-Id</span></span>
<span data-ttu-id="b8e84-112">Identyfikator URI zasobu.</span><span class="sxs-lookup"><span data-stu-id="b8e84-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e84-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b8e84-113">-Location</span></span>
<span data-ttu-id="b8e84-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b8e84-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e84-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8e84-115">-Name</span></span>
<span data-ttu-id="b8e84-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b8e84-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e84-117">-Tagi</span><span class="sxs-lookup"><span data-stu-id="b8e84-117">-Tags</span></span>
<span data-ttu-id="b8e84-118">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="b8e84-118">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e84-119">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="b8e84-119">-TenantId</span></span>
<span data-ttu-id="b8e84-120">Unikatowy identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b8e84-120">Tenant unique identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e84-121">-Type</span><span class="sxs-lookup"><span data-stu-id="b8e84-121">-Type</span></span>
<span data-ttu-id="b8e84-122">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="b8e84-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e84-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e84-123">CommonParameters</span></span>
<span data-ttu-id="b8e84-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8e84-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e84-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8e84-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e84-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8e84-126">INPUTS</span></span>

## <span data-ttu-id="b8e84-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8e84-127">OUTPUTS</span></span>

## <span data-ttu-id="b8e84-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8e84-128">NOTES</span></span>

## <span data-ttu-id="b8e84-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8e84-129">RELATED LINKS</span></span>

