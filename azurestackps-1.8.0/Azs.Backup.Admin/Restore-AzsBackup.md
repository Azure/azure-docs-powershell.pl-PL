---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 573a47b3684020817130e1d41c764abef717de0a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889329"
---
# <span data-ttu-id="4b43b-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="4b43b-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="4b43b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b43b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b43b-103">Przywracanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4b43b-103">Restore a backup.</span></span>

## <span data-ttu-id="4b43b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b43b-104">SYNTAX</span></span>

### <span data-ttu-id="4b43b-105">Backups_Restore (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4b43b-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b43b-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="4b43b-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b43b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4b43b-107">DESCRIPTION</span></span>
<span data-ttu-id="4b43b-108">Przywracanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4b43b-108">Restore a backup.</span></span>

## <span data-ttu-id="4b43b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b43b-109">EXAMPLES</span></span>

### <span data-ttu-id="4b43b-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4b43b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="4b43b-111">Przywracanie z kopii zapasowej stosu Azure.</span><span class="sxs-lookup"><span data-stu-id="4b43b-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="4b43b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b43b-112">PARAMETERS</span></span>

### <span data-ttu-id="4b43b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b43b-113">-AsJob</span></span>
<span data-ttu-id="4b43b-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="4b43b-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4b43b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4b43b-115">-Force</span></span>
<span data-ttu-id="4b43b-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4b43b-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4b43b-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4b43b-117">-Location</span></span>
<span data-ttu-id="4b43b-118">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4b43b-118">Name of location to backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b43b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4b43b-119">-Name</span></span>
<span data-ttu-id="4b43b-120">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4b43b-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b43b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b43b-121">-ResourceGroupName</span></span>
<span data-ttu-id="4b43b-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4b43b-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b43b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b43b-123">-ResourceId</span></span>
<span data-ttu-id="4b43b-124">{{Opis ResourceId (wypełnienie)}}</span><span class="sxs-lookup"><span data-stu-id="4b43b-124">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="4b43b-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4b43b-125">-Confirm</span></span>
<span data-ttu-id="4b43b-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b43b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b43b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b43b-127">-WhatIf</span></span>
<span data-ttu-id="4b43b-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b43b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b43b-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4b43b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b43b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b43b-130">CommonParameters</span></span>
<span data-ttu-id="4b43b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b43b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b43b-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b43b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b43b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b43b-133">INPUTS</span></span>

## <span data-ttu-id="4b43b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b43b-134">OUTPUTS</span></span>

## <span data-ttu-id="4b43b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b43b-135">NOTES</span></span>

## <span data-ttu-id="4b43b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b43b-136">RELATED LINKS</span></span>

