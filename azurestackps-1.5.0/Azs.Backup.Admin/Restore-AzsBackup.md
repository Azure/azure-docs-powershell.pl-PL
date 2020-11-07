---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 385947ead1039103933cb7e752dc5dee768b388a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523730"
---
# <span data-ttu-id="fa68a-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="fa68a-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="fa68a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa68a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa68a-103">Przywracanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fa68a-103">Restore a backup.</span></span>

## <span data-ttu-id="fa68a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa68a-104">SYNTAX</span></span>

### <span data-ttu-id="fa68a-105">Backups_Restore (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="fa68a-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa68a-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="fa68a-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa68a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fa68a-107">DESCRIPTION</span></span>
<span data-ttu-id="fa68a-108">Przywracanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fa68a-108">Restore a backup.</span></span>

## <span data-ttu-id="fa68a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa68a-109">EXAMPLES</span></span>

### <span data-ttu-id="fa68a-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fa68a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="fa68a-111">Przywracanie z kopii zapasowej stosu Azure.</span><span class="sxs-lookup"><span data-stu-id="fa68a-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="fa68a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa68a-112">PARAMETERS</span></span>

### <span data-ttu-id="fa68a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa68a-113">-AsJob</span></span>
<span data-ttu-id="fa68a-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="fa68a-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="fa68a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fa68a-115">-Force</span></span>
<span data-ttu-id="fa68a-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fa68a-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fa68a-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fa68a-117">-Location</span></span>
<span data-ttu-id="fa68a-118">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fa68a-118">Name of location to backup.</span></span>

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

### <span data-ttu-id="fa68a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa68a-119">-Name</span></span>
<span data-ttu-id="fa68a-120">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fa68a-120">Name of the backup.</span></span>

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

### <span data-ttu-id="fa68a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa68a-121">-ResourceGroupName</span></span>
<span data-ttu-id="fa68a-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa68a-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="fa68a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa68a-123">-ResourceId</span></span>
<span data-ttu-id="fa68a-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="fa68a-124">The resource id.</span></span>

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

### <span data-ttu-id="fa68a-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa68a-125">-Confirm</span></span>
<span data-ttu-id="fa68a-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa68a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa68a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa68a-127">-WhatIf</span></span>
<span data-ttu-id="fa68a-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa68a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa68a-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa68a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa68a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa68a-130">CommonParameters</span></span>
<span data-ttu-id="fa68a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa68a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa68a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa68a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa68a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa68a-133">INPUTS</span></span>

## <span data-ttu-id="fa68a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa68a-134">OUTPUTS</span></span>

## <span data-ttu-id="fa68a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa68a-135">NOTES</span></span>

## <span data-ttu-id="fa68a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa68a-136">RELATED LINKS</span></span>
