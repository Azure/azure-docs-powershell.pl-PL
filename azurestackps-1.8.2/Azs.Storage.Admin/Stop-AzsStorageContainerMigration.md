---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055569"
---
# <span data-ttu-id="6206f-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="6206f-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="6206f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6206f-102">SYNOPSIS</span></span>
<span data-ttu-id="6206f-103">Anulowanie zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="6206f-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="6206f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6206f-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6206f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6206f-105">DESCRIPTION</span></span>
<span data-ttu-id="6206f-106">Anulowanie zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="6206f-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="6206f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6206f-107">EXAMPLES</span></span>

### <span data-ttu-id="6206f-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="6206f-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="6206f-109">Anuluj migrację kontenera.</span><span class="sxs-lookup"><span data-stu-id="6206f-109">Cancel container migration.</span></span>

## <span data-ttu-id="6206f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6206f-110">PARAMETERS</span></span>

### <span data-ttu-id="6206f-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="6206f-111">-JobId</span></span>
<span data-ttu-id="6206f-112">Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="6206f-112">Operation Id.</span></span>

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

### <span data-ttu-id="6206f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6206f-113">-ResourceGroupName</span></span>
<span data-ttu-id="6206f-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6206f-114">Resource group name.</span></span>

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

### <span data-ttu-id="6206f-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="6206f-115">-FarmName</span></span>
<span data-ttu-id="6206f-116">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="6206f-116">Farm Id.</span></span>

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

### <span data-ttu-id="6206f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6206f-117">-AsJob</span></span>
<span data-ttu-id="6206f-118">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="6206f-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6206f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6206f-119">-Force</span></span>
<span data-ttu-id="6206f-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6206f-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6206f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6206f-121">-WhatIf</span></span>
<span data-ttu-id="6206f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6206f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6206f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6206f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6206f-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6206f-124">-Confirm</span></span>
<span data-ttu-id="6206f-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6206f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6206f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6206f-126">CommonParameters</span></span>
<span data-ttu-id="6206f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6206f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6206f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6206f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6206f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6206f-129">INPUTS</span></span>

## <span data-ttu-id="6206f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6206f-130">OUTPUTS</span></span>

## <span data-ttu-id="6206f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6206f-131">NOTES</span></span>

## <span data-ttu-id="6206f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6206f-132">RELATED LINKS</span></span>
