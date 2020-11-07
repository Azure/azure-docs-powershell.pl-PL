---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889653"
---
# <span data-ttu-id="03031-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="03031-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="03031-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03031-102">SYNOPSIS</span></span>
<span data-ttu-id="03031-103">Zwraca listę wszystkich udziałów plików w sieci szkieletowej w określonym miejscu.</span><span class="sxs-lookup"><span data-stu-id="03031-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="03031-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03031-104">SYNTAX</span></span>

### <span data-ttu-id="03031-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="03031-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="03031-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="03031-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="03031-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="03031-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="03031-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03031-108">DESCRIPTION</span></span>
<span data-ttu-id="03031-109">Zwraca listę wszystkich udziałów plików w sieci szkieletowej w określonym miejscu.</span><span class="sxs-lookup"><span data-stu-id="03031-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="03031-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03031-110">EXAMPLES</span></span>

### <span data-ttu-id="03031-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="03031-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="03031-112">Zwraca listę wszystkich udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="03031-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="03031-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="03031-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="03031-114">Zwraca udział pliku na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="03031-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="03031-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03031-115">PARAMETERS</span></span>

### <span data-ttu-id="03031-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03031-116">-Name</span></span>
<span data-ttu-id="03031-117">Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="03031-117">Fabric file share name.</span></span>

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

### <span data-ttu-id="03031-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="03031-118">-Location</span></span>
<span data-ttu-id="03031-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="03031-119">Location of the resource.</span></span>

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

### <span data-ttu-id="03031-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03031-120">-ResourceGroupName</span></span>
<span data-ttu-id="03031-121">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="03031-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="03031-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03031-122">-ResourceId</span></span>
<span data-ttu-id="03031-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="03031-123">The resource id.</span></span>

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

### <span data-ttu-id="03031-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="03031-124">-Filter</span></span>
<span data-ttu-id="03031-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="03031-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03031-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03031-126">CommonParameters</span></span>
<span data-ttu-id="03031-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03031-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03031-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03031-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03031-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03031-129">INPUTS</span></span>

## <span data-ttu-id="03031-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03031-130">OUTPUTS</span></span>

### <span data-ttu-id="03031-131">Microsoft. AzureStack. Management. Fabric. admin. models.</span><span class="sxs-lookup"><span data-stu-id="03031-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="03031-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03031-132">NOTES</span></span>

## <span data-ttu-id="03031-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03031-133">RELATED LINKS</span></span>
