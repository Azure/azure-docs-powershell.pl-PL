---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522945"
---
# <span data-ttu-id="d2857-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="d2857-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="d2857-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2857-102">SYNOPSIS</span></span>
<span data-ttu-id="d2857-103">Anulowanie zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="d2857-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="d2857-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2857-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2857-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2857-105">DESCRIPTION</span></span>
<span data-ttu-id="d2857-106">Anulowanie zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="d2857-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="d2857-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2857-107">EXAMPLES</span></span>

### <span data-ttu-id="d2857-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d2857-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="d2857-109">Anuluj migrację kontenera.</span><span class="sxs-lookup"><span data-stu-id="d2857-109">Cancel container migration.</span></span>

## <span data-ttu-id="d2857-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2857-110">PARAMETERS</span></span>

### <span data-ttu-id="d2857-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2857-111">-AsJob</span></span>
<span data-ttu-id="d2857-112">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="d2857-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2857-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="d2857-113">-FarmName</span></span>
<span data-ttu-id="d2857-114">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="d2857-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2857-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d2857-115">-Force</span></span>
<span data-ttu-id="d2857-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2857-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2857-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="d2857-117">-JobId</span></span>
<span data-ttu-id="d2857-118">Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="d2857-118">Operation Id.</span></span>

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

### <span data-ttu-id="d2857-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2857-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2857-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2857-120">Resource group name.</span></span>

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

### <span data-ttu-id="d2857-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2857-121">-Confirm</span></span>
<span data-ttu-id="d2857-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2857-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2857-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2857-123">-WhatIf</span></span>
<span data-ttu-id="d2857-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2857-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2857-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d2857-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2857-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2857-126">CommonParameters</span></span>
<span data-ttu-id="d2857-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2857-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2857-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2857-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2857-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2857-129">INPUTS</span></span>

## <span data-ttu-id="d2857-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2857-130">OUTPUTS</span></span>

## <span data-ttu-id="d2857-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2857-131">NOTES</span></span>

## <span data-ttu-id="d2857-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2857-132">RELATED LINKS</span></span>

