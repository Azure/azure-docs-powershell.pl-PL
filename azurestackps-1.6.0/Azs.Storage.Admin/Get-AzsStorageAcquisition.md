---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523522"
---
# <span data-ttu-id="fade6-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="fade6-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="fade6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fade6-102">SYNOPSIS</span></span>
<span data-ttu-id="fade6-103">Zwraca listę obiektów BLOB acquistions.</span><span class="sxs-lookup"><span data-stu-id="fade6-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="fade6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fade6-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fade6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fade6-105">DESCRIPTION</span></span>
<span data-ttu-id="fade6-106">Zwraca listę obiektów BLOB acquistions.</span><span class="sxs-lookup"><span data-stu-id="fade6-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="fade6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fade6-107">EXAMPLES</span></span>

### <span data-ttu-id="fade6-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fade6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="fade6-109">Pobierz listę obiektów BLOB acquistions.</span><span class="sxs-lookup"><span data-stu-id="fade6-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="fade6-110">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="fade6-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="fade6-111">Pobierz listę obiektów BLOB acquistions.</span><span class="sxs-lookup"><span data-stu-id="fade6-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="fade6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fade6-112">PARAMETERS</span></span>

### <span data-ttu-id="fade6-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="fade6-113">-FarmName</span></span>
<span data-ttu-id="fade6-114">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="fade6-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fade6-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="fade6-115">-Filter</span></span>
<span data-ttu-id="fade6-116">Ciąg filtru</span><span class="sxs-lookup"><span data-stu-id="fade6-116">Filter string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fade6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fade6-117">-ResourceGroupName</span></span>
<span data-ttu-id="fade6-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fade6-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fade6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fade6-119">CommonParameters</span></span>
<span data-ttu-id="fade6-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fade6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fade6-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fade6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fade6-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fade6-122">INPUTS</span></span>

## <span data-ttu-id="fade6-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fade6-123">OUTPUTS</span></span>

## <span data-ttu-id="fade6-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fade6-124">NOTES</span></span>

## <span data-ttu-id="fade6-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fade6-125">RELATED LINKS</span></span>
