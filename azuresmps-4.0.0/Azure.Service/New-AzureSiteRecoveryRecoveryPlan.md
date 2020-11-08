---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2F749E4A-149F-44E0-8AEB-F2C416140906
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d1162ed2c9126942cc6ae31cbe31fdc2ef130d8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054942"
---
# <span data-ttu-id="7185e-101">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7185e-101">New-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="7185e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7185e-102">SYNOPSIS</span></span>
<span data-ttu-id="7185e-103">Tworzy plan odzyskiwania witryny w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="7185e-103">Creates a site recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="7185e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7185e-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7185e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7185e-105">DESCRIPTION</span></span>
<span data-ttu-id="7185e-106">Polecenie cmdlet **New-AzureSiteRecoveryRecoveryPlan** tworzy plan odzyskiwania w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7185e-106">The **New-AzureSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="7185e-107">Plan odzyskiwania umożliwia zbieranie maszyn wirtualnych w grupie w celu przejęcia awaryjnego i odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7185e-107">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="7185e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7185e-108">EXAMPLES</span></span>

### <span data-ttu-id="7185e-109">Przykład 1: Dodawanie planu odzyskiwania do magazynu odzyskiwania witryny</span><span class="sxs-lookup"><span data-stu-id="7185e-109">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\> New-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="7185e-110">To polecenie dodaje plan odzyskiwania o nazwie RecoveryPlan.xml do magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7185e-110">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7185e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7185e-111">PARAMETERS</span></span>

### <span data-ttu-id="7185e-112">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="7185e-112">-File</span></span>
<span data-ttu-id="7185e-113">Określa ścieżkę pliku planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7185e-113">Specifies the path of the recovery plan file.</span></span>

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

### <span data-ttu-id="7185e-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="7185e-114">-Profile</span></span>
<span data-ttu-id="7185e-115">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7185e-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7185e-116">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7185e-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7185e-117">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7185e-117">-WaitForCompletion</span></span>
<span data-ttu-id="7185e-118">Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji przed zwróceniem sterowania do konsoli programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7185e-118">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7185e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7185e-119">CommonParameters</span></span>
<span data-ttu-id="7185e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7185e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7185e-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7185e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7185e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7185e-122">INPUTS</span></span>

## <span data-ttu-id="7185e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7185e-123">OUTPUTS</span></span>

## <span data-ttu-id="7185e-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7185e-124">NOTES</span></span>

## <span data-ttu-id="7185e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7185e-125">RELATED LINKS</span></span>

[<span data-ttu-id="7185e-126">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7185e-126">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="7185e-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7185e-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="7185e-128">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7185e-128">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


