---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bf583c30d2faff1055debf366a84a0739789467
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889969"
---
# <span data-ttu-id="5b488-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="5b488-101">Start-AzsBackup</span></span>

## <span data-ttu-id="5b488-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b488-102">SYNOPSIS</span></span>
<span data-ttu-id="5b488-103">Wykonaj kopię zapasową określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="5b488-103">Back up a specific location.</span></span>

## <span data-ttu-id="5b488-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b488-104">SYNTAX</span></span>

### <span data-ttu-id="5b488-105">Utwórz kopię zapasową (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5b488-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b488-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="5b488-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b488-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5b488-107">DESCRIPTION</span></span>
<span data-ttu-id="5b488-108">Wykonaj kopię zapasową określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="5b488-108">Back up a specific location.</span></span>

## <span data-ttu-id="5b488-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b488-109">EXAMPLES</span></span>

### <span data-ttu-id="5b488-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5b488-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="5b488-111">Rozpocznij tworzenie kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5b488-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="5b488-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b488-112">PARAMETERS</span></span>

### <span data-ttu-id="5b488-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b488-113">-AsJob</span></span>
<span data-ttu-id="5b488-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="5b488-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5b488-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5b488-115">-Force</span></span>
<span data-ttu-id="5b488-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5b488-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5b488-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5b488-117">-Location</span></span>
<span data-ttu-id="5b488-118">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="5b488-118">Name of the backup location.</span></span>

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

### <span data-ttu-id="5b488-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b488-119">-ResourceGroupName</span></span>
<span data-ttu-id="5b488-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5b488-120">Name of the resource group.</span></span>

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

### <span data-ttu-id="5b488-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b488-121">-ResourceId</span></span>
<span data-ttu-id="5b488-122">{{Opis ResourceId (wypełnienie)}}</span><span class="sxs-lookup"><span data-stu-id="5b488-122">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="5b488-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b488-123">-Confirm</span></span>
<span data-ttu-id="5b488-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b488-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b488-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b488-125">-WhatIf</span></span>
<span data-ttu-id="5b488-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b488-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b488-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5b488-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b488-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b488-128">CommonParameters</span></span>
<span data-ttu-id="5b488-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b488-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b488-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b488-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b488-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b488-131">INPUTS</span></span>

## <span data-ttu-id="5b488-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b488-132">OUTPUTS</span></span>

### <span data-ttu-id="5b488-133">Microsoft. AzureStack. Management. Backup. admin. models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="5b488-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="5b488-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b488-134">NOTES</span></span>

## <span data-ttu-id="5b488-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b488-135">RELATED LINKS</span></span>

