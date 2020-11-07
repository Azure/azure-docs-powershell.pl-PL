---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7dff6c2d9c191d852420ab2c2017a0b9d1cf8d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523925"
---
# <span data-ttu-id="f242b-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="f242b-101">Start-AzsBackup</span></span>

## <span data-ttu-id="f242b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f242b-102">SYNOPSIS</span></span>
<span data-ttu-id="f242b-103">Wykonaj kopię zapasową określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="f242b-103">Back up a specific location.</span></span>

## <span data-ttu-id="f242b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f242b-104">SYNTAX</span></span>

### <span data-ttu-id="f242b-105">Utwórz kopię zapasową (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f242b-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f242b-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="f242b-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f242b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f242b-107">DESCRIPTION</span></span>
<span data-ttu-id="f242b-108">Wykonaj kopię zapasową określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="f242b-108">Back up a specific location.</span></span>

## <span data-ttu-id="f242b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f242b-109">EXAMPLES</span></span>

### <span data-ttu-id="f242b-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f242b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="f242b-111">Rozpocznij tworzenie kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f242b-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="f242b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f242b-112">PARAMETERS</span></span>

### <span data-ttu-id="f242b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f242b-113">-AsJob</span></span>
<span data-ttu-id="f242b-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="f242b-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f242b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f242b-115">-Force</span></span>
<span data-ttu-id="f242b-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f242b-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f242b-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f242b-117">-Location</span></span>
<span data-ttu-id="f242b-118">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f242b-118">Name of the backup location.</span></span>

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

### <span data-ttu-id="f242b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f242b-119">-ResourceGroupName</span></span>
<span data-ttu-id="f242b-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f242b-120">Name of the resource group.</span></span>

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

### <span data-ttu-id="f242b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f242b-121">-ResourceId</span></span>
<span data-ttu-id="f242b-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f242b-122">The resource id.</span></span>

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

### <span data-ttu-id="f242b-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f242b-123">-Confirm</span></span>
<span data-ttu-id="f242b-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f242b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f242b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f242b-125">-WhatIf</span></span>
<span data-ttu-id="f242b-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f242b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f242b-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f242b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f242b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f242b-128">CommonParameters</span></span>
<span data-ttu-id="f242b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f242b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f242b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f242b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f242b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f242b-131">INPUTS</span></span>

## <span data-ttu-id="f242b-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f242b-132">OUTPUTS</span></span>

### <span data-ttu-id="f242b-133">Microsoft. AzureStack. Management. Backup. admin. models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="f242b-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="f242b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f242b-134">NOTES</span></span>

## <span data-ttu-id="f242b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f242b-135">RELATED LINKS</span></span>
