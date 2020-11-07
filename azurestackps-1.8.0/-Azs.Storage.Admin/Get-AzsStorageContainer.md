---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4847310f65a0b652d15321cd49583212ef5844d8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889382"
---
# <span data-ttu-id="c8a33-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c8a33-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="c8a33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8a33-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a33-103">Zwraca listę kontenerów, które można migrować w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="c8a33-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="c8a33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8a33-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c8a33-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8a33-105">DESCRIPTION</span></span>
<span data-ttu-id="c8a33-106">Zwraca listę kontenerów, które można migrować w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="c8a33-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="c8a33-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8a33-107">EXAMPLES</span></span>

### <span data-ttu-id="c8a33-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c8a33-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="c8a33-109">Zapoznaj się z listą kontenerów, które można migrować w określonym udziale.</span><span class="sxs-lookup"><span data-stu-id="c8a33-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="c8a33-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8a33-110">PARAMETERS</span></span>

### <span data-ttu-id="c8a33-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="c8a33-111">-FarmName</span></span>
<span data-ttu-id="c8a33-112">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="c8a33-112">Farm Id.</span></span>

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

### <span data-ttu-id="c8a33-113">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c8a33-113">-MaxCount</span></span>
<span data-ttu-id="c8a33-114">Maksymalna liczba kontenerów.</span><span class="sxs-lookup"><span data-stu-id="c8a33-114">The max count of containers.</span></span>

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

### <span data-ttu-id="c8a33-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a33-115">-ResourceGroupName</span></span>
<span data-ttu-id="c8a33-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8a33-116">Resource group name.</span></span>

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

### <span data-ttu-id="c8a33-117">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="c8a33-117">-ShareName</span></span>
<span data-ttu-id="c8a33-118">Nazwa udziału przechowująca kontenery magazynu.</span><span class="sxs-lookup"><span data-stu-id="c8a33-118">Share name which holds the storage containers.</span></span>

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

### <span data-ttu-id="c8a33-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="c8a33-119">-StartIndex</span></span>
<span data-ttu-id="c8a33-120">Indeks początkowy kontenera get.</span><span class="sxs-lookup"><span data-stu-id="c8a33-120">The start index of get containers.</span></span>

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

### <span data-ttu-id="c8a33-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a33-121">CommonParameters</span></span>
<span data-ttu-id="c8a33-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a33-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a33-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8a33-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a33-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8a33-124">INPUTS</span></span>

## <span data-ttu-id="c8a33-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8a33-125">OUTPUTS</span></span>

## <span data-ttu-id="c8a33-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8a33-126">NOTES</span></span>

## <span data-ttu-id="c8a33-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8a33-127">RELATED LINKS</span></span>

