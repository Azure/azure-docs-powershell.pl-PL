---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889493"
---
# <span data-ttu-id="84c60-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="84c60-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="84c60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84c60-102">SYNOPSIS</span></span>
<span data-ttu-id="84c60-103">Anulowanie zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="84c60-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="84c60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84c60-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84c60-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84c60-105">DESCRIPTION</span></span>
<span data-ttu-id="84c60-106">Anulowanie zadania migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="84c60-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="84c60-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84c60-107">EXAMPLES</span></span>

### <span data-ttu-id="84c60-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="84c60-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="84c60-109">Anuluj migrację kontenera.</span><span class="sxs-lookup"><span data-stu-id="84c60-109">Cancel container migration.</span></span>

## <span data-ttu-id="84c60-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84c60-110">PARAMETERS</span></span>

### <span data-ttu-id="84c60-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="84c60-111">-JobId</span></span>
<span data-ttu-id="84c60-112">Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="84c60-112">Operation Id.</span></span>

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

### <span data-ttu-id="84c60-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84c60-113">-ResourceGroupName</span></span>
<span data-ttu-id="84c60-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84c60-114">Resource group name.</span></span>

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

### <span data-ttu-id="84c60-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="84c60-115">-FarmName</span></span>
<span data-ttu-id="84c60-116">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="84c60-116">Farm Id.</span></span>

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

### <span data-ttu-id="84c60-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84c60-117">-AsJob</span></span>
<span data-ttu-id="84c60-118">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="84c60-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="84c60-119">-Force</span><span class="sxs-lookup"><span data-stu-id="84c60-119">-Force</span></span>
<span data-ttu-id="84c60-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="84c60-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="84c60-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c60-121">-WhatIf</span></span>
<span data-ttu-id="84c60-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84c60-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c60-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84c60-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c60-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84c60-124">-Confirm</span></span>
<span data-ttu-id="84c60-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84c60-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c60-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c60-126">CommonParameters</span></span>
<span data-ttu-id="84c60-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84c60-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c60-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84c60-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c60-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84c60-129">INPUTS</span></span>

## <span data-ttu-id="84c60-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84c60-130">OUTPUTS</span></span>

## <span data-ttu-id="84c60-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84c60-131">NOTES</span></span>

## <span data-ttu-id="84c60-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84c60-132">RELATED LINKS</span></span>
