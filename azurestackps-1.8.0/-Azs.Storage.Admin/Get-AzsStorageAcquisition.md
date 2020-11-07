---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889386"
---
# <span data-ttu-id="7b8f0-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="7b8f0-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="7b8f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8f0-103">Zwraca listę obiektów BLOB acquistions.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="7b8f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b8f0-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b8f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b8f0-105">DESCRIPTION</span></span>
<span data-ttu-id="7b8f0-106">Zwraca listę obiektów BLOB acquistions.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="7b8f0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b8f0-107">EXAMPLES</span></span>

### <span data-ttu-id="7b8f0-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7b8f0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="7b8f0-109">Pobierz listę obiektów BLOB acquistions.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="7b8f0-110">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7b8f0-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="7b8f0-111">Pobierz listę obiektów BLOB acquistions.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="7b8f0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b8f0-112">PARAMETERS</span></span>

### <span data-ttu-id="7b8f0-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="7b8f0-113">-FarmName</span></span>
<span data-ttu-id="7b8f0-114">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-114">Farm Id.</span></span>

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

### <span data-ttu-id="7b8f0-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="7b8f0-115">-Filter</span></span>
<span data-ttu-id="7b8f0-116">Ciąg filtru</span><span class="sxs-lookup"><span data-stu-id="7b8f0-116">Filter string</span></span>

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

### <span data-ttu-id="7b8f0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b8f0-117">-ResourceGroupName</span></span>
<span data-ttu-id="7b8f0-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-118">Resource group name.</span></span>

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

### <span data-ttu-id="7b8f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8f0-119">CommonParameters</span></span>
<span data-ttu-id="7b8f0-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8f0-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b8f0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8f0-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b8f0-122">INPUTS</span></span>

## <span data-ttu-id="7b8f0-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b8f0-123">OUTPUTS</span></span>

## <span data-ttu-id="7b8f0-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b8f0-124">NOTES</span></span>

## <span data-ttu-id="7b8f0-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b8f0-125">RELATED LINKS</span></span>

