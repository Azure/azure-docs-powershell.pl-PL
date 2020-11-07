---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86b9e7574344e1b4724648ce55fa2e36aed6591b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888666"
---
# <span data-ttu-id="37c86-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="37c86-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="37c86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37c86-102">SYNOPSIS</span></span>
<span data-ttu-id="37c86-103">Zwraca listę wszystkich udziałów plików w sieci szkieletowej w określonym miejscu.</span><span class="sxs-lookup"><span data-stu-id="37c86-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="37c86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37c86-104">SYNTAX</span></span>

### <span data-ttu-id="37c86-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="37c86-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="37c86-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="37c86-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="37c86-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="37c86-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="37c86-108">Opis</span><span class="sxs-lookup"><span data-stu-id="37c86-108">DESCRIPTION</span></span>
<span data-ttu-id="37c86-109">Zwraca listę wszystkich udziałów plików w sieci szkieletowej w określonym miejscu.</span><span class="sxs-lookup"><span data-stu-id="37c86-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="37c86-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37c86-110">EXAMPLES</span></span>

### <span data-ttu-id="37c86-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="37c86-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="37c86-112">Zwraca listę wszystkich udziałów plików.</span><span class="sxs-lookup"><span data-stu-id="37c86-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="37c86-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="37c86-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="37c86-114">Zwraca udział pliku na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="37c86-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="37c86-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37c86-115">PARAMETERS</span></span>

### <span data-ttu-id="37c86-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="37c86-116">-Filter</span></span>
<span data-ttu-id="37c86-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="37c86-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="37c86-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="37c86-118">-Location</span></span>
<span data-ttu-id="37c86-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="37c86-119">Location of the resource.</span></span>

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

### <span data-ttu-id="37c86-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37c86-120">-Name</span></span>
<span data-ttu-id="37c86-121">Nazwa udziału plików w sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="37c86-121">Fabric file share name.</span></span>

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

### <span data-ttu-id="37c86-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c86-122">-ResourceGroupName</span></span>
<span data-ttu-id="37c86-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="37c86-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="37c86-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37c86-124">-ResourceId</span></span>
<span data-ttu-id="37c86-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="37c86-125">The resource id.</span></span>

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

### <span data-ttu-id="37c86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c86-126">CommonParameters</span></span>
<span data-ttu-id="37c86-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c86-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c86-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c86-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37c86-129">INPUTS</span></span>

## <span data-ttu-id="37c86-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37c86-130">OUTPUTS</span></span>

### <span data-ttu-id="37c86-131">Microsoft. AzureStack. Management. Fabric. admin. models.</span><span class="sxs-lookup"><span data-stu-id="37c86-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="37c86-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37c86-132">NOTES</span></span>

## <span data-ttu-id="37c86-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37c86-133">RELATED LINKS</span></span>

