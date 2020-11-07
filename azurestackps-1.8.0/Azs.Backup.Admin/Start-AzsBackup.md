---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bf583c30d2faff1055debf366a84a0739789467
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888873"
---
# <span data-ttu-id="811ed-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="811ed-101">Start-AzsBackup</span></span>

## <span data-ttu-id="811ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="811ed-102">SYNOPSIS</span></span>
<span data-ttu-id="811ed-103">Wykonaj kopię zapasową określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="811ed-103">Back up a specific location.</span></span>

## <span data-ttu-id="811ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="811ed-104">SYNTAX</span></span>

### <span data-ttu-id="811ed-105">Utwórz kopię zapasową (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="811ed-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="811ed-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="811ed-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="811ed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="811ed-107">DESCRIPTION</span></span>
<span data-ttu-id="811ed-108">Wykonaj kopię zapasową określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="811ed-108">Back up a specific location.</span></span>

## <span data-ttu-id="811ed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="811ed-109">EXAMPLES</span></span>

### <span data-ttu-id="811ed-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="811ed-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="811ed-111">Rozpocznij tworzenie kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="811ed-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="811ed-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="811ed-112">PARAMETERS</span></span>

### <span data-ttu-id="811ed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="811ed-113">-AsJob</span></span>
<span data-ttu-id="811ed-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="811ed-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="811ed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="811ed-115">-Force</span></span>
<span data-ttu-id="811ed-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="811ed-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="811ed-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="811ed-117">-Location</span></span>
<span data-ttu-id="811ed-118">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="811ed-118">Name of the backup location.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="811ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="811ed-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="811ed-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811ed-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="811ed-121">-ResourceId</span></span>
<span data-ttu-id="811ed-122">{{Opis ResourceId (wypełnienie)}}</span><span class="sxs-lookup"><span data-stu-id="811ed-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="811ed-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="811ed-123">-Confirm</span></span>
<span data-ttu-id="811ed-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="811ed-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="811ed-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="811ed-125">-WhatIf</span></span>
<span data-ttu-id="811ed-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="811ed-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="811ed-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="811ed-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="811ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="811ed-128">CommonParameters</span></span>
<span data-ttu-id="811ed-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="811ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="811ed-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="811ed-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="811ed-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="811ed-131">INPUTS</span></span>

## <span data-ttu-id="811ed-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="811ed-132">OUTPUTS</span></span>

### <span data-ttu-id="811ed-133">Microsoft. AzureStack. Management. Backup. admin. models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="811ed-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="811ed-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="811ed-134">NOTES</span></span>

## <span data-ttu-id="811ed-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="811ed-135">RELATED LINKS</span></span>

