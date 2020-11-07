---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 30a1bc70b4e704d8dadf864dedf7173476909cf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888737"
---
# <span data-ttu-id="aa83c-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="aa83c-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="aa83c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa83c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa83c-103">Zwraca przydziały określające limity przydziałów dla obiektów obliczeniowych.</span><span class="sxs-lookup"><span data-stu-id="aa83c-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="aa83c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa83c-104">SYNTAX</span></span>

### <span data-ttu-id="aa83c-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="aa83c-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa83c-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="aa83c-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa83c-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="aa83c-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="aa83c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aa83c-108">DESCRIPTION</span></span>
<span data-ttu-id="aa83c-109">Zapoznaj się z listą istniejących przydziałów.</span><span class="sxs-lookup"><span data-stu-id="aa83c-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="aa83c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa83c-110">EXAMPLES</span></span>

### <span data-ttu-id="aa83c-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa83c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="aa83c-112">Pobieranie wszystkich przydziałów obliczeń w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="aa83c-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="aa83c-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa83c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="aa83c-114">Uzyskiwanie określonego przydziału obliczeń.</span><span class="sxs-lookup"><span data-stu-id="aa83c-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="aa83c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa83c-115">PARAMETERS</span></span>

### <span data-ttu-id="aa83c-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="aa83c-116">-Location</span></span>
<span data-ttu-id="aa83c-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="aa83c-117">Location of the resource.</span></span>

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

### <span data-ttu-id="aa83c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa83c-118">-Name</span></span>
<span data-ttu-id="aa83c-119">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="aa83c-119">Name of the quota.</span></span>

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

### <span data-ttu-id="aa83c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa83c-120">-ResourceId</span></span>
<span data-ttu-id="aa83c-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="aa83c-121">The resource id.</span></span>

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

### <span data-ttu-id="aa83c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa83c-122">CommonParameters</span></span>
<span data-ttu-id="aa83c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa83c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa83c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa83c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa83c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa83c-125">INPUTS</span></span>

## <span data-ttu-id="aa83c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa83c-126">OUTPUTS</span></span>

### <span data-ttu-id="aa83c-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="aa83c-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="aa83c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa83c-128">NOTES</span></span>

## <span data-ttu-id="aa83c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa83c-129">RELATED LINKS</span></span>

