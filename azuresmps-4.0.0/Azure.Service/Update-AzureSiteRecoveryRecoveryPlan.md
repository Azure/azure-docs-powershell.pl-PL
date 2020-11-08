---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5625ED47-BD85-4BF5-9044-2012E5A67BA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1c680adf1d9d850f89cb81e1525a0e0e06eb6c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054980"
---
# <span data-ttu-id="b6291-101">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b6291-101">Update-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="b6291-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6291-102">SYNOPSIS</span></span>
<span data-ttu-id="b6291-103">Aktualizuje plan odzyskiwania w witrynie odzyskiwanie witryny.</span><span class="sxs-lookup"><span data-stu-id="b6291-103">Updates a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="b6291-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6291-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6291-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6291-105">DESCRIPTION</span></span>
<span data-ttu-id="b6291-106">Polecenie cmdlet **Update-AzureSiteRecoveryRecoveryPlan** aktualizuje plan odzyskiwania w usłudze Azure Site Recovery, a następnie go publikuje.</span><span class="sxs-lookup"><span data-stu-id="b6291-106">The **Update-AzureSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="b6291-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6291-107">EXAMPLES</span></span>

### <span data-ttu-id="b6291-108">Przykład 1: aktualizowanie planu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="b6291-108">Example 1: Update a recovery plan</span></span>
```
PS C:\> Update-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="b6291-109">To polecenie powoduje zaktualizowanie określonego planu odzyskiwania, a następnie jego opublikowanie.</span><span class="sxs-lookup"><span data-stu-id="b6291-109">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="b6291-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6291-110">PARAMETERS</span></span>

### <span data-ttu-id="b6291-111">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="b6291-111">-File</span></span>
<span data-ttu-id="b6291-112">Określa plik planu odzyskiwania planu odzyskiwania, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6291-112">Specifies the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6291-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="b6291-113">-Profile</span></span>
<span data-ttu-id="b6291-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6291-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6291-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b6291-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6291-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="b6291-116">-WaitForCompletion</span></span>
<span data-ttu-id="b6291-117">Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji przed zwróceniem sterowania do konsoli programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b6291-117">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="b6291-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6291-118">CommonParameters</span></span>
<span data-ttu-id="b6291-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6291-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6291-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6291-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6291-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6291-121">INPUTS</span></span>

## <span data-ttu-id="b6291-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6291-122">OUTPUTS</span></span>

## <span data-ttu-id="b6291-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6291-123">NOTES</span></span>

## <span data-ttu-id="b6291-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6291-124">RELATED LINKS</span></span>

[<span data-ttu-id="b6291-125">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b6291-125">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="b6291-126">Nowe — AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b6291-126">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="b6291-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b6291-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)


