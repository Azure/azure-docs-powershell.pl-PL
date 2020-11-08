---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: E214AFEB-90A6-4553-94D4-FBEA6ADE572E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee340c2302670628bb8a3893567d7f8a2da754f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055406"
---
# <span data-ttu-id="affb3-101">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="affb3-101">Resume-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="affb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="affb3-102">SYNOPSIS</span></span>
<span data-ttu-id="affb3-103">Wznawia wstrzymane zadanie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="affb3-103">Resumes a suspended Site Recovery job.</span></span>

## <span data-ttu-id="affb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="affb3-104">SYNTAX</span></span>

### <span data-ttu-id="affb3-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="affb3-105">ByObject (Default)</span></span>
```
Resume-AzureSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="affb3-106">ById</span><span class="sxs-lookup"><span data-stu-id="affb3-106">ById</span></span>
```
Resume-AzureSiteRecoveryJob -Id <String> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="affb3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="affb3-107">DESCRIPTION</span></span>
<span data-ttu-id="affb3-108">Polecenie cmdlet **Resume-AzureSiteRecoveryJob** Wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="affb3-108">The **Resume-AzureSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="affb3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="affb3-109">EXAMPLES</span></span>

### <span data-ttu-id="affb3-110">Przykład 1: Wznów wszystkie zadania</span><span class="sxs-lookup"><span data-stu-id="affb3-110">Example 1: Resume all jobs</span></span>
```
PS C:\> $Jobs = Get-AzureSiteRecoveryJob  
PS C:\> Resume-AzureSiteRecoveryJob -Job $Jobs
ID               : d16397fb-cdf1-4972-b677-c333f3c557b4
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : Suspended
StateDescription : WaitingForManualAction
StartTime        : 10/6/2014 10:19:28 AM
EndTime          : 10/6/2014 10:19:31 AM
AllowedActions   : {Cancel, RestartTestFailoverCleanup}
Name             : Test failover
Tasks            : {Recovery plan preflight checks, Create test environment, All groups failover: Pre steps (1), 
                   Recovery plan failover...} 
Errors           : {}
```

<span data-ttu-id="affb3-111">Pierwsze polecenie pobiera wszystkie zadania odzyskiwania witryny Azure dla bieżącego magazynu odzyskiwania witryny przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryJob** , a następnie zapisuje wyniki w zmiennej $jobs.</span><span class="sxs-lookup"><span data-stu-id="affb3-111">The first command gets all the Azure Site Recovery jobs for the current Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="affb3-112">Drugie polecenie wznowi zadanie określone przez $Jobs.</span><span class="sxs-lookup"><span data-stu-id="affb3-112">The second command resumes the job specified by $Jobs.</span></span>

## <span data-ttu-id="affb3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="affb3-113">PARAMETERS</span></span>

### <span data-ttu-id="affb3-114">-Komentarze</span><span class="sxs-lookup"><span data-stu-id="affb3-114">-Comments</span></span>
<span data-ttu-id="affb3-115">Określa komentarze dotyczące dziennika zadań.</span><span class="sxs-lookup"><span data-stu-id="affb3-115">Specifies the comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affb3-116">-ID</span><span class="sxs-lookup"><span data-stu-id="affb3-116">-Id</span></span>
<span data-ttu-id="affb3-117">Określa identyfikator zadania do wznowienia.</span><span class="sxs-lookup"><span data-stu-id="affb3-117">Specifies the ID of a job to resume.</span></span>

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

### <span data-ttu-id="affb3-118">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="affb3-118">-Job</span></span>
<span data-ttu-id="affb3-119">Określa zadanie, które ma zostać wznowione.</span><span class="sxs-lookup"><span data-stu-id="affb3-119">Specifies the job to resume.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="affb3-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="affb3-120">-Profile</span></span>
<span data-ttu-id="affb3-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="affb3-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="affb3-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="affb3-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="affb3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affb3-123">CommonParameters</span></span>
<span data-ttu-id="affb3-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="affb3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affb3-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="affb3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affb3-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="affb3-126">INPUTS</span></span>

## <span data-ttu-id="affb3-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="affb3-127">OUTPUTS</span></span>

## <span data-ttu-id="affb3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="affb3-128">NOTES</span></span>

## <span data-ttu-id="affb3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="affb3-129">RELATED LINKS</span></span>

[<span data-ttu-id="affb3-130">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="affb3-130">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="affb3-131">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="affb3-131">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="affb3-132">Zatrzymaj — AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="affb3-132">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


