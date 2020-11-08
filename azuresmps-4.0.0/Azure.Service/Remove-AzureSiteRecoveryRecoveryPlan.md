---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: A62D8097-FC26-40E4-803C-09F7979A2A2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91f96e5004446a4490a1d9b78a2dc0c7f3a25cd6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055077"
---
# <span data-ttu-id="28c0c-101">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28c0c-101">Remove-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="28c0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="28c0c-103">Usuwa plan odzyskiwania witryny z witryny odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="28c0c-103">Removes a site recovery plan from Site Recovery.</span></span>

## <span data-ttu-id="28c0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28c0c-104">SYNTAX</span></span>

### <span data-ttu-id="28c0c-105">ByRPObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="28c0c-105">ByRPObject (Default)</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-WaitForCompletion] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28c0c-106">ById</span><span class="sxs-lookup"><span data-stu-id="28c0c-106">ById</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -Id <String> [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28c0c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="28c0c-107">DESCRIPTION</span></span>
<span data-ttu-id="28c0c-108">Polecenie cmdlet **Remove-AzureSiteRecoveryRecoveryPlan** usuwa plan odzyskiwania witryny z bieżącego odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28c0c-108">The **Remove-AzureSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="28c0c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28c0c-109">EXAMPLES</span></span>

### <span data-ttu-id="28c0c-110">Przykład 1: usuwanie planu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="28c0c-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="28c0c-111">W pierwszym poleceniu jest używane polecenie cmdlet **Get-AzureSiteRecoveryRecoveryPlan** w celu pobrania planu odzyskiwania witryny, a następnie zapisanie go w zmiennej $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="28c0c-111">The first command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="28c0c-112">Drugie polecenie usuwa plan odzyskiwania w $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="28c0c-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="28c0c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28c0c-113">PARAMETERS</span></span>

### <span data-ttu-id="28c0c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="28c0c-114">-Force</span></span>
<span data-ttu-id="28c0c-115">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="28c0c-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c0c-116">-ID</span><span class="sxs-lookup"><span data-stu-id="28c0c-116">-Id</span></span>
<span data-ttu-id="28c0c-117">Określa identyfikator planu odzyskiwania, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="28c0c-117">Specifies the ID of the recovery plan to remove.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c0c-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="28c0c-118">-Profile</span></span>
<span data-ttu-id="28c0c-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28c0c-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28c0c-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="28c0c-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c0c-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28c0c-121">-RecoveryPlan</span></span>
<span data-ttu-id="28c0c-122">Określa plan odzyskiwania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="28c0c-122">Specifies the recovery plan to remove.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28c0c-123">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="28c0c-123">-WaitForCompletion</span></span>
<span data-ttu-id="28c0c-124">Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji przed zwróceniem sterowania do konsoli programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28c0c-124">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c0c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28c0c-125">-Confirm</span></span>
<span data-ttu-id="28c0c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28c0c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c0c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c0c-127">-WhatIf</span></span>
<span data-ttu-id="28c0c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28c0c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28c0c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28c0c-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c0c-130">CommonParameters</span></span>
<span data-ttu-id="28c0c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c0c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28c0c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c0c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28c0c-133">INPUTS</span></span>

## <span data-ttu-id="28c0c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28c0c-134">OUTPUTS</span></span>

## <span data-ttu-id="28c0c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28c0c-135">NOTES</span></span>

## <span data-ttu-id="28c0c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28c0c-136">RELATED LINKS</span></span>

[<span data-ttu-id="28c0c-137">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28c0c-137">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="28c0c-138">Nowe — AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28c0c-138">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="28c0c-139">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28c0c-139">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


