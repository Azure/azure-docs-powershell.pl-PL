---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4847310f65a0b652d15321cd49583212ef5844d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523154"
---
# <span data-ttu-id="fafc9-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fafc9-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="fafc9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fafc9-102">SYNOPSIS</span></span>
<span data-ttu-id="fafc9-103">Zwraca listę kontenerów, które można migrować w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="fafc9-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="fafc9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fafc9-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fafc9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fafc9-105">DESCRIPTION</span></span>
<span data-ttu-id="fafc9-106">Zwraca listę kontenerów, które można migrować w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="fafc9-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="fafc9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fafc9-107">EXAMPLES</span></span>

### <span data-ttu-id="fafc9-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fafc9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="fafc9-109">Zapoznaj się z listą kontenerów, które można migrować w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="fafc9-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="fafc9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fafc9-110">PARAMETERS</span></span>

### <span data-ttu-id="fafc9-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="fafc9-111">-FarmName</span></span>
<span data-ttu-id="fafc9-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="fafc9-112">Farm Id.</span></span>

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

### <span data-ttu-id="fafc9-113">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fafc9-113">-MaxCount</span></span>
<span data-ttu-id="fafc9-114">Maksymalna liczba kontenerów.</span><span class="sxs-lookup"><span data-stu-id="fafc9-114">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fafc9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fafc9-115">-ResourceGroupName</span></span>
<span data-ttu-id="fafc9-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fafc9-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fafc9-117">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="fafc9-117">-ShareName</span></span>
<span data-ttu-id="fafc9-118">Nazwa udziału przechowująca kontenery magazynu.</span><span class="sxs-lookup"><span data-stu-id="fafc9-118">Share name which holds the storage containers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fafc9-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="fafc9-119">-StartIndex</span></span>
<span data-ttu-id="fafc9-120">Indeks początkowy kontenera get.</span><span class="sxs-lookup"><span data-stu-id="fafc9-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fafc9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fafc9-121">CommonParameters</span></span>
<span data-ttu-id="fafc9-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fafc9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fafc9-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fafc9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fafc9-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fafc9-124">INPUTS</span></span>

## <span data-ttu-id="fafc9-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fafc9-125">OUTPUTS</span></span>

## <span data-ttu-id="fafc9-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fafc9-126">NOTES</span></span>

## <span data-ttu-id="fafc9-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fafc9-127">RELATED LINKS</span></span>

