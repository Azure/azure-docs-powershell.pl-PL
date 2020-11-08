---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054549"
---
# <span data-ttu-id="7883e-101">Get-AzureSiteRecoveryRecoveryPlanFile</span><span class="sxs-lookup"><span data-stu-id="7883e-101">Get-AzureSiteRecoveryRecoveryPlanFile</span></span>

## <span data-ttu-id="7883e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7883e-102">SYNOPSIS</span></span>
<span data-ttu-id="7883e-103">Pobiera plan odzyskiwania witryny Azure w formacie XML.</span><span class="sxs-lookup"><span data-stu-id="7883e-103">Downloads an Azure Site Recovery plan in XML format.</span></span>

## <span data-ttu-id="7883e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7883e-104">SYNTAX</span></span>

### <span data-ttu-id="7883e-105">ByRPObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7883e-105">ByRPObject (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7883e-106">ById</span><span class="sxs-lookup"><span data-stu-id="7883e-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7883e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7883e-107">DESCRIPTION</span></span>
<span data-ttu-id="7883e-108">Polecenie cmdlet **Get-AzureSiteRecoveryRecoveryPlanFile** pobiera plan odzyskiwania witryny Azure w formacie XML.</span><span class="sxs-lookup"><span data-stu-id="7883e-108">The **Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet downloads an Azure Site Recovery plan in XML format.</span></span>
<span data-ttu-id="7883e-109">Za pomocą tego pliku można zaktualizować plan odzyskiwania, a następnie przekazać go do serwera odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="7883e-109">You can use this file to update the recovery plan and then upload it to the Site Recovery server.</span></span>

<span data-ttu-id="7883e-110">Plan odzyskiwania umożliwia zbieranie maszyn wirtualnych w grupie w celu przejęcia awaryjnego i odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7883e-110">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="7883e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7883e-111">EXAMPLES</span></span>

### <span data-ttu-id="7883e-112">Przykład 1: Pobieranie pliku planu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="7883e-112">Example 1: Get a recovery plan file</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="7883e-113">To polecenie korzysta z polecenia cmdlet **Get-AzureSiteRecoveryRecoveryPlan** w celu pobrania planu odzyskiwania, a następnie zapisu go w zmiennej $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="7883e-113">This command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="7883e-114">Drugie polecenie używa polecenia cmdlet **GetAzureSiteRecoveryRecoveryPlanFile** , aby uzyskać plik XML planu odzyskiwania witryny w $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="7883e-114">The second command uses the **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet to get the site recovery plan XML file in $RecoveryPlan.</span></span>
<span data-ttu-id="7883e-115">Polecenie zapisuje plik XML w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="7883e-115">The command stores the XML file at the specified path.</span></span>

## <span data-ttu-id="7883e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7883e-116">PARAMETERS</span></span>

### <span data-ttu-id="7883e-117">-ID</span><span class="sxs-lookup"><span data-stu-id="7883e-117">-Id</span></span>
<span data-ttu-id="7883e-118">Określa identyfikator planu odzyskiwania, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="7883e-118">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="7883e-119">-Path</span><span class="sxs-lookup"><span data-stu-id="7883e-119">-Path</span></span>
<span data-ttu-id="7883e-120">Określa pełną ścieżkę do przechowywania pliku XML planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7883e-120">Specifies the full path to store the recovery plan XML file.</span></span>

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

### <span data-ttu-id="7883e-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="7883e-121">-Profile</span></span>
<span data-ttu-id="7883e-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7883e-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7883e-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7883e-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7883e-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7883e-124">-RecoveryPlan</span></span>
<span data-ttu-id="7883e-125">Określa obiekt **ASRRecoveryPlan** , z którego należy pobrać plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7883e-125">Specifies an **ASRRecoveryPlan** object from which to get the recovery plan.</span></span>
<span data-ttu-id="7883e-126">Aby uzyskać obiekt **ASRRecoveryPlan** , użyj polecenia cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="7883e-126">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="7883e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7883e-127">CommonParameters</span></span>
<span data-ttu-id="7883e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7883e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7883e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7883e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7883e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7883e-130">INPUTS</span></span>

## <span data-ttu-id="7883e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7883e-131">OUTPUTS</span></span>

## <span data-ttu-id="7883e-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7883e-132">NOTES</span></span>

## <span data-ttu-id="7883e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7883e-133">RELATED LINKS</span></span>

[<span data-ttu-id="7883e-134">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7883e-134">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)


