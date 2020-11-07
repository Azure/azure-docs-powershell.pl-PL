---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 460d24e091a702cfee32b8c5b7d9c3a8016e73b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888710"
---
# <span data-ttu-id="0cfd7-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="0cfd7-101">Start-AzsBackup</span></span>

## <span data-ttu-id="0cfd7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0cfd7-102">SYNOPSIS</span></span>
<span data-ttu-id="0cfd7-103">Wykonaj kopię zapasową określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-103">Back up a specific location.</span></span>

## <span data-ttu-id="0cfd7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0cfd7-104">SYNTAX</span></span>

### <span data-ttu-id="0cfd7-105">Utwórz kopię zapasową (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0cfd7-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0cfd7-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="0cfd7-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cfd7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0cfd7-107">DESCRIPTION</span></span>
<span data-ttu-id="0cfd7-108">Wykonaj kopię zapasową określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-108">Back up a specific location.</span></span>

## <span data-ttu-id="0cfd7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0cfd7-109">EXAMPLES</span></span>

### <span data-ttu-id="0cfd7-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="0cfd7-110">EXAMPLE 1</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="0cfd7-111">Rozpocznij tworzenie kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="0cfd7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0cfd7-112">PARAMETERS</span></span>

### <span data-ttu-id="0cfd7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cfd7-113">-AsJob</span></span>
<span data-ttu-id="0cfd7-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfd7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0cfd7-115">-Force</span></span>
<span data-ttu-id="0cfd7-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-116">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfd7-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0cfd7-117">-Location</span></span>
<span data-ttu-id="0cfd7-118">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-118">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfd7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cfd7-119">-ResourceGroupName</span></span>
<span data-ttu-id="0cfd7-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-120">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfd7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cfd7-121">-ResourceId</span></span>
<span data-ttu-id="0cfd7-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-122">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cfd7-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0cfd7-123">-Confirm</span></span>
<span data-ttu-id="0cfd7-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfd7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cfd7-125">-WhatIf</span></span>
<span data-ttu-id="0cfd7-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cfd7-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfd7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cfd7-128">CommonParameters</span></span>
<span data-ttu-id="0cfd7-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cfd7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cfd7-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cfd7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cfd7-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cfd7-131">INPUTS</span></span>

## <span data-ttu-id="0cfd7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0cfd7-132">OUTPUTS</span></span>

### <span data-ttu-id="0cfd7-133">Microsoft. AzureStack. Management. Backup. admin. models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="0cfd7-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="0cfd7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0cfd7-134">NOTES</span></span>

## <span data-ttu-id="0cfd7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cfd7-135">RELATED LINKS</span></span>
