---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055816"
---
# <span data-ttu-id="f93c9-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="f93c9-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="f93c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f93c9-102">SYNOPSIS</span></span>
<span data-ttu-id="f93c9-103">Dzierżawa katalogu.</span><span class="sxs-lookup"><span data-stu-id="f93c9-103">Directory tenant.</span></span>

## <span data-ttu-id="f93c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f93c9-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="f93c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f93c9-105">DESCRIPTION</span></span>
<span data-ttu-id="f93c9-106">Dzierżawa katalogu.</span><span class="sxs-lookup"><span data-stu-id="f93c9-106">Directory tenant.</span></span>

## <span data-ttu-id="f93c9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f93c9-107">EXAMPLES</span></span>

### <span data-ttu-id="f93c9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f93c9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f93c9-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="f93c9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f93c9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f93c9-110">PARAMETERS</span></span>

### <span data-ttu-id="f93c9-111">-ID</span><span class="sxs-lookup"><span data-stu-id="f93c9-111">-Id</span></span>
<span data-ttu-id="f93c9-112">Identyfikator URI zasobu.</span><span class="sxs-lookup"><span data-stu-id="f93c9-112">URI of the resource.</span></span>

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

### <span data-ttu-id="f93c9-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f93c9-113">-Location</span></span>
<span data-ttu-id="f93c9-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f93c9-114">Location of the resource.</span></span>

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

### <span data-ttu-id="f93c9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f93c9-115">-Name</span></span>
<span data-ttu-id="f93c9-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f93c9-116">Name of the resource.</span></span>

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

### <span data-ttu-id="f93c9-117">-Tagi</span><span class="sxs-lookup"><span data-stu-id="f93c9-117">-Tags</span></span>
<span data-ttu-id="f93c9-118">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="f93c9-118">List of key-value pairs.</span></span>

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

### <span data-ttu-id="f93c9-119">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="f93c9-119">-TenantId</span></span>
<span data-ttu-id="f93c9-120">Unikatowy identyfikator dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="f93c9-120">Tenant unique identifier.</span></span>

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

### <span data-ttu-id="f93c9-121">-Type</span><span class="sxs-lookup"><span data-stu-id="f93c9-121">-Type</span></span>
<span data-ttu-id="f93c9-122">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="f93c9-122">Type of resource.</span></span>

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

### <span data-ttu-id="f93c9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93c9-123">CommonParameters</span></span>
<span data-ttu-id="f93c9-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f93c9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93c9-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f93c9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93c9-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f93c9-126">INPUTS</span></span>

## <span data-ttu-id="f93c9-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f93c9-127">OUTPUTS</span></span>

## <span data-ttu-id="f93c9-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f93c9-128">NOTES</span></span>

## <span data-ttu-id="f93c9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f93c9-129">RELATED LINKS</span></span>

